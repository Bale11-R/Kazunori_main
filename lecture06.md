# 9月度第6回講義課題

### CloudTrailのログ情報

```json
{
"eventVersion":"1.08",
"userIdentity":{
	"type":"IAMUser",
	"principalId":"AIDAW2D5XEIR6RDEFKGKK",
	"arn":"arn:aws:iam::********user/Kazu_IAMuser",
	"accountId":"********",
	"accessKeyId":"********",
	"userName":"Kazu_IAMuser",
	"sessionContext":{
		"sessionIssuer":{
		},
		"webIdFederationData":{
		},
		"attributes":{
			"creationDate":"2022-11-10T12:50:36Z",
			"mfaAuthenticated":"true"
		}
	}
},
"eventTime":"2022-11-10T13:09:50Z",
"eventSource":"rds.amazonaws.com",
"eventName":"DescribeDBInstances",
"awsRegion":"ap-northeast-1",
"sourceIPAddress":"AWS Internal",
"userAgent":"AWS Internal",
"requestParameters":{
	"dBInstanceIdentifier":"kurata-database-01"
},
"responseElements":null,
"requestID":"e812bf00-3b05-4be8-99f1-93ebf54ed180",
"eventID":"0856f7a7-4c84-490f-b72c-d962e50f3ba0",
"readOnly":true,
"eventType":"AwsApiCall",
"managementEvent":true,
"recipientAccountId":"468415095331",
"eventCategory":"Management",
"sessionCredentialFromConsole":"true"
}
```
* ユーザーのタイプ（IAMUser）とユーザーの名前（ARN）
* イベント発生時刻、イベントの名前（起動されたDBの情報を返す）、発生元（RDS）、リージョン（東京）、発生元IPアドレス（内部ネットワーク）



### CloudWatchによるアラーム設定
##### 「Unhealthy」のとき、アラートを出す設定
* ![アプリ（nginx）未起動時](https://user-images.githubusercontent.com/116282189/201360974-87ed67e2-1019-468a-8c95-b29ad2e98ffa.jpg)
* ![unhealthyAlerm](https://user-images.githubusercontent.com/116282189/201361054-94a34da9-8a20-48b4-8167-f25759d12cdd.jpg)


##### 「healthy」のとき、OKメールを出す設定
* ![アプリ（nginx-unicorn）起動時](https://user-images.githubusercontent.com/116282189/201361220-170a87ab-36c6-4e88-94c3-80cfd9723322.jpg)
* ![healthyAlerm](https://user-images.githubusercontent.com/116282189/201361267-946818f7-135c-417a-92d7-d245e2e9aca1.jpg)


### 見積のURL
* https://calculator.aws/#/estimate?id=8734472245aa792cee71ca779040109eca2b3945


### 今までの利用料
* ![2022年10月利用料](https://user-images.githubusercontent.com/116282189/201361692-06d1d3f4-1bff-4458-9a02-7e0e93163dcb.jpg)
* ![2022年11月利用料](https://user-images.githubusercontent.com/116282189/201361732-3aa5accd-d65c-474b-9fd9-89ba0f6af13e.jpg)


### 感想
##### ログの確認や監視、アラート設定など、運用の実務業務を疑似体験しているようで、非常にためになった。「ログを取っていないのは話にならない」は、今後の人生において肝に銘じながら生きていく。
