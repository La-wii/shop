<template>
  <header>
    <div class="container">
      <div class="nav col-xs-12 col-md-10 px-2 mx-auto">
        <ul>
          <li v-for="(link, index) in link" :key="index" class="px-5"> 
            <a :href="link.url">{{link.text}}</a>   
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data (){
    return {
        link :[
        {
          text: 'Home',
          url:'#',
          current: false,
        },
        {
          text: 'I nostri drink',
          url:'#drink',
          current: false,
        },
        {
          text: 'Chi siamo',
          url:'#chisiamo',
          current: false,
        },
        {
          text: 'DrinkRandom',
          url:'#drinkrandom',
          current: false,
          
        },
        {
          text: 'Contatti',
          url:'#contatti',
          current: false,
        }
        ]
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
header{
  background: rgb(233,192,33);
  background: linear-gradient(90deg, rgba(233,192,33,1) 0%, rgba(220,55,230,1) 35%, rgba(0,212,255,1) 100%);
}
.container{
  width: 80%;
}
li
{
  padding-top: 10px;
  display: inline-block;
  list-style: none;
  font-size: 14px;
}
.nav ul li a{
  text-decoration: none;
  color: white;
}
.nav ul li a:hover{
  color: rgb(6, 6, 70);
}
</style>
