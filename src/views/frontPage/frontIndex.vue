<template>
    <div>
        <div class="css-main-index">
				<div  style="padding-top:40px;"><!-- class="css-out-content" -->
					<div class="css-header"  style="font-size:16px;">
						<!-- <div class="container" style="padding-bottom:0;">
							<router-link to="/frontPage/frontIndex" title="惠安智慧就业平台"> 
								<img src="static/frontPage/imgs/a.jpg" class="css-logo pull-left" style="width:230px; height:40px;" >
								</router-link>
							<div class="css-subwebsite pull-left"  style="background: url('static/frontPage/imgs/enterr.png') no-repeat left 5px;">
								<router-link to="/frontPage/SchoolList"><b>进入子站</b><span class="text-primary">[切换分站]</span> </router-link>
							</div>
							<div class="css-right pull-right">
								<div class="css-search pull-right">
									<form id="search" action="">
										<ul class="css-list-inline pull-right css-hot">
											<li>欢迎您使用本网站</li>
										</ul>
										<ul class="css-list-inline pull-right">
											<li><input class="css-submit" value="" type="button"></li>
											<li>
												<input name="keyword"  type="text" placeholder="请输入查询关键词">
											</li>
										</ul>
									</form>
								</div>
							</div>
						</div> -->
						 <div class="vsech">
				<div class="sech">
					<form id="search" action="">
			        <img class="here" src="/static/frontPage/imgs/logo.jpg"><!-- SchoolList.html -->
			        <div class="child"><router-link to="/branchsit"><img src="/static/frontPage/imgs/here.jpg">&nbsp;进入子站&nbsp;<span>[切换分站]</span> </router-link></div>
			        <input type="text" name="keyword" class="inp" placeholder="请输入职位或公司"><input type="image" name="" class="btn" src="/static/frontPage/imgs/serach.jpg">
			        <div class="sou"><router-link to="#">程序员</router-link><router-link to="#">高薪名企</router-link><router-link to="#">收银员</router-link></div>
			    	</form>
			    </div>
			  </div> 
					</div>
				</div>
				<div class="css-nav">
						<div class="container">
							<div class="pull-left css-usernav">
								<span onmouseover="seen()" onmouseout="disn()">用户功能频道</span>
							</div>
							<ul class="pull-left css-navbar">
								<li><router-link to="/frontPage/secleve">平台首页</router-link></li>
								<li><router-link to="/frontPage/StudentLogin">学生用户</router-link></li>
								<li><router-link to="#">学习平台</router-link></li>
								<li><router-link to="#">高校分站点</router-link></li>
								<!-- <li><router-link to="#">吉林.长春</router-link></li> -->
							</ul>
						</div>  
				</div>
					<div class="container clearfix">
						<div class="css-channel pull-left">
							<div class="css-menu" id="css-menu">
								<div onmouseover="lul_list()" onmouseout="lul_out()" class="cr_li">
									<router-link to="/" class="li_a">平台首页</router-link>
									<!-- <router-link to="index.html" class="li_a">平台首页 </router-link> -->
									<div class="box1" id="box1">
										<div class="list-left">
											<ul  class="lt-ul">
												<li><router-link to="/frontPage/recruitment">岗位信息</router-link></li>
												<li><router-link to="/frontPage/campusTalkPage">校园宣讲会</router-link></li>
												<li><router-link to="/frontPage/campusRecruitmentPage">校园招聘公告</router-link></li>
											</ul>
										</div>
										<div class="list-con">
											<ul class="cn-ul">
												<p class="txt">按行业查看职位</p>
												 <div v-for="pitem in positionIndustry">
												 <li><router-link to="#this" @click="find(pitem)">{{pitem.name}}</router-link></li>
												 </div>
											</ul>
										</div>   
										<div class="list-bg"></div>
										<div class="list-right">
											<ul class="cn-ul">
												<p class="txt">按类别查看职位</p>
												<div v-for="ptyim in positionType">
												<li><router-link to="#this" @click="find(ptyim)">{{ptyim.name}}</router-link></li>
												</div>
											</ul>
										</div> 
									</div>
								</div>
								<div onmouseover="lul_list1()" onmouseout="lul_out1()" class="cr_li stubg">
									<router-link to="/" class="li_a">学生服务</router-link>
									<div class="box1" id="box2">
										<div class="css-subMenu">
											<div class="top-M">就业信息</div>
											<ul class="Mul">
												<li><router-link to="/frontPage/recruitment">岗位信息</router-link></li>
												<li><router-link to="/frontPage/campusTalkPage">校园宣讲会</router-link></li>
												<li><router-link to="/frontPage/campusRecruitmentPage">校园招聘公告</router-link></li>
											</ul>
										</div>

										<div class="css-subMenu">
											<div class="top-M">职业辅导</div>
											<ul class="Mul">
												<li><router-link to="/frontPage/guidance">政策法规</router-link></li>
												<li><router-link to="/frontPage/guidance">就业心得</router-link></li>
												<li><router-link to="/frontPage/guidance">辅导活动</router-link></li>
												<li><router-link to="/frontPage/guidance">职业课程</router-link></li>
												<li><router-link to="/frontPage/guidance">专家咨询</router-link></li>
											</ul>
										</div>
										<div class="css-subMenu">
											<div class="top-M">就业服务</div>
											<ul class="Mul">
												<li><router-link to="/frontPage/StudentLogin">学历学位认证</router-link></li>
												<li><router-link to="/frontPage/StudentLogin">电子图像校对</router-link></li>
												<li><router-link to="/frontPage/StudentLogin">报到证查询</router-link></li>
											</ul>
										</div>

										<div class="css-subMenu">
											<div class="top-M">用户中心</div>
											<ul class="Mul">
												<li><router-link to="/frontPage/StudentLogin">推荐表注册</router-link></li>
												<li><router-link to="/frontPage/StudentLogin">简历管理</router-link></li>
												<li><router-link to="/frontPage/StudentLogin">职位收藏夹</router-link></li>
												<li><router-link to="/frontPage/StudentLogin">职位申请记录</router-link></li>
												<li><router-link to="/frontPage/StudentLogin">我的日程表</router-link></li>
												<li><router-link to="/frontPage/StudentLogin">账号设置</router-link></li>
											</ul>
										</div>
									</div>
								</div>
								<div onmouseover="lul_list2()" onmouseout="lul_out2()" class="cr_li danwbg">
									<router-link class="li_a" to="/">单位服务</router-link>
									<div class="box1" id="box3">
										<div class="css-subMenu">
											<div class="top-M">基础服务</div>
											<ul class="Mul">
												<li><router-link to="/frontPage/UnitReg">单位注册</router-link></li>
												<li><router-link to="/frontPage/UnitReg">职位发布</router-link></li>
											</ul>
										</div>
										<div class="css-subMenu">
											<div class="top-M">充值服务</div>
											<ul class="Mul">
												<li><router-link to="/frontPage/unitLogin">广告申请</router-link></li>
												<li><router-link to="/frontPage/unitLogin">职位置顶</router-link></li>
												<li><router-link to="/frontPage/unitLogin">定向发布</router-link></li>
												<li><router-link to="/frontPage/unitLogin">下载简历</router-link></li>
												<li><router-link to="/frontPage/unitLogin">职位邀请</router-link></li>
											</ul>
										</div>
										<div class="css-subMenu">
											<div class="top-M">会员服务</div>
											<ul class="Mul">
												<li><router-link to="/frontPage/unitLogin">充值服务所有内容</router-link></li>
												<li><router-link to="/frontPage/unitLogin">校园统一认证</router-link></li>
												<li><router-link to="/frontPage/unitLogin">生源专业查询</router-link></li>
												<li><router-link to="/frontPage/unitLogin">招聘会展位优选</router-link></li>
												<li><router-link to="/frontPage/unitLogin">专属在线客服</router-link></li>
											</ul>
										</div>
									</div>
								</div>
								<div  onmouseover="lul_list3()" onmouseout="lul_out3()" class="cr_li schoolbg">
									<router-link class="li_a" to="/">学校服务</router-link>
									<div class="box1" id="box4">
										<div class="css-subMenu">
											<div class="top-M">就业管理</div>
											<ul class="Mul">
												<li><router-link to="/frontPage/disLogin">推荐表审核</router-link></li>
												<li><router-link to="/frontPage/disLogin">协议书审核</router-link></li>
												<li><router-link to="/frontPage/disLogin">电子图像校对</router-link></li>
											</ul>
										</div>

										<div class="css-subMenu">
											<div class="top-M">常用链接</div>
											<ul class="Mul">
												<li><router-link to="http://www.baidu.com/">长春毕业生就业网</router-link></li>
											</ul>
										</div>
									</div>
								</div>
								<div class="cr_li schoolLbg">
									<!-- <router-link to="SchoolList.html" class="li_a">高校分站点</router-link> -->
									<router-link class="li_a" to="/frontPage/SchoolList">高校分站点</router-link>
								</div>
							</div>
						</div>
						<div class="css-slide">
							<div class="xmK mb50">
								<div class="lB" id="lB">
									<div v-for="carim in carouselFigure">
										<router-link :to="carim.url"  class="aimg" onmouseover="ba_move()" onmouseout="ba_out()" style="display: block;">
											<img v-bind:src ="carim.name"/>
										</router-link>
									</div>
									<div class="dian_ul1">
										<div class="Txin" style="float: left;">
											<ul class="Tul" id="Tul">
												<div v-for="poim in photoAnnotate">
													<li style="display: block;">{{poim.name}}</li>
												</div>
											</ul>
										</div>
									</div>
									<ul class="dian_ul"  id="dian_ul">
										<li onmousemove="dian_list(0)" onmouseout="ba_out()" class="dian_li_bg"></li>
										<li onmousemove="dian_list(1)" onmouseout="ba_out()"></li>
										<li onmousemove="dian_list(2)" onmouseout="ba_out()"></li>
										<li onmousemove="dian_list(3)" onmouseout="ba_out()"></li>
										<li onmousemove="dian_list(4)" onmouseout="ba_out()"></li>
									</ul>
								</div>
							</div>
						</div>
						<div class="login">
				            <div class="hi">
				                <p>Hi，你好~<br/>找工作？招人才...</p>            
				                <div class="dl"><router-link to="/frontPage/disLogin">用户登录</router-link></div>
				                <div class="zc"><router-link to="/frontPage/distRegist">免费注册</router-link></div>
				            </div>
				            <div class="notice">
				                <h2><router-link to="notice.html">公告<span></span><span></span><span></span></router-link></h2>
				                <ul style="font-size:16px;">
									<div v-for="notice in noticeList">
										<li><router-link to="#this" @click="findthe(notice)">{{notice.name}}</router-link></li>										
									<!-- *5
										<li><router-link to="#this">江苏省2018届高校毕业生百校联动计划2017年下半年重点场次安排</router-link></li>
										 -->
									</div>
								</ul>
				                <!-- <ul>
				                    <li><router-link to="">尼日利亚传统领袖：卡诺埃米尔萨努西二世和尼日利亚驻沪总领事阿里·欧切尼</li></router-link>
				                </ul> -->
				            </div>
				        </div>
						<div class="clearfix"></div>
						<!-- <div class="css-imggroup">
							<ul>
								<div v-for="advers in advertisingPosition">
								<li>
									<a @click="findadv(advers)" target="_blank">
										<img :src ="advers.img" :title="advers.titles"></router-link>
								</li>
								</div>
							</ul>
						</div> -->
						<div class="css-imgline" style="background: red;">
							<router-link to="noticePage.html" target="_blank"><img src="static/frontPage/imgs/banner002.jpg" alt="大图片"></router-link>
						</div>
						<div class="clearfix"></div>
						<div class="css-jobfair pull-left">
							<div class="tab">
				                <ul class="title" id="title">
				                    <li > <router-link to="/frontPage/secleve">job招聘会</router-link></li>
				                    <li><router-link to="/frontPage/secleve">百校联动招聘会</router-link></li>
				                    <li><router-link to="/frontPage/secleve">校园宣讲会</router-link></li>
				                    <li><router-link to="/frontPage/secleve">校园招聘公告</router-link></li>
				                </ul>
								<!-- <ul class="tabs clearfix">
									<li v-for="(tab,index) in tabsName">
										<a v-bind:href="tab.url" class="tab-link" @mouseover="tabsSwitch(index)" v-bind:class="{active:tab.isActive}">{{tab.name}}</router-link>
									</li>
									<div style="float: left; height: 48px; line-height: 48px; width:80px; margin-left: 150px;  "><router-link to="/frontPage/campusTalkPage"> MORE>></router-link></div>
								</ul> -->
				                <!-- <ul class="tabs clearfix">
									<li v-for="(tab,index) in tabsName">
										<a v-bind:href="tab.url" class="tab-link" @mouseover="tabsSwitch(index)" v-bind:class="{active:tab.isActive}">{{tab.name}}</router-link>
									</li>
									<div style="float: left; height: 48px; line-height: 48px; width:80px; margin-left: 150px;  "><router-link to="campusTalkPage.html"> MORE>> </router-link></div>
								</ul> -->
				                <div class="content">
				                    <div class="contentlist">
				                        <ul>
				                            <div v-for="ctim in campusPreachlist"><!-- 校园宣讲会 -->
												<li><router-link to="#this" @click="findly(ctim)">{{ctim.subject}}</router-link>
													<span>{{ctim.meta.createdAt}}</span>
												</li>
											</div>
				                            <!-- <li><router-link to="">尼日利亚传统领袖：尼应学习借鉴中国自贸区建设经验</router-link><span>2017-08-06</span></li>
				                            <li><router-link to="">2018年江苏省大学生村官自主择业专场供需洽谈会</router-link><span>2017-08-06</span></li>                       
				                            <li><router-link to="">江苏省2018年智能装备制造业暨常州机电职业技术学院</router-link><span>2017-08-06</span></li>
				                        </ul>
				                    </div>
				                    <div class="contentlist">
				                        <ul>
				                        	<div v-for="dtim in campusRecruitlist">
												<li><router-link to="#this" @click="find(dtim)"> 校园宣招聘公告 
													{{dtim.subject}}</router-link>
													<span>{{dtim.meta.createdAt}}</span>
												</li>
											</div>
				                            <!-- <li><router-link to="">关于邀请参加宁波市第二十届高层次人才智力引进洽谈会的函</router-link><span>2017-08-06</span></li>
				                            <li><router-link to="">2018年江苏省大学生村官自主择业专场供需洽谈会</router-link><span>2017-08-06</span></li>                       
				                            <li><router-link to="">工业和信息化部人才交流中心 （2018年度）全国秋季巡回招聘</router-link><span>2017-08-06</span></li>
				                            <li><router-link to="">江苏省大学生村官自主择业专场供需洽谈会</router-link><span>2017-08-06</span></li>                       
				                            <li><router-link to="">江苏省2018年智能装备制造业暨常州机电职业技术学院</router-link><span>2017-08-06</span></li> -->
				                        </ul>
				                    </div>
				                    <div class="contentlist">
				                        <ul>
				                            <!-- <li><router-link to="">3尼日利亚传统领袖：尼应学习借鉴中国自贸区建设经验</router-link><span>2017-08-06</span></li> -->
											<div v-for="ctim in campusPreachlist">
												<li><router-link to="#this" @click="findly(ctim)">{{ctim.subject}}</router-link>
													<!-- <span class="css-col200">{{ctim.corp.name}}</span> -->
													<span>{{ctim.meta.createdAt}}</span>
												</li>
											</div>
				                        </ul>
				                    </div>
				                    <div class="contentlist">
				                        <ul>
				                            <li><router-link to="">4尼日利亚传统领袖：尼应学习借鉴中国自贸区建设经验</router-link><span>2017-08-06</span></li>
				                        </ul>
				                    </div>
				                </div>
				            </div>
							<!-- <div class="box">
								<ul class="tabs clearfix">
									<li v-for="(tab,index) in tabsName">
										<a v-bind:href="tab.url" class="tab-link" @mouseover="tabsSwitch(index)" v-bind:class="{active:tab.isActive}">{{tab.name}}</router-link>
									</li>
									<div style="float: left; height: 48px; line-height: 48px; width:80px; margin-left: 150px;  "><router-link to="/frontPage/campusTalkPage"> MORE>></router-link></div>
								</ul>

								<div class="cards">
									<div class="tab-card" style="display: block;" >
										<ul class="ulC">
											<div v-for="ctim in campusPreachlist">校园宣讲会
												<li><router-link to="#this" @click="findly(ctim)">
													<span class="css-col400">{{ctim.subject}}</span>
													<span class="css-col200">{{ctim.corp.name}}</span>
													<span class="tim">{{ctim.meta.createdAt}}</span>
												</router-link></li>
											</div>
										</ul>
									</div>
									<div class="tab-card">
										<ul class="ulC">
											<div v-for="dtim in campusRecruitlist">
												<li><router-link to="#this" @click="find(dtim)"> 校园宣招聘公告 
													<span class="css-col400">{{dtim.subject}}</span>
													<span class="css-col200">{{dtim.tenant}}</span>
													<span class="tim">{{dtim.meta.createdAt}}</span>
												</router-link></li>
											</div>
										</ul>
									</div>
								</div>
							</div> -->
						</div>
						<div class="css-calendar pull-right" style="position: relative;">
							<!--<div style="width: 387px; height: 400px; background: #bfe9e7; position: relative; margin: 0 auto; margin-top: 100px;" >-->
								<div class="css-caption1" style="width:347px; height:50px; background: #2577e3 url('static/frontPage/imgs/date.png') no-repeat 10px 13px;; color: #ffffff; padding-left: 40px; font-size: 18px; line-height: 51px;">
									就业日历
								</div>
								<!-- <div id='schedule-box'  class="boxshaw" >
									
								</div> -->
								
								<div class="calendarb">
								<calendarb></calendarb></div>
								<div class="css-job" id="css-job">
									<div class="job-top">
										<div class="top-left" id='h3Ele'>
											<!--2017-03-01-->
										</div>
										<div onclick="jobclose()" class="top-right">
											X
										</div>
									</div>
									<div class="job-box">
											<p><router-link to="/frontPage/campusTalkPage">校园宣讲会：<span style="color:#00B8EC ">1场</span></router-link></p>

									</div>
								</div>
							</div>
						<!--</div>-->
						<div class="clearfix"></div>
						<!-- 拒绝诈骗-->
						<div class="css-imgline" style="margin-top: 0;">
							<img src="static/frontPage/imgs/banner003.jpg" alt="拒绝诈骗图片" style="margin-top: 0;">
						</div>
						<div class="clearfix"></div>
						<div class="css-hotjob">
							<div class="css-caption">
								<div><router-link to="" target="_blank" style="color:#fff;"><img src="static/frontPage/imgs/newjob.jpg">最新职位</router-link></div>
								
							</div>
							<div class="css-content">
								<div class="css-ujobs clearfix">
									<div v-for="jobs in newJobs">
										<div v-if="(jobs.vip=='1')">
										<ul>
											<li>
												{{jobs.company}}
												<img src="static/frontPage/imgs/vip.gif" title="VIP">
											</li>
											<li>
												<router-link to="recruitmentDetailPage.html"  target="_blank" class="text-blue">{{jobs.position}}</router-link>
												<router-link to="recruitmentDetailPage.html"  target="_blank" class="text-blue">{{jobs.position2}}</router-link>
												<router-link to="recruitmentDetailPage.html" target="_blank" class="text-blue">{{jobs.position3}}</router-link>
											</li>
										</ul>
										</div>
									</div>
									
								</div>
								<div class="css-njobs">
								<div v-for="jobs in newJobs">
									<div v-if="(jobs.vip=='0')">
									<ul>
										<li>{{jobs.company}}</li>
										<li>
											<router-link to="recruitmentDetailPage.html" target="_blank" class="text-blue">{{jobs.position}}</router-link>
											<router-link to="recruitmentDetailPage.html" target="_blank" class="text-blue">{{jobs.position2}}</router-link>
											<router-link to="recruitmentDetailPage.html" target="_blank" class="text-blue">{{jobs.position3}}</router-link>
										</li>
									</ul>
									</div>
								</div>
									
								</div>
							</div>
						</div>
						<div class="clearfix"></div>
						<!-- <div class="css-corphire">
							<div class="css-caption">
								<div><img src="static/frontPage/imgs/vvip.png">高级会员</div>
								<span><router-link to="seniorMemberPage.html" class="css-more">MORE&nbsp;&gt;&gt;</router-link></span>
							</div>
							<div id="marquee5">
								<div style="height: 10000px;">
									<ul class="css-logos">
										<li v-for="senior in menber">
											<a :href="['companyDetailPage.html?id='+senior.id]" target="_blank">
												<img v-bind:src="senior.img" v-bind:title="senior.name">
												<p>{{senior.name}}</p>
											</router-link>
										</li>
										

									</ul>
								</div>

							</div>
						</div> -->
						<div class="css-talentmarket">
							<div class="css-caption">
								<div><router-link to="recruitmentBrochurePage.html" target="_blank" style="color:#fff;">
									<img src="static/frontPage/imgs/les_06.jpg">
									招聘简章</router-link>
								</div>
							</div>
							<div class="css-content">
								<ul class="cc">
								
									<li v-for="recruit in recruitmentBrochure">
										<a :href="['recruitmentBrochureDetailPage.html?id='+recruit.id]">
											{{recruit.title}}
										</a>
										<time>{{recruit.time}}</time>
									</li>
									
									
								</ul>
							</div>
						</div>
						<div class="clearfix"></div>
						<div class="css-friendlink" style="margin: 20px 0;padding-bottom:10px;">
							<div class="css-caption">
								<div>
									<img src="static/frontPage/imgs/link.png"> 
									友情链接
								</div>
							</div>

							<ul class="link">
								<li><router-link to="http://www.ccedin.net/index.shtml">吉林长春教育局</router-link></li>
								<li><router-link to="http://www.chsi.com.cn/xlrz/201202/20120228/284926187.html">长春市就业服务中心</router-link></li>
							</ul>
						</div>
						<div class="clearfix"></div>
					</div>
				</div>
	</div>

</template>
<script>
import axiosApi from "@/api/public"
import calendarb from '@/components/calendar/calendarb.vue'

export default{
    data() {
        return {
            tabsName: [{
				name: "校园宣讲会",
				url:"/frontPage/campusTalkPage",
				isActive: true
			}, {
				name: "校园招聘公告",
				url:"/frontPage/campusRecruitmentPage",
				isActive: false
			}],
            active: false,
			noticeList:[],
			campusPreachlist:[],
			campusRecruitlist:[],
			carouselFigure:[],
			photoAnnotate:[],
			positionIndustry:[],
			positionType:[],
			advertisingPosition:[],
			menber:[],
			recruitmentBrochure:[],
			newJobs:[]//最新职位
        };
  },
    components:{
        calendarb
    },
  mounted(){
    this.getFiveNotice();
    this.getCampusPreaching();
    this.getCampusRecruitment();
    this.getCarouselFigure();
    this.getPhotoAnnotate();
    this.getPositionIndustry();
    this.getPositionType();
    this.getAdvertisingPosition();
    this.getMenber();
    this.getRecruitmentBrochure();
    this.getNewJobs();
	},
  methods:{
        getPositionIndustry: function(){
				//按行业查看职位
				var _this = this;
				axiosApi.axiosGet(
					"/apis/naf/code/items/35/list"
				).then((response) => {
					if(response.data.errcode===1){
						alert(response.data.errmsg);
					}else{
						_this.positionIndustry = response.data.data;
					}
				}),function(error){
					$.alert('对不起，你的请求处理失败了!');   //失败处理
				};
        },
        getPositionType: function(){
				//按类别查看职位
				var _this = this;
				axiosApi.axiosGet(
					"/apis/api/getdata/naf/code/items/36/list"
				).then((response) => {
					if(response.data.errcode===1){
						alert(response.data.errmsg);
					}else{
						_this.positionType = response.data.data;
					}
				}),function(error){
					$.alert('对不起，你的请求处理失败了!');   //失败处理
				};
        },
        getCampusPreaching: function(){
				//校园宣讲会
				var _this = this;
				axiosApi.axiosGet(
					"/apis/jobs/campus/simple?skip=0&limit=10"
				).then((response) => {
					if(response.data.errcode===1){
						alert(response.data.errmsg);
					}else{
						_this.campusPreachlist = response.data.data;
					}
				}),function(error){
					$.alert('对不起，你的请求处理失败了!');   //失败处理
				};
        },
        getCampusRecruitment: function(){
            //校园招聘公告
            var _this = this;
            axiosApi.axiosGet(
                "/apis/jobs/jobfair/simple?skip=0&limit=10"
            ).then((response) => {
                if(response.data.errcode===1){
                    alert(response.data.errmsg);
                }else{
                    _this.campusRecruitlist = response.data.data;
                }
            }),function(error){
                $.alert('对不起，你的请求处理失败了!');   //失败处理
            };
        },
        tabsSwitch: function(tabIndex) {

            var tabCardCollection = document.querySelectorAll(".tab-card"),
                    len = tabCardCollection.length;

            for(var i = 0; i < len; i++) {
                tabCardCollection[i].style.display = "none";
                this.tabsName[i].isActive = false;
            }
            this.tabsName[tabIndex].isActive = true;
            tabCardCollection[tabIndex].style.display = "block";
        },
        getFiveNotice: function(){
				//右上角五条公告
				var _this = this;
				axiosApi.axiosGet(
					"static/frontPage/json/fiveNotice.json"
				).then((response) => {
					if(response.data.errcode===1){
						alert(response.data.errmsg);
					}else{
						_this.noticeList = response.data.list;
					}
				}),function(error){
					$.alert('对不起，你的请求处理失败了!');   //失败处理
				};
			},
		findthe: function(notice){
				//
				location.href="noticePage.html?id="+notice.id;
        },
		getCarouselFigure: function(){
				//轮播图
				var _this = this;
				axiosApi.axiosGet(
					"static/frontPage/json/homeCarouselFigure.json"
				).then((response) => {
					if(response.data.errcode===1){
						alert(response.data.errmsg);
					}else{
						_this.carouselFigure = response.data.list;
					}
				}),function(error){
					$.alert('对不起，你的请求处理失败了!');   //失败处理
				};
		},	
		getPhotoAnnotate: function(){
				//轮播图注释
				var _this = this;
				axiosApi.axiosGet(
					"static/frontPage/json/photoAnnotate.json"
				).then((response) => {
					if(response.data.errcode===1){
						alert(response.data.errmsg);
					}else{
						_this.photoAnnotate = response.data.list;
					}
				}),function(error){
					$.alert('对不起，你的请求处理失败了!');   //失败处理
				};
		},
		getAdvertisingPosition: function(){
				//广告
				var _this = this;
				axiosApi.axiosGet(
					"static/frontPage/json/advertisingPosition.json"
				).then((response) => {
					if(response.data.errcode===1){
						alert(response.data.errmsg);
					}else{
						_this.advertisingPosition = response.data.list;
					}
				}),function(error){
					$.alert('对不起，你的请求处理失败了!');   //失败处理
				};
		},
		findadv: function(advers){
				//
				location.href="companyDetailPage.html?id="+advers.id;
		},
		getMenber: function(){
			//高级会员
			var _this = this;
			axiosApi.axiosGet(
				"static/frontPage/json/menber.json"
			).then((response) => {
				if(response.data.errcode===1){
					alert(response.data.errmsg);
				}else{
					_this.menber = response.data.list;
				}
			}),function(error){
				$.alert('对不起，你的请求处理失败了!');   //失败处理
			};
		},
		getRecruitmentBrochure: function(){
				//招聘简章
				var _this = this;
				axiosApi.axiosGet(
					"static/frontPage/json/recruitmentBrochure.json"
				).then((response) => {
					if(response.data.errcode===1){
						alert(response.data.errmsg);
					}else{
						_this.recruitmentBrochure = response.data.list;
					}
				}),function(error){
					$.alert('对不起，你的请求处理失败了!');   //失败处理
				};
		},
		getNewJobs: function(){
			//最新职位
			var _this = this;
			axiosApi.axiosGet(
				"static/frontPage/json/newJobs.json"
			).then((response) => {
				if(response.data.errcode===1){
					alert(response.data.errmsg);
				}else{
					_this.newJobs = response.data.list;
				}
			}),function(error){
				$.alert('对不起，你的请求处理失败了!');   //失败处理
			};
		},
		find: function(pitem){
			//按行业查看职业
			var _this =this;
                _this.$router.push({
                    path:'/frontPage/recruitment',
                    query: {
                     "_id": pitem._id
                        }
                })
			//location.href="recruitment.html?id="+pitem.id;
		},
		find: function(ptyim){
			//按行业查看职业
			var _this =this;
                _this.$router.push({
                    path:'/frontPage/recruitment',
                    query: {
                     "_id": ptyim._id
                        }
                })
			//location.href="recruitment.html?id="+ptyim.id;
		},
		findly: function(ctim){
			//跳转宣讲会详情
			var _this =this;
                _this.$router.push({
                    path:'/frontPage/companyDetailPage',
                    query: {
                     "_id": ctim._id
                        }
                })
			
			//location.href="companyDetailPage?id="+ctim._id;
		},
		find: function(dtim){
			//跳转校园招聘公告详情
			var _this =this;
                _this.$router.push({
                    path:'/frontPage/companyPage',
                    query: {
                     "_id": dtim._id
                        }
                })
			//location.href="companyPage.html?id="+dtim._id;
		}
  }
}
//   var mySchedule = new Schedule({
  		// el: '#schedule-box',
//  		//date: '2018-9-20',
//  		clickCb: function (y,m,d) {
// 			document.querySelector('#h3Ele').innerHTML =y+'-'+m+'-'+d
// 		},
// 		nextMonthCb: function (y,m,d) {
//  			document.querySelector('#h3Ele').innerHTML =y+'-'+m+'-'+d
//  		},
//  		nextYeayCb: function (y,m,d) {
//  			document.querySelector('#h3Ele').innerHTML =y+'-'+m+'-'+d
//  		},
//  		prevMonthCb: function (y,m,d) {
//  			document.querySelector('#h3Ele').innerHTML =y+'-'+m+'-'+d
//  		},
//  		prevYearCb: function (y,m,d) {
//  			document.querySelector('#h3Ele').innerHTML =y+'-'+m+'-'+d
//  		}
  	// });

 	function job(day){
 		/*var str = this.formatDate(this.currentYear , this.currentMonth, this.currentDay);*/
 		var cssjob=document.getElementById("css-job");
 		cssjob.style.display="block";
 	}
 	function jobclose(){
 		var cssjob=document.getElementById("css-job");
 		cssjob.style.display="none";
 	}
	    $(function(){
        //tab选项卡点击
        //$(".title li").click(function(){  标题点击
            //var index=$(this).index();  获得当前点击标题的下标
            //$(this).addClass("active").siblings().removeClass("active"); 给当前选项添加选中，其他移除选中
           // $(".content .contentlist").eq(index).show().siblings().hide();  对应下标的内容框显示，其他隐藏
        //});
        //tab选项卡悬停
        /* $(".title ul li").eq(0).addClass("active"); */
        $("#title ul li").first().addClass("active");
        $(".title li").hover(function(){  ////标题悬停
            var index=$(this).index();  //获得当前点击标题的下标
            $(this).addClass("active").siblings().removeClass("active"); //给当前选项添加选中，其他移除选中
            $(".content .contentlist").eq(index).show().siblings().hide();  //对应下标的内容框显示，其他隐藏
        });
    })

</script>


<style>
@import "../../../static/frontPage/css/index2.css";
	body {font-size: 16px;}

#frontIndex{
    background:blueviolet;
    width:800px;
    height:800px;
}


			/*校园宣讲会*/

			.box {
				/* width: 800px;*/
				height: 403px;
				background: #ffffff;
				/* margin: 0 auto;*/
				/*border: 1px solid #000;*/
			}

			.tabs li {
				float: left;
				margin-right: 8px;
				list-style: none;
			}

			.tabs .tab-link {
				display: block;
				width: 250px;
				height: 49px;
				text-align: center;
				line-height: 49px;
				background-color: #00B8EC;
				color: #fff;
				text-decoration: none;
			}

			.tabs .tab-link.active {
				height: 47px;
				border-bottom: 2px solid #E35885;
				transition: .3s;
			}

			.cards {
				float: left;
			}

			.cards .tab-card {
				display: none;
			}

			.clearfix:after {
				content: "";
				display: block;
				height: 0;
				clear: both;
			}

			.clearfix {
				zoom: 1;
			}
			.css-nav{
				width:100%;
			}
		</style>

	