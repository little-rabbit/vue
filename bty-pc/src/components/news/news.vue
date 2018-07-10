<template>
  <div class="news">
    <div class="tops top6">
        <ul class="tab">
          <li  v-for='(item,index) in datas' :key=index @click='selected(index)' :class="{active:index==num}">
            {{item.title}}
          </li>
        </ul>
    </div> 
    <div class="location">
        当前所在位置>
        <a href="">首页</a>>
        <a href="">新闻中心</a>>
        <a href="">{{datas[num].title}}</a>
    </div>
    <div class="center" v-for='(item,index) in datas' :key=index v-if='index==num'>
        <div class="text" v-for='(item_produce,index) in item.produce' :key=index>
          <p class='img'>
            <img :src='item_produce.img' alt="">
          </p>
           <h3>{{item_produce.text1}}</h3>
           <p style='margin-left:5px'>{{item_produce.text2}}</p>
        </div>
        
    </div>
  </div>
</template>

<script>
export default {
  name: 'News',
  data () {
    return {
      datas:[
        {title:"政策新闻",
         produce:[
          {
            text1:'国内装配式建筑的疑惑和解决',
            text2:'近年来，政府越来越重视装配式建筑发展。装配式建筑有着环保、便捷、安...',
            img:require('../../assets/image/news1_1.jpg')
          },
          {
           text1:'国内装配式建筑的疑惑和解决',
            text2:'近年来，政府越来越重视装配式建筑发展。装配式建筑有着环保、便捷、安...',
            img:require('../../assets/image/news1_1.jpg')
          },
          {
           text1:'国内装配式建筑的疑惑和解决',
            text2:'近年来，政府越来越重视装配式建筑发展。装配式建筑有着环保、便捷、安...',
            img:require('../../assets/image/news1_1.jpg')
          },
          {
           text1:'国内装配式建筑的疑惑和解决',
            text2:'近年来，政府越来越重视装配式建筑发展。装配式建筑有着环保、便捷、安...',
            img:require('../../assets/image/news1_1.jpg')
          },
          {
           text1:'国内装配式建筑的疑惑和解决',
            text2:'近年来，政府越来越重视装配式建筑发展。装配式建筑有着环保、便捷、安...',
            img:require('../../assets/image/news1_1.jpg')
          },
          {
           text1:'国内装配式建筑的疑惑和解决',
            text2:'近年来，政府越来越重视装配式建筑发展。装配式建筑有着环保、便捷、安...',
            img:require('../../assets/image/news1_1.jpg')
          }
         ]
         },
        {title:"企业动态",
         produce:[
          {
           text1:'国内装配式建筑的疑惑和解决',
            text2:'近年来，政府越来越重视装配式建筑发展。装配式建筑有着环保、便捷、安...',
            img:require('../../assets/image/news2_1.jpg')
          },
          {
           text1:'国内装配式建筑的疑惑和解决',
            text2:'近年来，政府越来越重视装配式建筑发展。装配式建筑有着环保、便捷、安...',
            img:require('../../assets/image/news3_1.jpg')
          },
          {
           text1:'国内装配式建筑的疑惑和解决',
            text2:'近年来，政府越来越重视装配式建筑发展。装配式建筑有着环保、便捷、安...',
            img:require('../../assets/image/news3_1.jpg')
          },
          {
           text1:'国内装配式建筑的疑惑和解决',
            text2:'近年来，政府越来越重视装配式建筑发展。装配式建筑有着环保、便捷、安...',
            img:require('../../assets/image/news3_1.jpg')
          },
          {
           text1:'国内装配式建筑的疑惑和解决',
            text2:'近年来，政府越来越重视装配式建筑发展。装配式建筑有着环保、便捷、安...',
            img:require('../../assets/image/news3_1.jpg')
          },
          {
           text1:'国内装配式建筑的疑惑和解决',
            text2:'近年来，政府越来越重视装配式建筑发展。装配式建筑有着环保、便捷、安...',
            img:require('../../assets/image/news3_1.jpg')
          }
         ]
        },
        {title:"企业视频",
         produce:[
          {
           text1:'国内装配式建筑的疑惑和解决',
            text2:'近年来，政府越来越重视装配式建筑发展。装配式建筑有着环保、便捷、安...',
            img:require('../../assets/image/news3_1.jpg')
          }
         ]
        }
        
      ],
      num:0
    }
  },
  methods:{
    selected(index){
      this.num=index;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>