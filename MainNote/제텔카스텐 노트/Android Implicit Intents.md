#Android #Intent 
[[Android URI]]
### 왭사이트 열기
```Java
//주소 받기
String url = mWebesiteEditText.getText().toString(); 
//URI 만들기
Uri webpage = Uri.parse(url);  
//인텐트만들기
Intent intent = new Intent(Intent.ACTION_VIEW, webpage);  

//Acti
if (intent.resolveActivity(getPackageManager()) != null) {  
    startActivity(intent);  
} else {  
    Log.d("ImplicitIntents", "Can't handle this intent!");  
}
```