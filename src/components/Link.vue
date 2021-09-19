<template>
  <div class="container_link">
    <a 
      class="link" 
      :style="{'color': styles.color, 'background-color': styles.background}" 
      :href="url"
    >
      <i :class="icon"></i>
      <span>{{ text }}</span>
    </a>
  </div>
</template>

<script>
export default {
    name: 'Link',
    props: {
      text:   String,
      icon:   String,
      url:    String,
      styles: Object
    }
}
</script>

<style lang="scss">
.link
{
  display: inline-block;
  padding: 18px;
  margin-bottom: 12px;
  text-decoration: none;
  border-radius: 16px 0 16px 0;
  width: 100%;
  text-align: center;
  font-weight: 600;
  letter-spacing: 2px;
  transition: .4s;

  &:hover
  {
    transform: scale(1.1);
    box-shadow: 2px 2px 2px #fff;
  }

  i
  {
    position: absolute;
    left: 25px;
    font-size: 21px;
  }
}

</style>
