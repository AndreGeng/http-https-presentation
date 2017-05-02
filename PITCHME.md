HTTPS

HTTPS它是一个安全通信通道，它基于HTTP开发，用于在客户计算机和服务器之间交换信息。它使用安全套接字层(SSL)进行信息交换，简单来说它是HTTP的安全版,是使用 TLS/SSL 加密的 HTTP 协议。
<div class="fragment">
	![https](https://github.com/AndreGeng/http-https-presentation/blob/master/imgs/figure1.png?raw=true)
</div>


Notes:

ssl 3.0 是tsl1.0的基础, 有人也把tsl1.0叫做ssl 3.1

---

想要理解HTTPS, 需要理解几个概念:
* 对称加密算法
* 非对称加密算法
* CA(Certificate Authority)
* 数字证书
* 摘要/散列算法

Note:

提问: https是对称加密还是非对称加密

---

对称加密算法

常见算法DES, 3DES, AES


<div>
	<div style="display: inline-block; width:50%;">
		<div class="fragment">
			<p>pros:</p>
			<ul>
				<li>算法相对简单, 加密速度快</li>
			</ul>
		</div>
		<div class="fragment">
			<p>cons:</p>
			<ul>
				<li>通信方式1对1, 大量密钥的管理与更新是个问题</li>
				<li>密钥的分发</li>
			</ul>
		</div>

		<div class="fragment">
			公网环境下, 密钥如何的安全传输?
		</div>
	</div>
	<div style="display: inline-block; width:50%;">
		<img src="https://user-gold-cdn.xitu.io/2016/11/30/bd541d3c181738bf8f938bbd09967f05" alt="">
	</div>
</div>

Note:

DES使用的密钥key为8字节, 把64位的明文转成64位的密文.
3DES使用的密钥为64字节
AES 是一个迭代的、对称密钥分组的密码，它可以使用128、192 和 256 位密钥.

---

非对称加密算法

常见算法RSA

<div class="fragment">
	<p>pros:</p>
	<ul>
		<li>安全系数高</li>
		<li>通信方式1对多, server只需拥有一对公私钥就可以和n多客户端通信</li>
	</ul>
</div>

<div class="fragment">
	<p>cons:</p>
	<ul>
		<li>产生密钥麻烦</li>
		<li>加密速度慢</li>
	</ul>
</div>

<div class="fragment">
	如何防止中间人攻击?
</div>

Note:

1977年 R。S、A三人提出。RSA算法是第一个同时用于加密和数字签名的算法。能抵抗大多数密码攻击，秘钥越长越难破解。

RSA目前1024位基本安全，2048位秘钥极其安全

算法基于： 将两个大质数相乘十分容易，但是想要对其乘积进行因式分解却极其困难。

---

CA(Certificate Authority)第三方
