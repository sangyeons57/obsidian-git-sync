#Java #GoogleSheet #GoogleSheetAPI 

여러가지 방법을 시도했은데 최종적으로 성공한 방법을 적겠다
[[Java Google Sheet API & OAuth]] 에 관련 내용있다.

gradle.build
```gradle

apply plugin: 'java'  
apply plugin: 'application'  
  
mainClassName = 'SheetsQuickstart'  
sourceCompatibility = 1.8  
targetCompatibility = 11  
version = '1.0'  
  
repositories {  
    mavenCentral()  
}  
  
dependencies {  
    implementation 'com.google.api-client:google-api-client:2.0.0'  
    implementation 'com.google.oauth-client:google-oauth-client-jetty:1.34.1'  
    implementation 'com.google.apis:google-api-services-sheets:v4-rev20221216-2.0.0'  
  
    implementation 'com.google.auth:google-auth-library-oauth2-http:1.11.0'  
    implementation 'com.google.apis:google-api-services-drive:v3-rev20220815-2.0.0'  
    implementation 'com.google.apis:google-api-services-sheets:v4-rev20220927-2.0.0'  
  
}

```

Java file
```Java

```