# Guia de Instalação do AgroMart Mobile

O **AgroMart Mobile** é um aplicativo desenvolvido em **React Native** com **Expo** e **TypeScript**, projetado para ser **multiplataforma** (Android e iOS).  

Este guia descreve os requisitos e o processo de instalação para executar o projeto em ambiente local.

---

## Pré-requisitos

Antes de iniciar, certifique-se de ter os seguintes itens configurados:

- **Node.js** (versão recomendada: LTS 18 ou superior)  
- **Yarn** (gerenciador de pacotes)  
- **Expo CLI** – instale globalmente:  

```bash
  npm install -g expo-cli
```

Emulador Android Studio ou o aplicativo Expo Go (disponível na Play Store/App Store)

AgroMart API rodando localmente ou em ambiente remoto (necessário para fornecer os dados ao aplicativo)

!!! note "Importante"
    A API deve estar configurada e acessível antes de iniciar o aplicativo mobile, pois o sistema consome dados diretamente dela.

---

## Clonando o Repositório
Clone o repositório oficial do AgroMart Mobile e acesse a pasta do projeto:

```bash
git clone https://github.com/AgroMart/mobile-client
cd mobile-client
```

---

## Instalando Dependências
Com o projeto dentro da pasta, instale as dependências com:

```bash
yarn install
```

Isso instalará todas as bibliotecas necessárias, incluindo React Native, Expo, e integrações do projeto.

!!! tip "Dica"
    Caso o Yarn não esteja instalado, você pode adicioná-lo com:
    ```bash 
    npm install -g yarn
    ```

---

## Executando o Projeto
Para iniciar o servidor de desenvolvimento, use:

```bash
yarn start
```
Esse comando abrirá o Expo DevTools no navegador.
A partir dele, você pode:

- Ler o QR Code com o aplicativo Expo Go (Android/iOS) para rodar em um dispositivo físico;

- Rodar no emulador Android configurado via Android Studio;

- Rodar no simulador iOS (disponível apenas em macOS com Xcode instalado).

---

## Repositório Oficial
Você pode acessar o código-fonte completo do projeto diretamente no GitHub:

> Repositório oficial: [AgroMart Mobile no GitHub](https://github.com/AgroMart/mobile-client)