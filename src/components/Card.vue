<template>
<div class="card shadow-sm">
  <span class="img" :style="{backgroundImage: `url(${item.termsDetailUrl})`}" />
      <div class="card-body">
        <p class="card-text"> {{ item.name }}</p>
        <div class="d-flex justify-content-between align-items-center">
          <div class="btn-group">
            <button class="btn btn-primary">동의</button>
          </div>
          <small class="text-body-secondary">필수사항</small>
        </div>
      </div>
  </div>
</template>
  
  
  <script>
      export default {
        name: 'Card',
        props: {
          item: Object
        }
      }
  </script>
      
      <!-- Add "scoped" attribute to limit CSS to this component only -->
      <style scoped>
      </style>
  