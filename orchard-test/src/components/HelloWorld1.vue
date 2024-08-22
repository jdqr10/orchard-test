<template>
  <div class="hello" style="border: 2px solid yellow;">
    <div class="div" style="border: 2px solid pink">
      <h1>ALL THE LATEST FROM AEG</h1>
      <div class="recipes">
        <div class="card" style="border: 2px solid blue">
          <img style="border-bottom: 4px solid red;" alt="Vue logo" src=".\img2\Image-01.jpg">
          <div class="info1">
            <h2>Summer Lunch Menu Mark Best</h2>
          <p>AEG ambasssador Mark Best's summer eats are guarnteed to help you make the most of the warner amnd enteranting at home</p>
          <a href="">READ MORE</a>
          </div>
        </div>
        <div class="card" style="border: 2px solid blue">
          <img style="border-bottom: 4px solid red;" alt="Vue logo" src=".\img2\Image-02.jpg">
          <div class="info">
            <h2>A Traditional Chrismas Eve, Mark Best Style</h2>
          <p>AEG ambasssador Mark Best's summer eats are guarnteed to help you make the most of the warner amnd enteranting at home</p>
          <a href="">READ MORE</a>
          </div>
        </div>
        <div class="card" style="border: 2px solid blue">
          <img style="border-bottom: 4px solid red;" alt="Vue logo" src=".\img2\Image-03.jpg">
          <div class="info">
            <h2>Taking Taste Further</h2>
          <p>AEG ambasssador Mark Best's summer eats are guarnteed to help you make the most of the warner amnd enteranting at home st of the warner amnd enteranting at home</p>
          <a href="">READ MORE</a>
          </div>
        </div>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello{
   background-color: #0e0e0e;
   padding: 130px 100px 100px 140px;
}
h1{
  font-size: 38px;
}
.recipes{
  display: flex;
 gap: 20px;
 margin-top: 55px;
}
.card{
  width: 100%;
}

h2{
  font-size: 18px;
}
.info1{
  text-align: left;
  width: 87%;
  margin-left: 9px;
}

.info{
  text-align: left;
  margin-left: 9px;
}

p{
  color: gray;
  line-height: 1.5;
}

a{
  color: white;
}

</style>
