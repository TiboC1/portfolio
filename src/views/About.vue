<template>
  <div class="about">
    <div class="empty"></div>
    <h2>About</h2>
    <div id="main-icons" class="container-fluid">
      <div class="row">
        <div v-for="icon in icons" :key="icon.id" class="col-sm-6 col-md-6 col-lg-3">
          <img class="mb-4" :src="getImg(icon.imgSource)" alt="">
        </div>
      </div>
    </div>
    <div id="skills-list">
      <ul class="list-group">
        <li v-for="skill in skills" :key ="skill.id">{{skill.name}}</li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      icons: [
        {
          name: "Speed",
          id: 1,
          imgSource: "speed.png"
        },
        {
          name: "responsiveness",
          id: 2,
          imgSource: "responsive.png"
        },
        {
          name: "Dynamic",
          id: 3,
          imgSource: "dynamic.png"
        },
        {
          name: "SEO",
          id: 4,
          imgSource: "seo.png"
        },
      ],


      skills: [
        {
          name: "HTML",
          id: 1,
        },
        {
          name: "CSS",
          id: 2,
        },
        {
          name: "Javascript",
          id: 3,
        },
        {
          name: "Vue",
          id: 4,
        },
        {
          name: "PHP",
          id: 5,
        },
        {
          name: "Laravel",
          id: 6,
        },
        {
          name: "Symfony",
          id: 7,
        },
        {
          name: "SEO",
          id: 8,
        },
      ]
    };
  },
  methods: {
    getImg(pic){
      return require('../assets/' + pic)
    }
  }
}
</script>

<style scoped>
.about{
  background: #45484d; /* Old browsers */
  background: -moz-linear-gradient(-45deg,  #45484d 0%, #000000 100%); /* FF3.6-15 */
  background: -webkit-linear-gradient(-45deg,  #45484d 0%,#000000 100%); /* Chrome10-25,Safari5.1-6 */
  background: linear-gradient(135deg,  #45484d 0%,#000000 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#45484d', endColorstr='#000000',GradientType=1 ); /* IE6-9 fallback on horizontal gradient */
  min-height: 100vh;
}

img{
  max-width: 100px;
}

.empty{
  height: 10vh;
  min-height: 40px;
}
</style>