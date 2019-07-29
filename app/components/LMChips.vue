<template>
  <Label class="chips" :text="text"></Label>
</template>

<script>
export default {
  name: 'LMChips',
  props: {
    text: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.chips {
  height: 26;
  margin-left: 10;
  border-radius: 13;
  font-family: "Poppins";
  background-color: #633280;
  color: white;
  text-align: center;
  padding: 10;
  margin-top: 10;
  font-size: 14;
  font-weight: 300;
}
</style>
