<template>
    <div style="background-color:#015fbc;">
        <div class="toplogo">
        <img src="static/branch/img//logo.png">

    </div>
    <div class="nav">
        <ul>
            <li><a href="#">主页</a></li>
            <li><a href="#">学生</a></li>
            <li><a href="#">单位</a></li>
            <li><a href="#">校友</a></li>
            <li><a href="#">关于我们</a></li>
            <li><a href="#">教师</a></li>
            <li><a href="#">用户登录</a></li>
        </ul>
    </div>
      
      
    </div>
</template>
<script>
import axiosApi from "@/api/public"
import store from '@/store/store.js'
export default{
    data() {
        return {
			// positionIndustry:[],
			// positionType:[],
        };
  },
    store,
    mounted(){
        // this.getPositionIndustry();
        // this.getPositionType();
      
        },
    methods:{
        // getPositionIndustry: function(){
		// 		//按行业查看职位
		// 		var _this = this;
		// 		axiosApi.axiosGet(
		// 			"/apis/api/getdata/naf/code/items/35/list"
		// 		).then((response) => {
		// 			if(response.data.errcode===1){
		// 				alert(response.data.errmsg);
		// 			}else{
		// 				_this.positionIndustry = response.data.data;
		// 			}
		// 		}),function(error){
		// 			$.alert('对不起，你的请求处理失败了!');   //失败处理
		// 		};
        // },
        // getPositionType: function(){
		// 		//按类别查看职位
		// 		var _this = this;
		// 		axiosApi.axiosGet(
		// 			"/apis/api/getdata/naf/code/items/36/list"
		// 		).then((response) => {
		// 			if(response.data.errcode===1){
		// 				alert(response.data.errmsg);
		// 			}else{
		// 				_this.positionType = response.data.data;
		// 			}
		// 		}),function(error){
		// 			$.alert('对不起，你的请求处理失败了!');   //失败处理
		// 		};
        // }
        
        }

    


}

</script>
<style scoped>

.toplogo{
	width: 1200px;
	height: 150px;
	margin: 0 auto;
}
.nav{
	height:40px;
	background-color: #00428c;
	width: 100%;
}
.nav ul{
	height: 40px;
	width: 1200px;
	margin: 0 auto;
	line-height: 40px;
}
.nav li{
	float: left;
}
.nav li:nth-child(1){
	background-color: #0057b4;
}
.nav li:nth-child(7){
	float: right;
}
.nav a{
	display: block;
	color: #fff;
	/*width: 100%;
	width: 100%;*/
	padding:0 30px;
}
.nav a:hover{
	background-color: #0057b4;
}
</style>
