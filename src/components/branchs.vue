<template>
  <div id="branchsit">
    <topnav></topnav>
    <router-view class="view"> </router-view>
  </div>
</template>

<script>
import store from '@/store/store.js'
import topnav from '@/components/branchsit/topnav'
export default{
  name:"branchsit",
  data () {
    return {
    }
  },
  store,
  components:{topnav},
 
}

</script>