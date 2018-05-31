# lagou
#### 拉钩网页面
* 判断滚动条是否滚到底部,滚到底部添加bottom-ab移除bottom-tip,反之。
```
$(window).scroll(function(){
	  var bottomEndHeight = $(".bottom-end").height() + 60;
	  var bodyHeight = $("body").height();//body高度
	  var windowHeight = $(window).height();//浏览器高度
	  var scrollHeight = $(window).scrollTop();//滚动条在Y轴的滚动距离
	  if((scrollHeight + windowHeight) >= (bodyHeight - bottomEndHeight)) {
	       $(".bottom-middle").addClass("bottom-ab").removeClass("bottom-tip")
	 }else {
	 $(".bottom-middle").addClass("bottom-tip").removeClass("bottom-ab")
	 }
})
```
#### 登录页面
* 用户需输入"手机号"，"密码",判断输入的手机号与密码是否正确，正确即登录成功。
```
$(".login").click(function(){
       var number = "13844109895";
       var password = "123456";
       var enterUserName = $("input[name='number']").val();
       var enterPassword = $("input[name='password']").val();
       if(enterUserName == number && enterPassword == password){
           alert("登录成功！");
           location.href="http://www.baidu.com";
      }else {
           alert("登陆失败！");
      }
})
```
