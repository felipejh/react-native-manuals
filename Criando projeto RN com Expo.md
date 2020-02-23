# Criando projeto Mobile com Expo e UI KItten

## Expo

#### Instalar o Expo CLI de maneira global

``` 
yarn add global expo-cli
``` 

#### Adicionar o *expo* ao *PATH*

1. Abrir o arquivo ```.zshrc```

    ``` sudo nano ˜/.zshrc ```

2. Adicionar a seguinte linha, no final:

    ```export PATH="$(yarn global bin):$PATH"``` 

> Mais informações podem ser acessadas através do link [Yarn Global](https://legacy.yarnpkg.com/lang/en/docs/cli/global/)

## Criando o projeto

1. #### Acessar a pasta do projeto e executar o comando abaixo
    ``` expo init mobile ``` 

2. #### Entrar na pasta do projeto criado
    ``` cd mobile ``` 

3. #### Instalar o UI Kitten

    ``` yarn add react-native-svg ```

    ``` yarn add @ui-kitten/components ``` 

    ``` yarn add @eva-design/eva ```

4. #### Abrir o projeto no VSCode
    ``` code . ```

5. #### Neste momento já podemos iniciar o App com o seguinte comando:
    ```yarn start ```

## Alterando a fonte do aplicativo

1. #### Baixar a fonte [Roboto](https://fonts.google.com/specimen/Roboto)


Navegação entre páginas -> [React Navigation](https://docs.expo.io/versions/v36.0.0/guides/routing-and-navigation/)
yarn add react-navigation

expo install react-native-gesture-handler react-native-reanimated react-native-screens react-native-safe-area-context

yarn add react-navigation-stack @react-native-community/masked-view react-native-safe-area-context


START app

yarn install
yarn add expo
"start": "expo start", -> "start": "npm run env -- prod && expo start -c",