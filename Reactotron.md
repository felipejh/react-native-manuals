# Reactotron

Instalar o Reactotron neste link ``` https://github.com/infinitered/reactotron/releases ```

Instalar a dependência no projeto ```yarn add reactotron-react-native```

Criar o arquivo ```/src/config/ReactotronConfig.js```

```
import Reactotron from 'reactotron-react-native';

if (__DEV__) {
  const tron = Reactotron.configure()
    .useReactNative()
    .connect();

  console.tron = tron;

  tron.clear();
}
```

import './config/ReactotronConfig';

Caso utilize um dispositivo físico por USB, talvez precise passar um objetov ```host``` com o número IP do seu computador dentro do parâmetro ```configure({ host: 192.168.0.4})```