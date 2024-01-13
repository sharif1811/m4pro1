<script setup>
  import {ref} from 'vue';

    const title = "this is our logo";
    const imgUrl = "https://www.sportico.com/wp-content/uploads/2020/09/0911_IMG.jpg";
    const des = "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sapiente qui dolore odio accusantium, placeat corrupti optio maiores amet magni . Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas, minima?";
    const width ="1000";
    const classText = 'text-red-500';
    const cssStyle = 'color:red;';
    const favColor = 'yellow';
    const number = ref(81);
    const showImage = ref(true);
    const showText = ref(true);
    const activeCountry = ref('Nepal')
    // function setActiveCountry(){
    //   const userInput = prompt('Enter Your Country Name ?');
    //   activeCountry.value = userInput;
    // }

    function countNumber (){
      const NumberCount = prompt('Enter Your Number');
      number.value = NumberCount;
    }

</script>

  <!--  -->


<template>
  <!-- <div>
    <h1 class="text-2xl">Corntry Name : <strong class="text-red-900"> {{ activeCountry }}</strong></h1>
    <ul>
      <li class="p-5" v-show="activeCountry=='Bangladesh'"> 
        <h2><strong class="underline">Bangladesh</strong></h2>
        <p><strong>Capital :</strong>Dhaka</p>
        <p><strong>Population :</strong>16165242</p>
        <p><strong>Area :</strong>147570</p>
      </li>
      <li class="p-5" v-show="activeCountry=='Nepal'">
        <h2 class="underline"><strong>Nepal</strong></h2>
        <p><strong>Capital :</strong>Dhaka</p>
        <p><strong>Population :</strong>16165242</p>
        <p><strong>Area :</strong>147570</p>
      </li>
      <li class="p-5" v-show="activeCountry=='Bhutan'">
        <h2 class="underline"><strong>Bhutan</strong></h2>
        <p><strong>Capital :</strong>Maldhip</p>
        <p><strong>Population :</strong>65242</p>
        <p><strong>Area :</strong>14570</p>
      </li>
      <li class="p-5" v-show="activeCountry=='Pakistan'">
        <h2 class="underline"><strong>Pakistan</strong></h2>
        <p><strong>Capital :</strong>Dhaka</p>
        <p><strong>Population :</strong>16165242</p>
        <p><strong>Area :</strong>147570</p>
      </li>
    </ul>
    <div>
        <button @click="setActiveCountry()" class="bg-blue-900 px-4 py-2 rounded-xl text-white font-bold">Set Active Country</button>
    </div>
    <div>
      <button @click="activeCountry='Bangladesh'" class="bg-blue-800 rounded-lg px-4 py-2 font-bold text-xl text-white ml-3">Bangladesh</button>
      <button @click="activeCountry='Nepal'" class="bg-blue-800 rounded-lg px-4 py-2 font-bold text-xl text-white ml-3">Nepal</button>
      <button @click="activeCountry='Bhutan'" class="bg-blue-800 rounded-lg px-4 py-2 font-bold text-xl text-white ml-3">Bhutan</button>
      <button @click="activeCountry='Pakistan'" class="bg-blue-800 rounded-lg px-4 py-2 font-bold text-xl text-white ml-3">Pakistan</button>
    </div>
  </div>
  <div class="div" >
    <h3 class="text-3xl font-bold underline">{{ title }}</h3>
    <img v-show="showImage" :width="width" :src="imgUrl" :alt="logo">
    <p v-show="showText" class="des" :class="classText" > {{ des }}</p>
  </div>
  <button @click="showImage=!showImage" class="bg-blue-800 ml-3 hover:bg-black text-white font-bold rounded-lg border-oragne-500 px-5 py-3 cursor-zoom-in">Hide Image</button>
  <button @click="showText=!showText" class="bg-blue-800 ml-3 hover:bg-black text-white font-bold rounded-lg border-orange-800 px-5 py-3 border-collapse">Hide Text</button>
  <h2 v-if="favColor=='red'">I Love Red</h2>
  <h2 v-if="favColor=='green'">I Love Blue</h2>
  <h2 v-if="favColor=='blue'">I Love green</h2>
  <h2 v-else>color dose not like</h2> -->
  <div>
    <span>{{ number }}</span>
    <span v-show="(number % 2 == 0)">   Number is Even  </span>
    <span v-show="(number % 2 == 1)">  Number is Odd</span><br>
    <button @click="number--" min="1" class="bg-red-900 text-white font-bold px-4 py-2 rounded-sm mt-5">decress</button>
    <button @click="number++" class="bg-blue-900 ml-4 text-white font-bold px-4 py-2 rounded-sm mt-5">Incress</button>

  <button @click="countNumber()" class="bg-blue-900 ml-4 text-white font-bold px-4 py-2 rounded-sm mt-5">Enter Number</button>
  </div>
</template>
<style scoped>
template{
  width: 6rem;
  margin: auto;
}
  h3{
    font: 30px;
    color: black;
    text-align:left;
    margin-bottom: 30px;
  }
  p{
    font: 30px;
    text-align:left;
  }
</style>
