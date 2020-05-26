<template>
  <div class="deer">
    <!-- <h1>deer deer</h1> -->
    <DeerForm cmsg="msg"/>
  </div>
</template>

<script>
// @ is an alias to /src
// import used component
import DeerForm from '@/components/DeerForm.vue' 

export default {
  name: 'Deer',  // this view name
  components: {
    DeerForm     // used component name
  },
}

</script>