<template>
  <Page backgroundSpanUnderStatusBar="true" androidStatusBarBackground="#BE1965">
    <LMActionBar/>
    <AbsoluteLayout>
      <AbsoluteLayout class="country">
        <Image top="215" left="10" stretch="none" src="~/assets/images/brazil.png"/>
      </AbsoluteLayout>
      <GridLayout rows="*, auto, auto">
        <GridLayout row="0" class="card" rows="*, *" margin="10">
          <StackLayout class="pic" row="0">
            <Label text="" />
          </StackLayout>
          <GridLayout row="1" rows="auto, auto, auto, auto">
            <GridLayout row="0" rows="*, *" paddingLeft="10" paddingTop="10">
              <Label row="0" class="label-name" text="Jorge Neto, 27"/>
              <Label row="1" class="label-lastname" text="SEGTOWICH"/>
            </GridLayout>
            <FlexboxLayout row="1" flexWrap="wrap" alignContent="space-between">
              <LMChips text="CS:GO"/>
              <LMChips text="PUBG"/>
              <LMChips text="LOL"/>
            </FlexboxLayout>
            <GridLayout row="2" columns="*, *" paddingTop="10" paddingLeft="10"> 
              <GridLayout col="0" columns="auto, auto">
                <Image col="0" stretch="none" src="~/assets/images/baseline-sentiment_very_satisfied-24px.png"/>
                <Label col="1" class="level" text="AMIGAVEL"/>
              </GridLayout>
              <GridLayout col="1" columns="auto, auto">
                <Image col="0" stretch="none" src="~/assets/images/baseline-school-24px.png"/>
                <Label col="1" class="level" text="PROFESSOR"/>
              </GridLayout>
            </GridLayout>
            <StackLayout row="3" marginTop="15">
              <Label class="title" text="A PROCURA DE" paddingLeft="10"/>
              <FlexboxLayout flexWrap="wrap" alignContent="space-between">
                <LMChips text="TOP LANER"/>
                <LMChips text="DUO"/>
                <LMChips text="RANKED"/>
              </FlexboxLayout>
            </StackLayout>
          </GridLayout>
        </GridLayout>
        <FlexboxLayout justifyContent="space-between" row="1">
          <StackLayout paddingLeft="80" class="center">
            <LMFabButton :icon="'~/assets/images/ic_expand_close.png'" color="#E60730"/>
          </StackLayout>
          <StackLayout paddingRight="80" class="center">
            <LMFabButton :icon="'~/assets/images/baseline-thumb_up-24px.png'" color="#009688"/>
          </StackLayout>
        </FlexboxLayout>
        <StackLayout padding="20 10" row="2">
          <GridLayout row="0" class="tab-menu" columns="auto, *, auto">
            <GridLayout col="0" columns="auto, auto">
              <Image class="tab-img tab-profile" col="0" stretch="none" src="~/assets/images/baseline-face-24px.png"/>
              <Label col="1" class="tab-item" text="PERFIL"/>
            </GridLayout>
            <Label col="1" text="" />
            <GridLayout col="2" columns="auto, auto">
              <Image class="tab-img" col="0" stretch="none" src="~/assets/images/baseline-chat-24px.png"/>
              <Label col="1" class="tab-item" text="CHAT"/>
            </GridLayout>
          </GridLayout>
        </StackLayout>
      </GridLayout>
      <AbsoluteLayout row="1">
        <LMFabButton class="country" top="90vh" left="160" :icon="'assets/images/baseline-thumb_up-24px.png'" color="#BE1965"/>
      </AbsoluteLayout>
    </AbsoluteLayout>
  </Page>
</template>

<script>
  import LMActionBar from '~/components/LMActionBar'
  import LMChips from '~/components/LMChips'
  import LMFabButton from '~/components/LMFabButton'

  export default {
    components: {
      LMActionBar,
      LMChips,
      LMFabButton
    },
  }
</script>

<style lang="scss" scoped>
.center {
  margin: 0 25;
  text-align: center;
}

.card {
  height: 450;
  width: 355;
  border-radius: 5;
  background-color: #ffffff;
  border-style: "solid";
  border-width: 1;
  border-color: #d6d6d6;
}

.pic {
  border-bottom-color: #d6d6d6;
  border-bottom-style: solid;
  border-bottom-width: 1;
}

.country {
  z-index: 9999;
}

.tab-menu {
  width: 355;
  height: 40;
  border-radius: 200;
  background-color: #633280;
  color: #ffffff;
  .tab-item {
    padding-right: 10;
    font-family: "Poppins";
    font-size: 18;
    font-weight: normal;
    font-style: normal;
    line-height: 27;
    color: #ffffff;
  }

  .tab-img {
    margin-top: 10;
    margin-right: 5;
  }

  .tab-profile {
    margin-left: 5;
  }
}
</style>
