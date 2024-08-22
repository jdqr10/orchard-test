<template>
  <div class="hello" style="border: 2px solid yellow;">
    <div class="three-columns">
      <div class="column"><img alt="Vue logo" src=".\img\Image-01.jpg"> </div>
      <div class="column"><img alt="Vue logo" src=".\img\Image-02.jpg"> <img class="img3" alt="Vue logo" src=".\img\Image-03.jpg">  </div>
      <div class="column-right">
        <div class="up" style="border: 2px solid purple;">
          <h2 class="comp_1_title">ANSWER YOWR BODY'S NEEDS</h2>
          <hr>
          <p class="paragraph1">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et sunt quod quae placeat, odio rem ipsum similique nesciunt aperiam iure quidem ipsam omnis consequuntur ipsa iusto laudantium facere vitae accusantium
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aperiam, eveniet nulla aliquid maiores veritatis laudantium facilis </p>
        </div>
          <div class="down" style="border: 2px solid orange;">
            <h3>BE MINDFUL</h3>
            <p class="paragraph2"><strong >Lorem ipsum dolor, sit amet consectetur adipisicing elit. Provident odit repudiandae obcaecati facilis nisi tempora. </strong></p>
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
.three-columns {
    display: flex;
    justify-content: space-between; /* or use 'space-around' or 'space-evenly' for different spacing */
}

.column {
    flex: 1; /* This makes each column take up equal space */
    padding: 10px;
    box-sizing: border-box; /* Ensures padding doesn’t affect the width */
    border: 2px solid green;
}

h2{
  font-size: 26px;
}

.img3{
  margin-top: 15px;
}

.down{
  text-align: left;
}

h3{
  font-size: 15px;
  color: red;
}
.paragraph1, .paragraph2{
  text-align: left;
  font-size: 20px;
  line-height: 1.5;
}

.column-right{
  padding: 10px;
    box-sizing: border-box;
  border: 2px solid rgb(176, 21, 21);
  display: flex;
  flex-direction: column;
  gap: 18px;
}

.comp_1_title{
  width: 100%;
}
</style>
