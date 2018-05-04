## ESN API

### api의 필요성

커뮤니티 또는 각 게임에서 ESN 블록체인을 이용하기 위해서는 여러가지 종류의 프로그래밍을 두루 사용 할 줄 알아야한다. 
여러가지 프로그램을 동시에 다루는 것은 쉽지 않으며, 이로인해 블록체인을 접목하기 쉽지 않기에 이를 쉽게 사용하기 위한 ENS API 제작 프로젝트를 시작한다.



## API client 등록하기

https://api.ethersocial.network/request/ 에서 자신의 서비스를 등록한 후 api key를 생성, 저장한다.


## ESN 주소 등록하기

https://api.ethersocial.network/api?module=registaccount?account=$account&apikey=$apikey

* $account - ESN 지갑주소
* $apikey - api key

예제
```javascript
curl "https://api.ethersocial.network/api?module=registaccount?account=0x64A2a64c80859f39f3329e2009bbdfCea04414ed&apikey=099DAD8DE10A3E6AEDB18C06A66D13943C226F4E48BF8369702ECD4C80E363F1"
```

Response: 200 OK, application/json

```javascript
{"account":"0x64A2a64c80859f39f3329e2009bbdfCea04414ed","error":null}
```


## 등록된 주소의 입금내역 확인하기

https://api.ethersocial.network/api?module=account&action=txlist&account=$account&apikey=$apikey

* $account - ESN 지갑주소
* $apikey - api key

최근 10개의 입금 목록을 보여줌

예제
```javascript
curl "https://api.ethersocial.network/v1/tx?account=0x64A2a64c80859f39f3329e2009bbdfCea04414ed&apikey=099DAD8DE10A3E6AEDB18C06A66D13943C226F4E48BF8369702ECD4C80E363F1"
```

Response: 200 OK, application/json

```javascript
{"account":"0x64A2a64c80859f39f3329e2009bbdfCea04414ed","error":null, "txlist":[{"txhash":"0x2ca17681a7c62c45c3b5138e3dee0d9a756088ac08dd7aee04722d26677c7bf9","value","110000000000000000"},{"txhash":"0x04f5f1462c92b9c145b070bde6974d30d4be2da564e52b96a400e4fbfd3444b7","value","3520000000000000000"}]}
```