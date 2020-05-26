<template>
  <div class="bird">
    <!-- <h1>bird bird</h1> -->
    <BirdForm cmsg="msg"/>
  </div>
</template>

<script>
// @ is an alias to /src
// import used component
import BirdForm from '@/components/BirdForm.vue' 

export default {
  name: 'Bird',  // this view name
  components: {
    BirdForm     // used component name
  },
}

</script>