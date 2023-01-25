#ApsScript #Android #Java 
Android Java 에서 google sheet api를 사용하는것이 힘들어서
Android Java로 AppsScript를 실행시키고 AppsScript에서 google sheet를 사용하는 방식을 사용했다.

우선 코드다
Android Java
```Java
package com.example.googlesheets;  
  
import androidx.annotation.Nullable;  
import androidx.appcompat.app.AppCompatActivity;  
  
import android.app.ProgressDialog;  
import android.content.Intent;  
import android.os.Bundle;  
import android.view.View;  
import android.widget.Button;  
import android.widget.EditText;  
  
import com.android.volley.AuthFailureError;  
import com.android.volley.DefaultRetryPolicy;  
import com.android.volley.Request;  
import com.android.volley.RequestQueue;  
import com.android.volley.Response;  
import com.android.volley.RetryPolicy;  
import com.android.volley.VolleyError;  
import com.android.volley.toolbox.StringRequest;  
import com.android.volley.toolbox.Volley;  
  
import java.io.IOException;  
import java.security.GeneralSecurityException;  
import java.util.HashMap;  
import java.util.Map;  
  
public class MainActivity extends AppCompatActivity {  
  
    @Override  
    protected void onCreate(Bundle savedInstanceState) {  
        super.onCreate(savedInstanceState);  
        setContentView(R.layout.activity_main);  

		start();
    }  
  
    public void start() {  
        String sName = "a";  
        String sPhone = "b";  
        String sAddress = "c";  
  
        StringRequest stringRequest = new StringRequest(Request.Method.POST, "https://script.google.com/macros/s/AKfycbw0o541rCPujyCnGFy5qVrKCLHX3jpaHvE2A7olEo5gtikcEwheB__3Dj6i7V__rfs8/exec", new Response.Listener<String>() {  
            @Override  
            public void onResponse(String response) {  
                System.out.println("SUCCESS");  
            }  
        }, new Response.ErrorListener() {  
            @Override  
            public void onErrorResponse(VolleyError error) {  
                System.out.println("NOT");  
            }  
        }){  
            @Nullable  
            @Override            protected Map<String, String> getParams() throws AuthFailureError {  
                Map<String,String> params = new HashMap<>();  
                params.put("action","addStudent");  
                params.put("vName", sName);  
                params.put("vPhone", sPhone);  
                params.put("vAddress",sAddress);  
  
                return params;  
            }  
        };  
  
        int socketTimeout = 50000;  
        RetryPolicy retryPolicy = new DefaultRetryPolicy(socketTimeout,0,DefaultRetryPolicy.DEFAULT_BACKOFF_MULT);  
        stringRequest.setRetryPolicy(retryPolicy);  
  
        RequestQueue requestQueue = Volley.newRequestQueue(this);  
        requestQueue.add(stringRequest);  
    }  
}

```