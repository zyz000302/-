<template>
  <div >
    <i-grid>
    <i-grid-item v-for="grid in grids" :key="grid" i-class="no-border">
        <i-grid-icon>
            <image :src="grid.image" />
        </i-grid-icon>
        <i-grid-label>{{grid.title}}</i-grid-label>
    </i-grid-item> 
</i-grid>
<i-panel :title="title_name">
    <view style="padding: 15px;">
    <i-card v-for="item in top" :key="item" i-class="split" :extra="item.name" :thumb="item.image">
    <view slot="content">{{item.remark}}</view>
    <view slot="footer">{{item.address}}</view>
</i-card>
</view>
</i-panel>
  </div>
</template>

<script>

export default {
  data () {
    return {
      title_name:"热门景点",
      grids: [
        {title="酒店",image:"/static/images/1.png"},
         {title="机票",image:"/static/images/2.png"},
          {title="火车票",image:"/static/images/3.png"},
           {title="汽车票",image:"/static/images/4.png"}

      ],
      top:[
        {name:"景点1",address:"地址1",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍1"},
        {name:"景点2",address:"地址2",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍2"},
        {name:"景点3",address:"地址3",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍3"},
      ]
    }
  },
  methods: {
  },
  created () {
  }
}
</script>

<style scoped>

</style>