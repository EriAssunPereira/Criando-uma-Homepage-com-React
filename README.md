# Criando-uma-Homepage-com-React

Vamos criar uma homepage com React, utilizando o Chakra UI para estilização e modularizando os componentes. Aqui está um guia detalhado passo a passo:

**Módulo 1: Configuração do Projeto**
Primeiro, crie um novo projeto React usando o Create React App e instale o Chakra UI.

```bash
npx create-react-app homepage-react
cd homepage-react
npm install @chakra-ui/react @emotion/react @emotion/styled framer-motion
```

**Módulo 2: Estrutura de Diretórios**
Organize seu projeto em pastas para componentes, páginas e temas. Por exemplo:

```
/homepage-react
  /src
    /components
    /pages
    /theme
  package.json
```

**Módulo 3: Tema do Chakra UI**
Dentro da pasta `theme`, crie um arquivo para personalizar o tema do Chakra UI.

```javascript
// src/theme/index.js
import { extendTheme } from '@chakra-ui/react';

const theme = extendTheme({
  // Personalize seu tema aqui
});

export default theme;
```

**Módulo 4: Componentes da Homepage**
Crie componentes individuais para cada parte da sua homepage. Por exemplo, um componente de cabeçalho:

```javascript
// src/components/Header.js
import { Box, Flex, Text, Button } from '@chakra-ui/react';

export const Header = () => {
  return (
    <Flex as="header" width="full" align="center" justify="space-between" p={4}>
      <Text fontSize="lg" fontWeight="bold">
        Minha Homepage
      </Text>
      <Box>
        <Button colorScheme="blue" mr={2}>
          Entrar
        </Button>
        <Button colorScheme="green">
          Registrar
        </Button>
      </Box>
    </Flex>
  );
};
```

**Módulo 5: Página Inicial**
Na pasta `pages`, crie um arquivo para a página inicial e use os componentes criados.

```javascript
// src/pages/HomePage.js
import React from 'react';
import { Header } from '../components/Header';
import { ChakraProvider } from '@chakra-ui/react';
import theme from '../theme';

const HomePage = () => {
  return (
    <ChakraProvider theme={theme}>
      <Header />
      {/* Adicione mais componentes aqui */}
    </ChakraProvider>
  );
};

export default HomePage;
```

**Módulo 6: Implementação de Botões de Eventos**
Adicione funcionalidades aos botões, como abrir um modal ou mudar o tema.

```javascript
// Exemplo de botão que abre um modal
<Button onClick={onOpen}>Abrir Modal</Button>

// Exemplo de botão que muda o tema
<Button onClick={toggleTheme}>Mudar Tema</Button>
```

**Módulo 7: Execução e Testes**
Execute o projeto com `npm start` e teste os componentes e eventos implementados.

```bash
npm start
```

Lembre-se de aplicar as propriedades e eventos que você aprendeu durante o curso para enriquecer a interatividade da sua homepage.
