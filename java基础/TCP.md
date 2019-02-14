####结构演变： OSI 7层模型 ----> TCP/IP 5层模型----->TCP/IP 4层模型   ####
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

#### 建立连接过程：三次握手和四次挥手。
三次握手过程：  
![三次握手](https://github.com/Linhital/Knowledge/blob/master/pic/connect.jpg)  
四次挥手过程：  
![四次挥手](https://github.com/Linhital/Knowledge/blob/master/pic/cut.jpg)  

为什么需要三次握手？  
当两次握手建立连接时，请求因为网络延时的原因重新发起时，该连接会建立两次，三次握手就会建立一次连接。  
为什么需要四次挥手？  
因为当客户端发起断开连接时，服务器可能会有未返回给客户端的数据。

