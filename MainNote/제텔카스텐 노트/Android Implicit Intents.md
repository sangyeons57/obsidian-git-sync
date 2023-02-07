#Android #Intent 

### 왭사이트 열기
```Java
String url = mWebesiteEditText.getText().toString();  
Uri webpage = Uri.parse(url);  
Intent intent = new Intent(Intent.ACTION_VIEW, webpage);  
System.out.println(url);  
startActivity(intent);  
  
System.out.println(getPackageManager());  
System.out.println(intent.resolveActivity(getPackageManager()));  
  
if (intent.resolveActivity(getPackageManager()) != null) {  
    startActivity(intent);  
} else {  
    Log.d("ImplicitIntents", "Can't handle this intent!");  
}
```