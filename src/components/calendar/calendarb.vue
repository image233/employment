<template>
  <div class="hi">
    <Calendar v-on:choseDay="clickDay" v-on:changeMonth="changeDate" v-on:isToday="clickToday" >
    </Calendar>
  </div>
</template>
<script>
import Calendar from 'vue-calendar-component';
export default {
  data () {
        return {
        msg: '日历~~~'
        }
    },
    components: {
        Calendar
    },
    methods: {
        clickDay(data) {
            console.log('选中了', data) //选中某一日
            // this.$toast('选中了' + data) //弹框组件toast
        },
        clickToday(data) {
            console.log('跳到本月', data) //跳到本月
        },
        changeDate(data) {
            // this.$toast('切换到的月份为' + data)
            console.log('左右点击切换月份', data) //左右点击切换月份
        },
        //demo() {
            // this.$refs.Calendar.ChoseMonth('2017-12-12',false); //跳到12月12日 但是不选中12月12日
            // this.$refs.Calendar.ChoseMonth('2017-12-12'); //例：跳到12月12日
        //}
    },
    created() {
        function format(date, index) {
            date = new Date(date);
            return `${date.getFullYear()}/${date.getMonth() + 1}/${index}`;
        }
        // this.arr = [{//选中多个日期
        //     date: format(new Date(), 1),
        //     className: "mark2"//选中日期圈圈颜色
        // }, {
        //     date: format(new Date(), 2),
        //     className: "mark2"
        // }, {
        //     date: format(new Date(), 13),
        //     className: "mark2"
        // }]
    }
}
</script>

<style >
.wh_content_item div .wh_isToday{
    background-color: #409EFF;
    color: #c8e0d7;
}
.wh_top_changge li{
    color: #409EFF;
}
.wh_jiantou1{
    color: #409EFF;
        width: 12px;
    height: 12px;
    border-top: 2px solid #409EFF;
    border-left: 2px solid #409EFF;
    -webkit-transform: rotate(-45deg);
    transform: rotate(-45deg)
}
.wh_jiantou2{
    color: #409EFF;
        width: 12px;
    height: 12px;
    border-bottom: 2px solid #409EFF;
    border-right: 2px solid #409EFF;
    -webkit-transform: rotate(-45deg);
    transform: rotate(-45deg)
}
.wh_content_all{
    background-color: #ffffff;
    /* height:240px; */
}
.wh_content_item{
    
    color: #616161;
}
.wh_content_item li{
    height:30px;
    width: 30px;
    line-height:30px;
}
h3 {
    text-align: center;
    width: 90%;
    margin: auto;
}
.div {
    margin: auto;
    width: 220px;
    height: 44px;
    line-height: 44px;
    background: #0fc37c ;
    color: #fff;
    font-size: 17px;
    text-align: center;
    margin-top: 20px;
}
.mark1 {
    background-color: red;
}
.mark2 {
    background-color: blue;
}
</style>
