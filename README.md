# APISpace 介绍

**本** **API** **服务由** **[APISpace（apispace.com）](https://www.apispace.com/?utm_source=github&utm_term=konghaojiance)** **提供。**

APISpace 是 Eolink 旗下专业的 API 开放与交易平台，为广大企业以及个人开发者提供多维度、全方位的API接口，覆盖短信验证、天气查询、快递物流、OCR文字识别等海量 API 服务，帮助用户快速获取数据，降低获取数据的成本和难度，提升开发效率。

APISpace 提供15种开发语言的代码示例，分别是：

-   Java(OK HTTP)
-   HTTP
-   cURL
-   微信小程序
-   PHP(pecl_http)、PHP(cURL)
-   Python(http.client)、Python(Requests)
-   JavaScript(Jquery AJAX)、JavaScript(XHR)
-   NodeJS(Native)、NodeJS(Request)
-   Ruby(Net:Http)
-   Shell(Httpie)、Shell(cUrl)

  


# **空号检测**

空号检测，也称号码检测，空号过滤，号码筛选等，是基于运营商大数据及流量使用情况返回手机号码状态，比如：实号、空号、风险号等。
**注意：** 该API一次请求支持批量检测1-50个号码，实际次数扣除按号码个数计算。

**使用该产品前，您需要通过** **[https://www.apispace.com/eolink/api/konghao/introduction](https://www.apispace.com/eolink/api/konghao/introduction?utm_source=github&utm_term=konghaojiance)** **申请** **API** **服务。**

本文档末尾提供了 Python(httpClient) 的调用代码示例，可以前往文档末尾查看。

更多代码示例：[https://www.apispace.com/eolink/api/konghao/guidence/](https://www.apispace.com/eolink/api/konghao/guidence/?utm_source=github&utm_term=konghaojiance)



  


### 三大优势


![whiteboard_exported_image (1).png](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b169c3c9c29242cc9f2d7e5ff11a12a4~tplv-k3u1fbpfcp-watermark.image?)
  


### 超多应用场景

空号检测已经广泛被使用于短信群发、电话营销、呼叫中心外包、金融信贷、企业名录等行业，帮助企业有效提高了沟通效率和成交率，降低了营销成本和客户投诉率。


![whiteboard_exported_image.png](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/8d49df7f970f482a973d82b22586d52d~tplv-k3u1fbpfcp-watermark.image?)

  


### 返回示例

```
{
    chargeStatus: "1",
    chargeCount: "2",
    message: "成功",
    data: [{
            mobile: "182*****510",
            lastTime: "1525257960000",
            area: "河南-郑州",
            numberType: "中国移动 GSM",
            chargesStatus: "1",
            status: "1"
        },
        {
            mobile: "182*****511",
            area: "河南-郑州",
            numberType: "中国移动 GSM",
            chargesStatus: "1",
            status: "4"
        }
    ],
    code: "200000"
}
        
```

  


### 服务保障

![image.png](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/a080abd15a534df18d47f0351edeeb24~tplv-k3u1fbpfcp-watermark.image?)
  


### **Python(http.client) 调用代码示例**


```
import http.client

conn = http.client.HTTPSConnection("undefined")

payload = ""

headers = {

}

conn.request("POST","/", payload, headers)

res = conn.getresponse()

data = res.read()

print(data.decode("utf-8"))


```
