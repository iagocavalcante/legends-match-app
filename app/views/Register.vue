<template>
  <Page backgroundSpanUnderStatusBar="true" androidStatusBarBackground="#BE1965">
    <LMActionBar/>
    <GridLayout rows="*">
      <ScrollView row="0" scrollBarIndicatorVisible="false"
        paddingBottom="100">
        <GridLayout rows="auto, *, auto, auto, auto, auto, auto, auto">
          <StackLayout row="0" class="btn-upload">
            <FlexboxLayout justifyContent="space-around" flexDirection="column">
              <GridLayout class="label-upload" rows="auto, auto">
                <Label row="0" alignSelf="center" text="ADICIONAR"></Label>
                <Label row="1" alignSelf="center" text="IMAGEM"></Label>
              </GridLayout>
              <Image alignSelf="center" stretch="none" src="~/assets/images/baseline-add_circle-24px.png"></Image>
            </FlexboxLayout>
          </StackLayout>
          <Label row="1" class="label" text="DADOS PESSOAIS"></Label>
          <GridLayout row="2" rows="*, *, *, *, *, *, *, *" class="header">
            <StackLayout row="0" class="input-field">
              <TextField class="input" hint="Nome"
                keyboardType="email" autocorrect="false"
                autocapitalizationType="none"
                ></TextField>
            </StackLayout>
            <StackLayout row="1" class="input-field">
              <TextField class="input" hint="Nick"
                autocorrect="false"
                autocapitalizationType="none"
                ></TextField>
            </StackLayout>
            <StackLayout row="2" class="input-field">
              <TextField class="input" hint="Idade"
                keyboardType="number" autocorrect="false"
                autocapitalizationType="none"
                ></TextField>
            </StackLayout>
            <!-- <StackLayout row="3" class="input-field">
              <ListPicker class="input list-picker" :items="countries" v-model="selectedCountry" />
            </StackLayout>
            <StackLayout row="4" class="input-field">
              <ListPicker class="input list-picker" :items="states" v-model="selectedState" />
            </StackLayout> -->
            <StackLayout row="3" class="input-field">
              <TextField class="input" hint="E-mail"
                keyboardType="emal" autocorrect="false"
                autocapitalizationType="none"
                ></TextField>
            </StackLayout>
            <GridLayout row="4" columns="*, *">
              <StackLayout col="0" class="input-field">
                <TextField class="input input-password" hint="Senha"
                  secure="true"
                  keyboardType="text" autocorrect="false"
                  autocapitalizationType="none"
                  ></TextField>
              </StackLayout>
              <StackLayout col="1" class="input-field password">
                <TextField class="input input-password" hint="Repetir senha"
                  secure="true"
                  keyboardType="text" autocorrect="false"
                  autocapitalizationType="none"
                  ></TextField>
              </StackLayout>
            </GridLayout>
            <StackLayout row="5" class="input-field">
              <TextView class="input text-area" hint="Sobre você"
                keyboardType="emal" autocorrect="true"
              ></TextView>
            </StackLayout>
          </GridLayout>
          <Label row="3" class="label label-jogador" text="DADOS DE JOGADOR"></Label>
          <GridLayout row="4" rows="*, *, *, *, *, *, *, *" class="header">
            <StackLayout row="0" class="input-field">
              <TextField class="input" hint="Nome"
                keyboardType="email" autocorrect="false"
                autocapitalizationType="none"
                ></TextField>
                <FlexboxLayout class="position" flexWrap="wrap" alignContent="space-between">
                  <LMChips text="TOP LANER"/>
                  <LMChips text="AD CARRY"/>
                  <LMChips text="CAMPER"/>
                  <LMChips text="TOP LANER"/>
                </FlexboxLayout>
            </StackLayout>
            <StackLayout row="1" class="input-field">
              <TextField class="input" hint="Nick"
                autocorrect="false"
                autocapitalizationType="none"
                ></TextField>
                <FlexboxLayout class="position" flexWrap="wrap" alignContent="space-between">
                  <LMChips text="TOP LANER"/>
                  <LMChips text="AD CARRY"/>
                  <LMChips text="CAMPER"/>
                  <LMChips text="TOP LANER"/>
                </FlexboxLayout>
            </StackLayout>
            <StackLayout row="2" class="input-field">
              <TextField class="input" hint="Idade"
                keyboardType="number" autocorrect="false"
                autocapitalizationType="none"
                ></TextField>
                <FlexboxLayout class="position" flexWrap="wrap" alignContent="space-between">
                  <LMChips text="TOP LANER"/>
                  <LMChips text="AD CARRY"/>
                  <LMChips text="CAMPER"/>
                  <LMChips text="TOP LANER"/>
                </FlexboxLayout>
            </StackLayout>
          </GridLayout>
          <Label row="5" class="label" text="VINCULAR CONTAS"></Label>
          <StackLayout row="6" class="accounts">
            <FlexboxLayout>
              <Image width="15%" src="~/assets/images/riot-games.png" stretch="none"></Image>
              <GridLayout width="80%" class="status" rows="auto, auto">
                <Label class="status-account" row="0" text="CONTA VINCULADA"></Label>
                <Label class="account-date" row="1" text="21.12.2019"></Label>
              </GridLayout>
              <StackLayout width="5%">
                <Image class="icon-left" src="~/assets/images/ic_more_vert_white.png" stretch="none"></Image>
              </StackLayout>
            </FlexboxLayout>
            <FlexboxLayout class="accounts-vinculate">
              <Image width="15%" src="~/assets/images/iconmonstr-steam-4.png" stretch="none"></Image>
              <GridLayout width="80%" class="status" rows="auto, auto">
                <Label class="status-account" row="0" text="CONTA VINCULADA"></Label>
                <Label class="account-date" row="1" text="21.12.2019"></Label>
              </GridLayout>
              <StackLayout width="5%">
                <Image class="icon-left" src="~/assets/images/ic_more_vert_white.png" stretch="none"></Image>
              </StackLayout>
            </FlexboxLayout>
            <FlexboxLayout class="accounts-vinculate">
              <Image width="15%" src="~/assets/images/iconmonstr-twitch-1.png" stretch="none"></Image>
              <GridLayout width="55%" class="status" rows="auto, auto">
                <Label class="status-account innactive" row="0" text="NÃO VINCULADA"></Label>
                <Label class="account-date" row="1" text="--"></Label>
              </GridLayout>
              <StackLayout width="30%">
                <Button text="CONECTAR" class="btn-connect"></Button>
              </StackLayout>
            </FlexboxLayout>
          </StackLayout>
          <FlexboxLayout row="7" class="footer" alignContent="center">
            <StackLayout width="50%">
              <Button text="SALVAR" class="btn-save"></Button>
            </StackLayout>
            <StackLayout width="50%">
              <Button text="CANCELAR" class="btn-cancel"></Button>
            </StackLayout>
          </FlexboxLayout>
        </GridLayout>
      </ScrollView>
    </GridLayout>
  </Page>
</template>

<script>
  import { isAndroid } from "platform";
  import LMActionBar from '~/components/LMActionBar'
  import LMChips from '~/components/LMChips'
  export default {
    components: {
      LMActionBar,
      LMChips
    },
    data: () => ({
      maxactionbarheight: isAndroid ? 50 : 35,
      countries: [
        'Brazil',
        'Argentina',
        'England'
      ],
      states: [
        'Pará',
        'São Paulo',
        'Rio de Janeiro'
      ],
      selectedState: ''
    })
  };
</script>

<style lang="scss" scoped>
.ab-action {
  font-size: 20;
  color: #633280;
}

.input-field {
  margin-bottom: 10;
}

.label-upload {
  vertical-align: center;
  margin-top: 35;
  text-align: center;
  width: 92;
  font-family: "Poppins";
  font-size: 16;
  font-weight: 500;
  font-style: normal;
  color: #ffffff;
}

.label {
  width: 149;
  height: 26;
  border-radius: 13;
  font-family: "Poppins";
  background-color: #633280;
  color: white;
  text-align: center;
  padding: 5;
  margin-bottom: 10;
  margin-top: 10;
  font-size: 14;
  font-weight: 500;
}

.chips:first {
  margin: 0;
}

.label-jogador {
  width: 174;
}

.btn-upload {
  margin-top: 41;
  margin-bottom: 13;
  width: 120;
  height: 120;
  border-radius: 10;
  background-color: #633280;
}

.btn-save {
  padding: 5;
  width: 90;
  height: 30;
  border-radius: 50;
  border-style: "solid";
  border-width: 3;
  border-color: #73af00;
  color: #73af00;
}

.btn-cancel {
  padding: 5;
  width: 116;
  height: 30;
  border-radius: 50;
  border-style: "solid";
  border-width: 3;
  border-color: #dc1543;
  color: #dc1543;
}

.list-picker {
  text-align: left;
}

.input {
  font-size: 13;
  width: 350;
  height: 42;
  font-weight: normal;
  color: rgb(190, 25, 101);
  background-color: white;
  border-radius: 5;
  padding-left: 15;
  border-style: "solid";
  border-width: 2;
  border-color: #633280;
}

.text-area {
  height: 137;
  padding-top: 10;
}

.input-password {
  width: 165;
}

.footer {
  padding: 15;
}

.position {
  padding-left: 5;
}

.accounts {
  padding: 20 10 20 10;
  horizontal-align: center;
  vertical-align: "center";
  .icon-writer {
    padding: 5;
    vertical-align: "center";
    right: 1;
  }

  .btn-connect {
    width: 100;
    height: 25;
    border-radius: 50;
    border-style: "solid";
    border-width: 3;
    border-color: #633280;
    color: #633280;
  }

  .accounts-vinculate {
    margin-top: 15;
  }
  
  .status {
    margin-left: 5;
    padding: 5;
    font-family: "Poppins";
    font-style: normal;
    horizontal-align: center;
    
    .status-account {
      font-size: 13;
      font-weight: 500;
      color: #633280;
    }

    .account-date {
      font-size: 11;
      font-weight: 600;
      line-height: 15;
      color: #d6d6d6;
    }

    .innactive {
      color: #d6d6d6;
    }
  }
}
</style>
