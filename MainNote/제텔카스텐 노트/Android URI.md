#Android #Java #URI #url 
### URI : URI는 특정 리소스를 식별하는 통합 식별자(Uniform Resource Identifier)를 의미한다. 웹기술에서 사용하는 논리적 물리적 리소스를 식별하는 고유한 문자열 시퀀스
### URL: 웹주소, 컴퓨터 네트워크상에서 리서스가 어디있는지 알려주기 위한 규약. URI의 서브셋이다
URI가 더 큰 범위
URI: 식별자
URL: 주소
```Java
Intent intent = new Intent
```
   // Get the string indicating a location. Input is not validated; it is   // passed to the location handler intact.   String loc = mLocationEditText.getText().toString();   // Parse the location and create the intent.   Uri addressUri = Uri.parse("geo:0,0?q=" + loc);   Intent intent = new Intent(Intent.ACTION_VIEW, addressUri);   // Find an activity to handle the intent, and start that activity.   if (intent.resolveActivity(getPackageManager()) != null) {       startActivity(intent);   } else {       Log.d("ImplicitIntents", "Can't handle this intent!");   }
```
```