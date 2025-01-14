## 白泽百科（端游）
### 请求格式
#### **host：**
```json
GET https://sprite.16163.com/d90/
```

#### **params：**
- `gameid` ：`d90`
- `token` :用于身份验证的JWT,格式为xxx.xxx.xxx。
    - JWT（JSON Web Token）是一种开放标准（RFC 7519），它定义了一种紧凑且自包含的方式，用于在各方之间作为JSON对象安全地传输信息。JWT由三个用点分隔的部分组成：头部（Header）、有效载荷（Payload）和签名（Signature）。

    - 头部xxx，base64解码后如下
    ```json
    {
      "typ": "JWT",
      "alg": "HS256"
    }
    ```
    typ: 表示令牌的类型。在此例中，为“JWT”。
    alg: 表示用于签名的算法。在此例中，为“HS256”（HMAC SHA-256）。
    - 有效载荷，base64解码后如下
    ```json
    {
      "exp": 1736796260,
      "uuid": ""
    }
    ```
    exp: 表示令牌的过期时间，以Unix时间戳格式表示，以毫秒为单位。在此例中，1736796260对应于2025-01-14 
    uuid: 表示用户的唯一标识符。
    - 签名xxx，无需解码。签名部分确保了JWT的完整性和验证发行者的身份。它使用头部中指定的算法（HS256）和一个密钥生成。

- 请求网址：
    ```json
    https://sprite.16163.com/d90/?gameid=d90&token=xxx.xxx.xxx
    ```
#### 参数获取
- 头部固定
    - `eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9`
- 有效载荷,过期时间戳加uuid。
    - uuid:我找了两个例子
    - `d90.5c733b97f726c32bc8fac07c21299ecb`
    - `d90.efb05e8f9d9a95a8186e80da5a8588c1`
    - 都是d90开头，
- 签名
    - 两个例子，已知HS256算法,对称加密。
    - `wWcVGEHKDA9a_UHibBSvo7dYbDVnH4ZicPPUfMmVhJo`
    - `FIUxvHpUXrKUDurG_iZUM2Ax9r4_OPpAnLC1Ah13S7w`
### 请求代码

#### Python（当然是万能的res库啦！）

```python
import requests
url = "https://sprite.16163.com/d90/"
params = {
    "gameid": "d90",
    "token": ""
}
response = requests.get(url, params=params)
print(response.text)
```

#### JavaScript (Fetch API)

```javascript
const url = "https://sprite.16163.com/d90/";
const params = {
    gameid: "d90",
    token: ""
};

fetch(`${url}?gameid=${params.gameid}&token=${params.token}`)
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

#### Java (HttpURLConnection)

```java
import java.net.HttpURLConnection;
import java.net.URL;
import java.util.Map;

public class GameResourceFetcher {
    public static void main(String[] args) {
        String url = "https://sprite.16163.com/d90/";
        Map<String, String> params = Map.of(
            "gameid", "d90",
            "token", ""
        );

        try {
            URL obj = new URL(url);
            HttpURLConnection con = (HttpURLConnection) obj.openConnection();
            con.setRequestMethod("GET");
            con.setDoOutput(true);
            con.setRequestProperty("Content-Type", "application/json");

            String param = "gameid=" + params.get("gameid") + "&token=" + params.get("token");
            con.getOutputStream().write(param.getBytes());

            int responseCode = con.getResponseCode();
            System.out.println("Response Code: " + responseCode);

        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

#### C# (HttpClient)

```csharp
using System;
using System.Net.Http;
using System.Threading.Tasks;

class Program
{
    static async Task Main()
    {
        var url = "https://sprite.16163.com/d90/";
        var parameters = new Dictionary<string, string>
        {
            ["gameid"] = "d90",
            ["token"] = ""
        };

        using (var httpClient = new HttpClient())
        {
            var response = await httpClient.GetAsync($"{url}?gameid={parameters["gameid"]}&token={parameters["token"]}");
            string content = await response.Content.ReadAsStringAsync();
            Console.WriteLine(content);
        }
    }
}
```

