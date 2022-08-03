<template>

<div class="post">
    <div class="post-header">
      <!-- 이미지를 스타일 속성 안에 url로 넣어야 잘 보임
      속성에 데이터 바인딩해서 이미지 넣으려면 속성 앞에 :붙이기 -->
      <!-- 백틱기호를 써서 문자로 만들면 `문자 ${변수}문자` 형태가 됨 -->
      <div class="profile" :style="{backgroundImage:`url(${인스타데이터.userImage})`}"></div>
      <span class="profile-name">{{인스타데이터.name}}</span>
    </div>
    <div class="post-body" :style="{backgroundImage:`url(${인스타데이터.postImage})`}"></div>
    <div class="post-content">
      <p>{{인스타데이터.likes}} Likes</p>
      <p><strong>{{인스타데이터.name}}</strong> {{인스타데이터.content}}</p>
      <p class="date">{{인스타데이터.date}}</p>
    </div>
</div> 


</template>

<script>

export default{ 
name:'',
components:{
},
props:{
인스타데이터:Object

},
data(){
    return{
};
    },
    setup(){},
    created(){},
    mounted(){},
    unmounted(){},
    methods:{}
}
</script>

<style>

.post {
  width: 100%;
}
.profile {
  background-image: url("https://placeimg.com/100/100/arch");
  width: 30px;
  height: 30px;
  background-size: 100%;
  border-radius: 50%;
  float: left;
}
.profile-name {
  display: block;
  float: left;
  padding-left: 10px;
  padding-top: 7px;
  font-size: 14px;
}
.post-header {
  height: 30px;
  padding: 10px;
}
.post-body {
  background-image: url("https://placeimg.com/640/480/animals");
  height: 450px;
  background-position: center;
  background-size: cover;
}
.post-content {
  padding-left: 15px;
  padding-right: 15px;
  font-size: 14px;
}
.date {
  font-size: 11px;
  color: grey;
  margin-top: -8px;
} 

</style>