# study
尚未參考完的資料  
## HMAC-SHA1 演算法
VITO の 學習筆記 http://vito-note.blogspot.tw/2012/05/3.html  
Protect a REST service using HMAC (Play 2.0) http://www.smartjava.org/content/protect-rest-service-using-hmac-play-20  
http://blog.csdn.net/janronehoo/article/details/7590976  
## MackDown
Markdown語言詳解 https://read01.com/J848LL.html  
## 其他
緩存 http://blog.csdn.net/feng8888bbb/article/details/69106186

## 加密技巧
    public static String get(String url, String key) {
        Object b = null;
        String signature = null;

        try {
            byte[] b1 = HmacSHA1.getHmacSHA1Encrypt(url, key);
            signature = new String(Base64.encode(b1, 0), Charset.forName("UTF-8"));
        } catch (Exception var5) {
            var5.printStackTrace();
        }

        return signature.replaceAll("\\s+", "");
    }
signature = SignatureUtils.get("email=" + email + "&pwd=" + password, "123456789" + date);
signature = URLEncoder.encode(signature, "UTF-8");

日期:20170607  
修改前(登入):id=null&token=null&pwd=E6fv3TH84d79   
修改前(未登入):&pwd=E6fv3TH84d79  
加密後:8FWh7NnqvwSlI/NR3LRpb5xo7UI=  
UTF8編碼後:8FWh7NnqvwSlI%2FNR3LRpb5xo7UI%3D  
URL:  
http://tnpasstest.ddns.net/apiv1_android/home?id=22&token=p85DR2SZ9SFjtdPXpbDC&signature=8FWh7NnqvwSlI%2FNR3LRpb5xo7UI%3D  
指南針APP:  
http://apps.friday.tw/news/?p=19487
