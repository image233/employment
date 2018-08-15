<template>
<center>
    <div id="brochure" >
        <div class="brav">
            <div class="bravmain">
                <form action="">
                    <div class="search">
                        <input name="keyword" type="text" placeholder="请输入关键词" class="gj">
                        <input name="" type="text" placeholder="发布时间" class="sj">
                        <a href=""><img class="se" src="static/frontPage/imgs/sea.jpg"><span>搜索</span></a>
                    </div>
                    <div class="info">
                    <div class="zk">
                        <p>企事业招考</p>
                    </div>
                    <div class="xx">
                        <ul >
                            <li v-for="ruleList in rulesList">
                                <span class="triangle-rihgt"></span>
                                <a  :href="['secleveDetail.html?id='+ruleList.id]" >{{ruleList.title}}</a>
                                <!-- <span >{{ruleList.auther}}</span> -->
                                <time >{{ruleList.time}}</time>
                            </li>
                            <li>
                                <span class="triangle-rihgt"></span>
                                <router-link to="/frontPage/secleveDetail">佛山市三水区部分医疗卫生单位赴高校招聘简章</router-link>
                                <!-- <span >{{ruleList.auther}}</span> -->
                                <time >2017-12-28</time>
                                <div class="clear"></div>
                            </li>
                            <li>
                                <span class="triangle-rihgt"></span>
                                <router-link to="/frontPage/secleveDetail">长春市壹诺教育图书发行有限公司招聘简章</router-link>
                                <time >2017-12-28</time>
                                <div class="clear"></div>
                            </li>
                            <li>
                                <span class="triangle-rihgt"></span>
                                <router-link to="/frontPage/secleveDetail">长春市百顺兴汽车贸易有限公司招聘简章</router-link>
                                <time >2017-12-28</time>
                                <div class="clear"></div>
                            </li>
                            <li>
                                <span class="triangle-rihgt"></span>
                                <router-link to="/frontPage/secleveDetail">长春市西三角咨询服务有限公司招聘简章</router-link>
                                <time >2017-12-28</time>
                                <div class="clear"></div>
                            </li>
                        </ul>
                    </div>
                        <div class="pages"> 
                            <span>14条数据&nbsp;&nbsp;共8页&nbsp;&nbsp;</span>
                            <ul  id="yw0"><li ><a href="">首页</a></li>
                                <li ><a href="">&lt;&lt;</a></li>
                                <li  class="here"><a href="">1</a></li>
                                <li ><a href="">2</a></li>
                                <li ><a href="">&gt;&gt;</a></li>
                                <li ><a href="">末页</a></li>
                            </ul>
                        </div>
                    </div>
                </form>
                
			<!-- <div class="css-footer" style="margin:0 auto">
		        <p>吉ICP备88888888号&nbsp;&nbsp;&nbsp;&nbsp;地址：吉林省长春市前进大街1888号&nbsp;&nbsp;&nbsp;&nbsp;邮编：130000</p>
		        <p>Copyright 2012 版权所有 吉林省高校招生就业指导服务中心(吉林省教育人才服务中心) All Right Reserved 技术支持：福瑞科技</p>
				
			</div> -->
            </div>
        </div>
    </div>

</center>
</template>

<script>


</script>
<style lang="scss" scoped>
ul{
	padding:0px;
	list-style: none;
}
input:focus{outline:none;}
.clear {
    clear:both; 
    height: 0; 
    line-height: 0; 
    font-size: 0;
}
.brav{
	width: 100%;
	height: 100%;
	background-color: #f5f5f5;
	padding-top:1px;
}
.bravmain{
	width: 1200px;
	margin: 0 auto;
	background-color: #f5f5f5;
	margin-top:10px;
}
.search{
	height: 62px;
	width: 100%;
	margin-bottom: 10px;
	background-color: #fff;
}
.gj{
	width: 440px;
	margin:10px;
}
.gj,.sj{
	height: 40px;
	float: left;
	text-indent: 10px;
	border:none;
	background-color: #f3f3f3;
}
.sj{
	width: 356px;
	margin:10px 0;
}
.se{
	width: 33px;
	height: 40px;
}
.search a{
	margin:10px;
	width:68px;
	display:inline-block;
    height:40px;
}
.search span{
	float: right;
	line-height: 40px;
	color: #22549b;
	font-weight: bold;
}
.info{
	font-size:16px;
	background-color: #fff;
}
.zk{
	width:1200px;
	height: 46px;
	line-height:46px;
	border-bottom: 1px solid #2577e3;
}
.zk p{
    float: left;
	display: block;
	width: 164px;
	text-align: center;
	letter-spacing: 1px;
	color:#fff;
	background-color:#2577e3;
}
.xx{
	font-size: 16px;
}
.xx li{
	width: 1200px;
	padding: 10px 0px;
	border-bottom:1px solid #f3f3f3;
}
.xx li:hover{
	background-color:#deebfc;
}
.triangle-rihgt {
	display:block;
	float: left;
	height:0;
	width:0;
	border:4px solid #2576e1;
	border-color:transparent  transparent transparent #2576e1;
	margin:10px 10px 0 30px;
}
.xx a{
	color: #2378e3;
    float: left;
}
.xx time{
	float: right;
	color: #2378e3;
	margin-right:30px;
}
.pages{
	height:60px;
	width: 380px;
	margin: 10px auto;
	text-align: center;
	font-size: 14px;
	color: #333331;
}
.pages span{
	float: left;
}
.pages ul{
	height:60px;
	/*margin: 0px auto;*/
}
.pages li{
	float: left;
	margin-right: 6px;
	border:1px solid #dcdcdc;
}
.pages a {
	width: 100%;
	padding:6px 4px;
	height: 100%;
	color: #333331;
}
.pages li:hover{
	color: #333331;
}
.here{
	color: #fff;
	background-color: #2677e3;
}
.here a {
	color: #fff;
}

</style>