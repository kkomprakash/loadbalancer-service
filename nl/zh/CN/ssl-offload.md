---

copyright:
  years: 2017
lastupdated: "2018-03-14"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# SSL 卸载

对于所有入局 HTTPS 连接，负载均衡器服务会终止 SSL 连接并与后端服务器建立明文 HTTP 通信。CPU 密集型 SSL 握手和加密/解密任务将从后端服务器转移开，从而允许它们使用其所有 CPU 周期来处理应用程序流量。 

负载均衡器需要 SSL 证书才能执行 SSL 卸载任务。您可以使用预先存在的 SSL 证书或购买一个新证书，并通过 [IBM Cloud 证书库](https://control.softlayer.com/security/sslcerts)对其进行管理。 

# SSL 密码套件
负载均衡器服务支持具有 SSL 卸载功能的 TLS V1.2。

您的负载均衡器支持以下 SSL 密码：

* ECDHE-RSA-AES256-GCM-SHA384
* ECDHE-RSA-AES256-SHA384
* AES256-GCM-SHA384
* AES256-SHA256
* ECDHE-RSA-AES128-GCM-SHA256
* ECDHE-RSA-AES128-SHA256
* AES128-GCM-SHA256
* AES128-SHA256

如果您的负载均衡器配置了一个或多个 HTTPS 前端应用程序端口（协议），缺省情况下，将针对您的负载均衡器启用所有上述预定义的 SSL 密码。您可以根据需要选择为您的负载均衡器启用其他 SSL 密码。
