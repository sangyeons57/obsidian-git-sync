#Android #Java 

spiiner만들기 전체적인 코드

layout xml 파일
 ``` xml
<Spinner  
    android:id="@+id/label_spinner"  
    android:layout_width="0dp"  
    android:layout_height="wrap_content"  
    android:layout_marginEnd="24dp"  
    android:layout_marginRight="24dp"  
    android:layout_marginStart="8dp"  
    android:layout_marginLeft="8dp"  
    android:layout_marginTop="24dp"  
    app:layout_constraintEnd_toEndOf="parent"  
    app:layout_constraintStart_toEndOf="@id/phone_text"  
    app:layout_constraintTop_toBottomOf="@id/address_text" />
```

String array
``

Java code
``` Java
public class OrderActivity extends AppCompatActivity implements AdapterView.OnItemSelectedListener {  
  
    @Override  
    protected void onCreate(Bundle savedInstanceState) {  
        super.onCreate(savedInstanceState);  
        setContentView(R.layout.activity_order);  
  
        Spinner spinner = findViewById(R.id.label_spinner);  
        if (spinner != null) {  
            spinner.setOnItemSelectedListener(this);  
        }  
        ArrayAdapter<CharSequence> adapter = ArrayAdapter.createFromResource(this,  
                R.array.labels_array, android.R.layout.simple_spinner_item);  
  
        if (spinner != null) {  
            spinner.setAdapter(adapter);  
        }  
    }

  
@Override  
	public void onItemSelected(AdapterView<?> parent, View view, int position, long id) {  
	    String spinnerLabel = parent.getItemAtPosition(position).toString();  
	    displayToast(spinnerLabel);  
	  
	}  
	  
	@Override  
	public void onNothingSelected(AdapterView<?> parent) {  
	  
	}
}
```