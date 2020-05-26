<template>
  <div class="horse">
    <!-- <h1>horse horse</h1> -->
    <HorseForm cmsg="msg"/>
  </div>
</template>

<script>
// @ is an alias to /src
// import used component
import HorseForm from '@/components/HorseForm.vue' 

export default {
  name: 'Horse',  // this view name
  components: {
    HorseForm     // used component name
  },
}

</script>