<template web>
  <Page>
    <GridLayout>
      <Label text="This is an about page" :textWrap="true" horizontalAlignment="center" verticalAlignment="center"/>
    </GridLayout>
  </Page>
</template>
<template native>
  <Page>
    <ActionBar :title="navbarTitle"/>
    <GridLayout>
      <Label text="This is an about page" :textWrap="true" horizontalAlignment="center" verticalAlignment="center"/>
    </GridLayout>
  </Page>
</template>
<script>

  export default {
    data() {
      return {
        navbarTitle: `About.vue`
      };
    }
  };
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import '~styles/style-two';
  @import '~styles/style-one';

  .nvw-label {
    height: 100%;
    width: 100%;
    padding-top: 3em;
    position: relative;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: top;
    align-items: center;
  }
</style>
