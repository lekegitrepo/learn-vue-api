<template>
  <div>
    <v-app id="inspire">
      <v-carousel v-model="model">
        <v-carousel-item v-for="(color, i) in colors" :key="color">
          <v-sheet :color="color" height="100%" tile>
            <v-row class="fill-height" align="center" justify="center">
              <div class="display-3">Slide {{ i + 1 }}</div>
            </v-row>
          </v-sheet>
        </v-carousel-item>
      </v-carousel>
    </v-app>
  </div>
</template>

<script>
export default {
  props: {
    colors: {
      type: Array,
    },
  },
};
</script>

<style lang="scss" scoped></style>
