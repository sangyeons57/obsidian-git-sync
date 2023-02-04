#Android #Java #Intent 

```Java
ActivityResultLauncher<Intent> launchSomeActivity = registerForActivityResult(  
        new ActivityResultContracts.StartActivityForResult(),  
        new ActivityResultCallback<ActivityResult>() {  
            @Override  
            public void onActivityResult(ActivityResult result) {  
                if (result.getResultCode() == Activity.RESULT_OK)  
                {  
	                //Intent실행에서 값이 돌아올경우 실행되는파트
	                result.getData()
	                //위 방법으로 데이터를 받을수있다 예시)
	                result.getData().getStringExtra(다른 Activity의토큰)
				
					String reply = "value";  
                    mReplyTextView.setText(reply); 
                
                }  
            }  
        }  
);


public static String token = "a";
Intent intent = new Intent(현제 Activity.this, 갈려는 Activity.class);
String message = "보낼려는값";
intent.putExtra(token, message);
launchSomeActivity.launch(intent);


```