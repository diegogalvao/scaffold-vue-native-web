<template web>
  <Page>
    <GridLayout rows="auto, auto">
      <!-- copy-webpack-plugin copies asset from src/assets to project output/build directory /assets -->
      <Img src="~/assets/logo.png" row="0" class="m-20"/>
      <HelloWorld :msg="msg" row="1"/>
    </GridLayout>
  </Page>
</template>
<template native>
  <Page>
    <ActionBar :title="navbarTitle"/>
    <GridLayout rows="auto, auto">
      <!-- copy-webpack-plugin copies asset from src/assets to project output/build directory /assets -->
      <Image src="~/assets/logo.png" row="0" class="m-20"/>
      <HelloWorld :msg="msg" row="1"/>
    </GridLayout>
  </Page>
</template>
<script>
  import HelloWorld from 'components/HelloWorld';

  const { VUE_APP_MODE, VUE_APP_PLATFORM } = process.env;

  export default {
    name: 'home',
    components: {
      HelloWorld,
    },
    data() {
      return {
        navbarTitle: `Home.vue`,
        msg: `Mode=${VUE_APP_MODE} and Platform=${VUE_APP_PLATFORM}`
      };
    }
  };

</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import '~styles/style-one';
  @import '~styles/style-two';

  img, Image {
    display: block;
    margin: auto;
    margin-top: 4em;
  }

  Image {
    height: 20%;
    width: 20%;
  }
</style>
