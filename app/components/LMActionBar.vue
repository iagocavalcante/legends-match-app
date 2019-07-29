<template>
  <ActionBar flat="true">
    <FlexboxLayout alignContent="center" class="header">
      <Label alignSelf="center" class="header-legend" text="LEGENDS"></Label>
      <Label alignSelf="center" class="header-match" text="MATCH"></Label>
    </FlexboxLayout>
    <NavigationButton text="" android.systemIcon="ic_menu_back"/>
  </ActionBar>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.header {
  horizontal-align: center;
  font-size: 20;
  .header-legend {
    font-weight: 300;
    color: #be1965;
  }
  .header-match {
    font-weight: bold;
    color: #633280;
  }
}
</style>
