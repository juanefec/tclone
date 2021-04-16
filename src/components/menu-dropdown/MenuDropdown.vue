<template>
    <v-menu rounded="b-xl" offset-y>
        <template v-slot:activator="{ attrs, on }">
          <v-btn
            :color="color"
            class="white--text ma-5"
            v-bind="attrs"
            v-on="on"
          >
            {{ text }}
          </v-btn>
        </template>
  
        <v-list>
          <v-list-item
            v-for="item in items"
            :key="item"
            @click="handleModelChange(item)"
            link
          >
            <v-list-item-title v-text="item"></v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
</template>
<script>
export default {
    name: "MenuDropdown",
    model: {
        prop: 'modelValue',
        event: 'change'
    },
    props: ['modelValue', 'color', 'text', 'items'],
    methods: {
        handleModelChange(item) {
            this.$emit("change", item)
        }
    }
    
}
</script>