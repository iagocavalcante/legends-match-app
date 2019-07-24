<template>
  <FlexboxLayout class="page">
    <StackLayout class="form">
      <FlexboxLayout alignContent="center" class="header">
        <Label alignSelf="center" class="header-legend" text="LEGENDS"></Label>
        <Label alignSelf="center" class="header-match" text="MATCH"></Label>
      </FlexboxLayout>

      <GridLayout rows="auto, auto, auto">
        <StackLayout row="0" class="input-field">
          <TextField class="input" hint="E-mail"
            keyboardType="email" autocorrect="false"
            autocapitalizationType="none"
            ></TextField>
          <StackLayout class="hr-light"></StackLayout>
        </StackLayout>

        <StackLayout row="1" class="input-field">
          <TextField class="input" ref="password"
            hint="Senha" secure="true"
            ></TextField>
          <StackLayout class="hr-light"></StackLayout>
        </StackLayout>

        <!-- <ActivityIndicator rowSpan="3" :busy="processing"></ActivityIndicator> -->
      </GridLayout>

      <Button text="ENTRAR" class="btn-login btn-primary"></Button>
      <Label text="Esqueceu a senha ? Clique aqui!"
        class="login-label"></Label>
    </StackLayout>

    <Button text="CADASTRE-SE" @tap="$navigateTo(register)" class="btn-signup btn-primary"></Button>
    <!-- <Label class="login-label sign-up-label">
      <FormattedString>
        <Span text="Don’t have an account?"></Span>
      </FormattedString>
    </Label> -->
  </FlexboxLayout>
</template>

<script>
  import Register from './Register'
  export default {
    data: () => ({
      register: Register
    }) 
  };
</script>

<style lang="scss" scoped>
  .page {
    align-items: center;
    flex-direction: column;
    background: rgb(220, 21, 67);
    background: linear-gradient(180deg, rgba(227,36,36,69) 0%, rgba(190,25,121,101) 35%, rgba(99,50,128,1) 100%);
  }

  .form {
    margin-left: 30;
    margin-right: 30;
    flex-grow: 2;
    vertical-align: middle;
  }

  .logo {
    margin-bottom: 12;
    height: 90;
    font-weight: bold;
  }

  .btn-login {
    width: 165;
    height: 35;
    border-radius: 50;
    background-color: #30024b;
    color: white;
    font-family: "Poppins";
    font-size: 16;
    font-weight: "500";
  }

  .btn-signup {
    width: 169;
    font-family: "Poppins";
    font-size: 16;
    font-weight: "500";
    height: 35;
    border-radius: 50;
    border-style: "solid";
    border-width: 3;
    color: #ffffff;
    border-color: #ffffff;
  }

  .header {
    horizontal-align: center;
    padding-bottom: 70;
    color: #ffffff;
    font-size: 36;
    height: 51;
    .header-legend {
      font-weight: 300;
    }
    .header-match {
      font-weight: 700;
    }
  }

  .input-field {
    margin-bottom: 10;
  }

  .input {
    font-size: 13;
    width: 349;
    height: 42;
    font-weight: "normal";
    color: rgb(190, 25, 101);
    background-color: white;
    border-radius: 5;
    padding-left: 15;
  }

  .input:disabled {
    background-color: white;
    opacity: 0.5;
  }

  .btn-primary {
    margin: 20 5 15 5;
  }

  .login-label {
    horizontal-align: center;
    color: #ffffff;
    font-size: 12;
  }

  .sign-up-label {
    margin-bottom: 20;
  }

  .bold {
    color: #000000;
  }
</style>
