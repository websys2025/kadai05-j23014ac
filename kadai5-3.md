## 外部APIの呼び出しのミニレポート
### Q3-1. 郵便番号APIについて説明せよ。
* エンドポイントと機能
エンドポイントは、https://zipcloud.ibsnet.co.jp/api/search?zipcode="+myForm.zipcode.value と定義している。  
入力された数値（myForm.zipcode.value）を利用してapiで県名、市区町村名、町域名を取得し、${zyusho.address1} ${zyusho.address2} ${zyusho.address3}で表示している。
* リクエストとレスポンスのフォーマット
リクエストはjson形式で行われていて、リクエストボディに含まれている。  
レスポンスは  
{  
  "message": null,  
	"results": [  
		{  
			"address1": "千葉県",  
			"address2": "千葉市若葉区",  
			"address3": "千城台北",  
			"kana1": "ﾁﾊﾞｹﾝ",  
			"kana2": "ﾁﾊﾞｼﾜｶﾊﾞｸ",  
			"kana3": "ﾁｼﾛﾀﾞｲｷﾀ",  
			"prefcode": "12",  
			"zipcode": "2640005"  
		}  
	],  
	"status": 200  
}  
のようになる。  
### Q3-2. 各自で調査したAPIについて説明せよ。
* APIの名称と参照URL
APIの名称はRobohashで、参照URLは https://robohash.org/${id} です。  
* エンドポイントと機能
エンドポイントは、https://robohash.org/${"+myForm.form_data.value+"}と定義している。  
入力された数値（myForm.form_data.value）を利用してapiでロボットの画像を取得し、document.getElementById("result").innerHTML += "<img src=\""+url+"\" alt=\"ロボットの画像\"><br>";で表示している。  
* リクエストとレスポンスのフォーマット
リクエストパラメータは、リクエストボディに含まれている。  
レスポンスは、ロボットの画像1枚である。  
### Q3-3. 感想
* 今回の課題で苦労したこと  
apiの表示の仕方
* 演習を通して理解できたこと  
apiの扱い方
* Web APIの利便性や課題など  
エラーに対するメッセージをいくつか考えた方がよいなと思った。
