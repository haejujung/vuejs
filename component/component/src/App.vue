<script>
  import UserProfile from '@/components/UserProfile.vue';
  export default {
    components: {
      UserProfile,
    },
    data(){
      return{
        userName: '정해주',
      };
    },
  }
</script>
<template>
  <UserProfile :name="userName"/>
</template>