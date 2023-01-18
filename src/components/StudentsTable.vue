<template>
  <template v-if="!isEdit">
    <td>{{item.name}}</td>
    <td><input type="checkbox" v-model="item.isDonePr"></td>
    <td>{{item.group}}</td>
    <td><a class="btn btn-outline-danger" href = "#" @click="$emit('delete', item._id)">Видалити</a></td>
    <td><a  class="btn btn-outline-success" href="#" @click="$emit('edit', item)">Змінити</a></td>
  </template>
</template>
<script>
export default {
  name: "StudentsTable",
  props: {
    item: {
      type: Object,
      require: true
    }
  }
};
</script>