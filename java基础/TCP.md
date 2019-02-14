##结构演变： OSI 7层模型 ----> TCP/IP 5层模型----->TCP/IP 4层模型   ####
**OSI 7层结构：**应用层、表示层、会话层、传输层、网络层、数据链路层、物理层。  
**TCP/IP 5层模型：**该模型将OSI 7层模型中的最上边的三层合为一层——应用层。  
**TCP/IP 4层模型：**在TCP/IP 5层模型中，因为数据链路层和物理层和硬件有着直接的关系，所以在软件层面将他们合为一层——网络接口层。  
对应关系如下：
<table>    
	<tr>
		<th>OSI 7层模型</th>
		<th>TCP/IP 5层模型</th>
		<th>TCP/IP 4层模型</th>
	</tr>
	<tr>
		<td>应用层</td>
		<td rowspan="3">应用层</td>
		<td rowspan="3">应用层</td>
	</tr> 
  	<tr>
		<td>表示层</td>
	</tr>
	<tr>
		<td>会话层</td>
	</tr> 
	<tr>
		<td>传输层</td>
		<td>传输层</td>
		<td>传输层</td>
	</tr> 
	<tr>
		<td>网络层</td>
		<td>网络层</td>
		<td>网络层</td>
	</tr> 
	<tr>
		<td>数据链路层</td>
		<td>数据链路层</td>
		<td  rowspan="3">网络接口层</td>
	</tr> 
	<tr>
		<td>物理层</td>
		<td>物理层</td>
	</tr> 
</table>

## 建立连接过程：三次握手和四次挥手。
三次握手过程：  
![三次握手](https://github.com/Linhital/Knowledge/blob/master/pic/connect.jpg)  
四次挥手过程：  
![四次挥手](https://github.com/Linhital/Knowledge/blob/master/pic/cut.jpg)  

**为什么需要三次握手？**  
当两次握手建立连接时，请求因为网络延时的原因重新发起时，该连接会建立两次，三次握手就会建立一次连接。  

**为什么需要四次挥手？**  
因为当客户端发起断开连接时，服务器可能会有未返回给客户端的数据。

## Socket嵌套字

socket是JDK对TCP/IP的一个封装。

## HTTP

Http协议是TCP/IP四层模型中应用层中的协议。他是建立在TCP/IP协议的基础上协议，TCP是传输层协议，IP协议是网络层协议。

http的发展过程：http0.9 ——>http 1.0 ——>http1.1——>http2.0  

http 0.9：建立连接只交互一次就断开连接。  
http 1.0：加入了请求头和消息头。  
http 1.1：加入长连接。  
http 2.0：二进制格式传数据，“推送”功能。  

http请求报文结构：  
![request](https://github.com/Linhital/Knowledge/blob/master/pic/request.png)   
http响应报文结构：  
![response](https://github.com/Linhital/Knowledge/blob/master/pic/response.png)  

## HTTPS

利用数据加密、身份验证和消息完整性验证机制
位于应用层和传输层之间，可以为任何基于TCP的应用层协议提供安全保障

数据传输的机密性：利用对称密钥算法对传输的数据进行加密。
身份验证机制：基于证书利用数字签名方法对服务器和客户端进行身份验证，其中客户端的身份验证是可选的。
消息完整性验证：消息传输过程中使用MAC算法来检验消息的完整性。

服务器使用非对称算法，获取私钥和公钥，把公钥交给客户端来加密数据的秘钥，让客户端传回，这就完成私钥的交换，使用该私钥来加/解密传输的内容。

Socket中添加证书的目的是对拥有该证书的服务端进行信任。


	