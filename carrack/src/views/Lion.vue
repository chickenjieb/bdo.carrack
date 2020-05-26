<template>
  <div class="lion">
    <!-- <h1>lion lion</h1> -->
    <LionForm cmsg="msg"/>
  </div>
</template>

<script>
// @ is an alias to /src
// import used component
import LionForm from '@/components/LionForm.vue' 

export default {
  name: 'Lion',  // this view name
  components: {
    LionForm     // used component name
  },
}

</script>