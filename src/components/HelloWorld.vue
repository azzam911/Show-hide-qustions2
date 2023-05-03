<template>
    <div class="hello" v-for="question in questions" :key="question">
    <h1 @click="question.open = !question.open">{{ question.title }}?</h1>
      <Transition name="slide-fade">
          <div class="message" v-show="question.open">
            <h4>{{ question.answer }}</h4>
          </div>
      </Transition>
  </div>
  
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      questions : {
        'question one':{
          'open': false,
          'title':'What Is Your Name',
          'answer':"My Name Is Azzam"
        },
        'question two':{
          'open': false,
          'title':'What Is Your Name',
          'answer':"My Name Is Zaid"
        },
        'question three':{
          'open': false,
          'title':'What Is Your Name',
          'answer':"My Name Is Abduallh"
        },
        'question four':{
          'open': false,
          'title':'What Is Your Name',
          'answer':"My Name Is Azzam"
        },
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
button {
  cursor: pointer;
}
.hello {
  background-color: #eee;
    width: 30rem;
    margin: 20px auto;
    padding: 20px;
    border-radius: 10px;
    color: #000;
}
.message {
  background-color: #fff;
  padding: 20px;
  color: #000;
  border-radius: 10px;
  font-size: 20px;
}

h1 {
  cursor: pointer;
}
/*
  Enter and leave animations can use different
  durations and timing functions.
*/
.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.4s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateX(20px);
  opacity: 0;
}


</style>
