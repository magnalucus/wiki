## API

### api의 필요성

커뮤니티 또는 각 게임에서 블록체인을 이용하기 위해서는 여러가지 종류의 프로그래밍을 두루 사용 할 줄 알아야한다. 이로인해 블록체인을 접목하기 쉽지 않기 때문에 블록체인을 좀 더 쉽게 사용할 수 있는 api 제작 프로젝트를 시작한다.


## API 개발

### API client 등록하기

https://api.ethersocial.network/v1/apikey/request/ 에서 자신의 서비스를 등록한 후 api key를 생성, 저장한다.


### ESN 주소 등록하기

https://api.ethersocial.network/v1/registaddress?address=$address&apikey=$apikey

* $address - ESN 지갑주소
* $apikey - api key

예제
```javascript
curl "https://api.ethersocial.network/v1/registaddress?address=0x64A2a64c80859f39f3329e2009bbdfCea04414ed&apikey=099DAD8DE10A3E6AEDB18C06A66D13943C226F4E48BF8369702ECD4C80E363F1"
```

Response: 200 OK, application/json

```javascript
{"address":"0x64A2a64c80859f39f3329e2009bbdfCea04414ed","error":null}
```

    