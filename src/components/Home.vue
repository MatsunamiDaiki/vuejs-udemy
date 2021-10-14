<template>
  <div>
    <p v-border:dotted="{ width: '5px', color: 'red' }">Home</p>
    <h2>{{title | upperCase }}</h2>
  </div>
</template>

<script>
export default {
  data(){
    return {
      tmpData:"hello",
      title:"Welcome to Tokyo",
    }
  },
  directives: {
    border(el, binding) {
      el.style.borderWidth = binding.value.width;
      el.style.borderColor = binding.value.color;
      el.style.borderStyle = binding.arg;
    },
  },
};
</script>
