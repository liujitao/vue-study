<template>
  <div class="item">
    <p>
      <span v-show="!isActive" v-on:click="activeItem">{{ item }}</span>
      <span v-show="isActive">
        <input v-model="content" v-on:blur="inactiveItem" type="text" />
      </span>
      <span v-on:click="$emit('deleteItem', index)">X</span>
    </p>
  </div>
</template>

<script>
export default {
  name: 'TodoListItem',
  props: ['item', 'index'],
  data() {
    return {
      content: '',
      isactive: false,
    }
  },
  methods: {
    activeItem() {
      this.isactive = true
      this.content = this.item
    },
    inactiveItem() {
      this.$emit('modifyItem', this.content, this.index)
      this.isactive = false
    },
  },
}
</script>