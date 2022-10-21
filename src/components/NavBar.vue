<template>
  <div class="header header-font bg-primary py-1">
    <div class="logo">
      <img class="ml-5 mt-1" src="../assets/Logo.png"/>
    </div>
    <div class="links upper-case text-white">
      <div class="link mr-5">
        <a class="ml-2">Store Home</a>
        <a class="ml-2">About</a>
        <a class="ml-2">Contact</a>
        <a class="ml-2">Reviews</a>
      </div>
    </div>
  </div>
</template>
<script>

</script>
<style>
  .logo{
    width: 25%;
    float: left;
  }
  .links{
    display: flex;
    width: 75%;
    float: left;
    justify-content: flex-end;
    font-Weight: 500;
    font-size: 14px;
    line-height: 21px;
  }
  .link{
  }
  .header{
    display: flex;
    align-items: center;
    font-size: 42px;
    line-height: 63px;
    font-size: 42px;
    line-height: 63px;
    padding-top: 0.5rem;
    padding-bottom: 0.5rem;
  }
</style>