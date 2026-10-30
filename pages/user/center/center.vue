<template>
	<div>
		<div id="head">
			<ul>
				<li><a href="http://www.sdau.edu.cn/" target="blank">每日推荐</a></li>
				<li><a href="https://sdau.metaersp.com/personalIndex" target="blank">知识图谱</a></li>
				<li><a href="https://library.sdau.edu.cn/12089/list.htm" target="blank">个人中心</a></li>
			</ul>
		</div>
		<div>
			<section id="content">
				<div class="header">
					<a href="javascript:;" class="current">我要登录</a>
					<a href="javascript:;">我要注册</a>
				</div>
				<div id=body>
					<div class="dom" style="display: block;">
						<form action="UserLogin" method="post">
							<input name="loginjudge" value="null" type="hidden">
							<div id="s1">
								<h>账号</h>
								<input id="input" type="text" name="account" class="input-item">
							</div>
							<div id="s1">
								<h>密码</h>
								<input id="input" type="password" name="password" class="input-item">
							</div>
							<div id="s1">
								<td colspan="2"><img id="img" src="checkCodeServlet" alt=""></td>
							</div>
							<input id="button" type="submit" value="登&nbsp;录">
						</form>
						<div class="other" align="center">
							<a href="#">找回密码</a>
							<span>|</span>
							<span>还没有注册?</span>
							<a href="userLogin.jsp">立即注册</a>
						</div>
					</div>
					<div class="dom">
						<form action="UserRegister" method="post">
							<input name="loginjudge" value="null" type="hidden">
							<div id="s1">
								<h>账号</h>
								<input id="input" name="account" type="text" placeholder="10位数字">
							</div>
							<div id="s1">
								<h>昵称</h>
								<input id="input" name="name" type="text" placeholder="3-5位英文字母">
							</div>
							<div id="s1">
								<h>密码</h>
								<input id="input" name="password" type="password" placeholder="6-10位英文、数字、下划线, 区分大小写">
							</div>
							<input id="button" type="submit" value="注&nbsp;册">
						</form>
						<div class="other" align="center">
							已有账号？<a href="userLogin.jsp">去登陆</a>
						</div>
					</div>
				</div>
			</section>
		</div>
	</div>
</template>

<script>
	window.onload = function() {
		let as = document.getElementsByClassName('header')[0].getElementsByTagName('a');
		let contents = document.getElementsByClassName('dom');
		for (let i = 0; i < as.length; i++) {
			let a = as[i];
			a.id = i;
			a.onclick = function() {
				for (let j = 0; j < as.length; j++) {
					as[j].className = '';
					contents[j].style.display = 'none';
				}
				this.className = 'current';
				contents[this.id].style.display = 'block';
			}
		}
	}
</script>

<style type="text/css">
	#head {
		padding-left: 340px;
		width: 100%;
		height: 50px;
	}

	#head ul {
		float: center;
	}

	#head ul li {
		float: left;
	}

	#head ul li a {
		display: block;
		width: 257px;
		color: black;
		background-color: white;
		text-align: center;
		text-decoration: none;
		margin: 0;
		padding-top: 10px;
		padding-bottom: 10px;
		font-size: 20px;
	}

	#head ul li a:hover {
		background-color: gray;
	}

	* {
		text-decoration: none;
	}

	a {
		color: blue;
	}

	#content {
		border: solid 2px #d5d5d5;
		width: 25rem;
		height: 33rem;
		background-color: transparent;
		margin: 0 auto;
		margin-top: 2%;
		float: center;
	}

	.header a {
		width: 50%;
		height: 60px;
		background-color: #ffffff;
		display: inline-block;
		float: left;
		text-align: center;
		line-height: 60px;
		color: #b8b8b8;
	}

	.header a.current {
		background-color: transparent;
		color: #000000;
	}

	#body {
		margin: 2rem;
	}

	.dom {
		width: 100%;
		display: none;
		margin-top: 6rem;
	}

	#input {
		width: 100%;
		height: 2rem;
		margin-top: 0.5rem;
		padding-left: 0.5rem;
		border-radius: 5px;
		border: 1px solid #7a7a7a;
	}

	#s1 {
		margin-bottom: 1rem;
	}

	#button {
		width: 100%;
		height: 3rem;
		border: none;
		font-size: 1.5em;
		color: #fff;
		background-image: linear-gradient(to right, #006400 0%, #9ACD32 100%);
		border-radius: 3px;
		margin-bottom: 1rem;
	}

	body {

		background-repeat: no-repeat;
		background-size: 100% auto;
	}
</style>