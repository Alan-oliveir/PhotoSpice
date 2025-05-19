# photospice_web

Interface web do sistema PhotoSpice, desenvolvida com Vue 3 em Vite. Esta parte do projeto é responsável por fornecer a interface de usuário para upload de imagens de circuitos, exibição da netlist gerada, configuração de parâmetros de simulação e visualização dos resultados.

## Funcionalidades

- Upload de imagens de circuitos esquemáticos
- Visualização do processamento da imagem e componentes detectados
- Interface para edição da netlist gerada
- Configuração de parâmetros de simulação (ponto de operação ou análise transiente)
- Visualização dos resultados (tensões nodais ou gráficos de tensão/corrente)

## IDE Recomendada

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (e desabilite o Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Configuração Personalizada

Veja a [Referência de Configuração do Vite](https://vitejs.dev/config/).

## Configuração do Projeto

```sh
npm install
```

### Compilação e Hot-Reload para Desenvolvimento

```sh
npm run dev
```

### Compilação e Minificação para Produção

```sh
npm run build
```

## Integração com o Backend

Esta interface web se comunica com o servidor Flask localizado na pasta `server` do projeto. As principais interações incluem:

1. Envio da imagem do circuito para processamento
2. Recebimento da netlist gerada
3. Envio dos parâmetros de simulação
4. Recebimento dos resultados da simulação

## Como Usar

1. Inicie o servidor backend (veja instruções no README da pasta `server`)
2. Inicie a aplicação web com `npm run dev`
3. Acesse a interface pelo navegador (geralmente em http://localhost:5173)
4. Faça upload da imagem do circuito
5. Após a análise, verifique e edite a netlist se necessário
6. Escolha o tipo de simulação (ponto de operação ou análise transiente)
7. Para análise transiente, configure os parâmetros de tempo e selecione os componentes/nós para visualização
8. Visualize os resultados da simulação
