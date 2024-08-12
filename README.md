Documentação do Componente App
Descrição

O componente App é uma aplicação React Native simples que alterna a exibição de duas imagens (symbol-on.png e symbol-off.png) com base em um estado booleano. Quando o usuário toca no símbolo, o estado isActive é alternado, o que altera a imagem exibida e o estilo de fundo da tela.
Importações

javascript

import React, { useState } from 'react';
import { StyleSheet, Text, View, Image, TouchableOpacity } from 'react-native';
import symbolOn from './assets/symbol-on.png';
import symbolOff from './assets/symbol-off.png';

    React: Biblioteca principal para criar componentes React.
    useState: Hook do React para gerenciar o estado dentro de um componente funcional.
    StyleSheet, Text, View, Image, TouchableOpacity: Componentes e funções do React Native para construção da interface e estilos.
    symbolOn e symbolOff: Importações das imagens que serão exibidas com base no estado.

Componente App
Estado

    isActive: Um estado booleano que determina se o símbolo está ativo ou não. Inicialmente definido como false.

Métodos

    handleSymbol: Alterna o valor de isActive entre true e false. Também imprime o valor atual de isActive no console.

Renderização

    O componente renderiza uma View com um estilo que muda com base no estado isActive.
    Um TouchableOpacity envolve um componente Image. A imagem exibida depende do estado isActive:
        Se isActive for true, a imagem symbolOn é exibida.
        Se isActive for false, a imagem symbolOff é exibida.
    O TouchableOpacity chama a função handleSymbol quando pressionado.

Estilos

    containerOn:
        flex: 1: O componente ocupa todo o espaço disponível.
        backgroundColor: 'black': Define a cor de fundo como preta.
        alignItems: 'center': Alinha os itens horizontalmente ao centro.
        justifyContent: 'center': Alinha os itens verticalmente ao centro.

    containerOff:
        flex: 1: O componente ocupa todo o espaço disponível.
        backgroundColor: '#ffffff': Define a cor de fundo como branca.
        alignItems: 'center': Alinha os itens horizontalmente ao centro.
        justifyContent: 'center': Alinha os itens verticalmente ao centro.

Uso

Para usar este componente, certifique-se de que você tem as imagens symbol-on.png e symbol-off.png na pasta assets. Importe e use o componente App em seu arquivo principal, geralmente App.js ou index.js.
Exemplo de Uso

javascript

import React from 'react';
import { SafeAreaView } from 'react-native';
import App from './App';

export default function Main() {
  return (
    <SafeAreaView style={{ flex: 1 }}>
      <App />
    </SafeAreaView>
  );
}
