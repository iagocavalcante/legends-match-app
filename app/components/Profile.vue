<template>
  <Page backgroundSpanUnderStatusBar="true" androidStatusBarBackground="#BE1965">
    <LMActionBar/>
    <GridLayout rows="*, auto" padding="10">
      <ScrollView row="0" scrollBarIndicatorVisible="false"
        paddingBottom="100">
        <GridLayout rows="*, *, *, *">
          <GridLayout row="0" columns="auto, *">
            <Image col="0" class="profile-pic" src="~/assets/images/profile-pic.png"/>
            <GridLayout col="1" paddingLeft="15" rows="*, *, *">
              <Label row="0" class="label-name" text="Jorge Neto, 27"/>
              <Label row="1" class="label-lastname" text="SEGTOWICH"/>
              <Image row="2" stretch="none" src="~/assets/images/brazil.png"/>
            </GridLayout>
          </GridLayout>
          <GridLayout row="1" columns="*, *" paddingTop="10">
            <GridLayout col="0" columns="auto, auto">
              <Image col="0" stretch="none" src="~/assets/images/baseline-sentiment_very_satisfied-24px.png"/>
              <Label col="1" class="level" text="AMIGAVEL"/>
            </GridLayout>
            <GridLayout col="1" columns="auto, auto" paddingLeft="20">
              <Image col="0" stretch="none" src="~/assets/images/baseline-school-24px.png"/>
              <Label col="1" class="level" text="PROFESSOR"/>
            </GridLayout>
          </GridLayout>
          <GridLayout row="2" rows="*, *, *" paddingTop="20">
            <StackLayout row="0" marginTop="10">
              <Label class="title" text="JOGA" />
              <FlexboxLayout class="position" flexWrap="wrap" alignContent="space-between">
                <LMChips text="CS:GO"/>
                <LMChips text="LOL"/>
                <LMChips text="PUBG"/>
                <LMChips text="FORTNITE"/>
              </FlexboxLayout>
            </StackLayout>
            <StackLayout row="1" marginTop="10">
              <Label class="title" text="CARACTERISTICAS" />
              <FlexboxLayout class="position" flexWrap="wrap" alignContent="space-between">
                <LMChips text="TOP LANER"/>
                <LMChips text="AD CARRY"/>
                <LMChips text="CAMPER"/>
                <LMChips text="LUKER"/>
              </FlexboxLayout>
            </StackLayout>
            <StackLayout row="2" marginTop="10">
              <Label class="title" text="A PROCURA DE" />
              <FlexboxLayout class="position" flexWrap="wrap" alignContent="space-between">
                <LMChips text="TOP LANER"/>
                <LMChips text="DUO"/>
                <LMChips text="RANKED"/>
              </FlexboxLayout>
            </StackLayout>
          </GridLayout>
        </GridLayout>
      </ScrollView>
      <FlexboxLayout row="1" class="footer" alignContent="center">
        <StackLayout width="50%">
          <Button text="EDITAR" class="btn-edit"></Button>
        </StackLayout>
        <StackLayout width="50%">
          <Button text="SAIR" class="btn-cancel"></Button>
        </StackLayout>
      </FlexboxLayout>
    </GridLayout>
  </Page>
</template>

<script>
  import LMActionBar from './LMActionBar'
  import LMChips from './LMChips'
  export default {
    components: {
      LMActionBar,
      LMChips
    },
  }
</script>

<style lang="scss" scoped>
.profile-pic {
  width: 120;
  height: 120;
  border-radius: 10;
  border-color: #633280;
  border-width: 3;
  border-style: solid;
}

.label-name {
  font-family: "Poppins";
  font-size: 26;
  font-weight: 300;
  font-style: normal;
  line-height: 39;
  color: #be1965;
}

.label-lastname {
  font-family: "Poppins";
  font-size: 20;
  font-weight: 600;
  font-style: normal;
  line-height: 30;
  color: #be1965;
}

.level {
  margin-left: 5;
  height: 25;
  padding: 10;
  border-radius: 50;
  background-color: #be1965;
  font-family: "Poppins";
  font-size: 16;
  font-weight: 300;
  font-style: normal;
  line-height: 25;
  color: #ffffff;
}

.title {
  font-family: "Poppins";
  font-size: 16;
  font-weight: normal;
  font-style: normal;
  color: #be1965;
}

.btn-cancel {
  padding: 5;
  width: 86;
  height: 30;
  border-radius: 50;
  border-style: "solid";
  border-width: 3;
  border-color: #dc1543;
  color: #dc1543;
}

.btn-edit {
  padding: 5;
  width: 86;
  height: 30;
  border-radius: 50;
  border-style: "solid";
  border-width: 3;
  border-color: #633280;
  color: #633280;
}

.footer {
  padding: 15;
  position: absolute;
  right: 0;
  bottom: 0;
  left: 0;
  text-align: center;
}
</style>
