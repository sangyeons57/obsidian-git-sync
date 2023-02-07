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

//Activity가 존제할경우 실행하는 코드인데 잘 작동하지가 않는다.
if (intent.resolveActivity(getPackageManager()) != null) {  
    startActivity(intent);  
} else {  
    Log.d("ImplicitIntents", "Can't handle this intent!");  
}
```


### 구글맵 검색
```Java
//검색어
String loc = mLocationEditText.getText().toString();  
//여기가 검색부분같은데 왜 맵이 실행 되는지는 모르겠다
//아마 "geo:0,0?q"
Uri addressUri = Uri.parse("geo:0,0?q=" + loc);  
Intent intent = new Intent(Intent.ACTION_VIEW, addressUri);  
  
if (intent.resolveActivity(getPackageManager()) != null) {  
    startActivity(intent);  
} else {  
    Log.d("ImplictIntents", "Can't handle this intent!");  
}
```