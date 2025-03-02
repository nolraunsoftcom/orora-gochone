# 생활배달 설정 순서

### 1. 프로젝트 ID 변경

- com.orora.\*

### 2. 앱이름 변경

- /android/app/src/main/res/values/strings.xml
- /app.json
- /ios/pungmuprugio/Info.plist

### 앱 아이콘 변경

### 스플레시 이미지 변경

### 파이어베이스 세팅

1. 위 프로젝트 ID로 ios/aos 프로젝트 세팅
2. 각 os별 파일 세팅
3. files내 푸시키 등록

### aos 운영키 등록

```
keytool -genkey -v -keystore orora.keystore -alias orora -keyalg RSA -keysize 2048 -validity 10000

keytool -exportcert -alias androiddebugkey -keystore ./android/app/debug.keystore -storepass android -keypass android | openssl sha1 -binary | openssl base64
keytool -exportcert -alias androiddebugkey -keystore ./android/app/debug.keystore | openssl sha1 -binary | openssl base64
keytool -exportcert -alias release -keystore ./android/app/release.keystore | openssl sha1 -binary | openssl base64

echo "5E:8F:16:06:2E:A3:CD:2C:4A:0D:54:78:76:BA:A6:F3:8C:AB:F6:25" | xxd -r -p | openssl base64
echo "55:30:5D:F9:08:E6:7A:E6:53:FD:C6:7E:6F:C9:95:44:88:3C:5B:E9" | xxd -r -p | openssl base64

```

~~비밀번호는 주로 프로젝트명+A1! 로 하고있음~~

### gradlew signingReport 등록

### 사운드 등록

---

윗딜브로스 모바일웹
https://witdeal-bros.members.markets/app/set/privacy.php
https://witdeal-bros.members.markets/app/set/set.php

윗딜셀러 모바일웹
https://witdeal-seller.members.markets/app/set/privacy.php
https://witdeal-seller.members.markets/app/set/set.php

윗딜영통신성 모바일웹
https://witdeal-002.members.markets
https://witdeal-002.members.markets/app/set/privacy.php
https://witdeal-002.members.markets/app/set/set.php

태성
김
ororapf@naver.com
+82-1661-0339

apple team id
C3N8GKX588
