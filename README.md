# Redux Saga + Reactotron setup

## Reactotron

O Reactotron é uma ótima ferramente para debugar projetos que usam Redux e Saga

### Setup

- Instalação: ```yarn add reactotron-react-js```

- Arquivo de configuração ([src/config/ReactotronConfig.js](src/config/ReactotronConfig.js)):

```js
import Reactotron from 'reactotron-react-js';

if (process.env.NODE_ENV === 'development') {
    const tron = Reactotron.configure().connect();

    tron.clear();

    console.tron = tron;
}
```

- importar arquivo de configuuração no [App.js](src/App.js)

```js
import './config/ReactotronConfig';
```

Feito isso, é esperado que o Reacotron consiga se conectar com a aplicação em ambiente de desenvolvimento

![Reactotron Connection](images/reactotron_connection.png)
___