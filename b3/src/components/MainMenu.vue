<template>
  <v-container
    id="menu-container"
    fluid
    class="flex-column max-w-3xl menu-container"
  >
    <p />
    <v-container
      fluid
      class="flex structure-list justify-center"
    >
      <StructureItem
        v-for="item in dataStructures"
        :key="item.code"
        :name="item.name"
        :data-structure="item"
      />
    </v-container>
    <v-row
      justify="center"
      no-gutters
    >
      <v-col
        sm="1"
      >
        <img
          aria-label="UNSA MAESTRIA"
          src="https://www.unsa.edu.pe/jaku/wp-content/themes/observatorio/img/unsa-logo.png"
        >
      </v-col>
    </v-row>
    <v-container>
      <h2 class="title">
        Realizado por:
      </h2>
      <h3 class="subtitle-1">
        <a
          target="_blank"
          role="link"
          aria-label="Creator git-hub link"
          href="https://github.com/ricktonycr"
        >Cruz Richard</a>
          &
        <a
          target="_blank"
          role="link"
          aria-label="Creator git-hub link"
          href="https://github.com/ddezav"
        >David Desa</a> &
        <a
          target="_blank"
          role="link"
          aria-label="Creator git-hub link"
          href="https://github.com/yolose100"
        >Tellez Elvis</a>
           </h3>
     </v-container>
  </v-container>
</template>

<script>
import StructureItem from './StructureItem.vue';

export default {
  name: 'MainMenu',
  components: {
    StructureItem,
  },
  props: {
  },
  data: () => ({
    dataStructures: [
      {
        name: 'B Tree',
        imageUrl: 'https://www.bforball.com/images/drawing-lessons/bird-with-b-98/step9.png',
        code: 'b-tree',
        structureType: 'tree',
        simpleHtml: '/structure/tree/b-tree',
      },
      {
        name: 'AVL',
        imageUrl: 'https://firebasestorage.googleapis.com/v0/b/structies.appspot.com/o/minheap.jpg?alt=media&token=98746fc9-b164-421a-8690-bc1c2bcdef63',
        code: 'avl.html',
        structureType: 'tree',
        simpleHtml: '/avl.html',
      }],
  }),

};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .menu-container {
    flex-wrap: wrap;
  }
</style>
