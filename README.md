# Firebase-Auth-Vue

Criando uma aplicação Vue.js com o sistema de autenticação Firebase

## Project setup

Para rodar o projeto é necessário ter instalado a ferramenta Vue CLI no seu computador.

Para isso abra o cmd na pasta raiz e execute o seguinte comando 
```
npm install -g @vue/cli
```

Agora dentro da pasta do projeto rode o seguinte comando para instalar os pacotes necessários
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Adicionar o Firebase ao projeto

Crie um projeto no firebase e copie as informações geradas do SDK. 
Depois abra a pasta main.js e substitua o firebaseConfig pelo atual

```
   var firebaseConfig = {
    apiKey: "",
    authDomain: "",
    databaseURL: "",
    projectId: "",
    storageBucket: "",
    messagingSenderId: "",
    appId: ""
  };
```











