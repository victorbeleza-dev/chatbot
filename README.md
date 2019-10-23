# chatbot-kotlin-dialogflow
Aplicativo de bate-papo para Android criado com Kotlin e Pusher que integra uma construção de chatbot ao Dialogflow. Siga o tutorial [aqui](https://pusher.com/tutorials/chatbot-kotlin-dialogflow).

## Vamos Começar

1. Clone o repostitório.
2. Crie uma conta no [Pusher app](https://dashboard.pusher.com).
3. Insira as informações do seu aplicativo Pusher dentro `server/src/main/kotlin/com/pusher/chatbotapi/MessageController.kt` e dentro `android/app/src/main/java/com/pusher/chatbot/ChatActivity.kt`.
4. Crie um agente do [Dialogflow agent](https://console.dialogflow.com/api-client) e configure-o seguindo as etapas do tutorial ou importando o arquivo zip `TriviaBot.zip` na raiz deste repositório usando a opção Exportar e Importar na página Configurações do seu agente.
5. Na seção Geral da página *Configurações* , copie a ID do projeto e insira-a na classe `server/src/main/kotlin/com/pusher/chatbotapi/MessageController.kt`.
6. Vá para o [Google Cloud Platform console](https://console.cloud.google.com/home/dashboard), escolha o projeto criado para o seu agente Dialogflow, crie uma nova chave de conta de serviço na seção APIs e serviços > Credenciais como um arquivo JSON e faça o download do arquivo para um diretório fora deste projeto.
7. Configure a variável de ambiente `GOOGLE_APPLICATION_CREDENTIALS` e defina como valor o local do arquivo JSON que contém a chave privada que você criou na etapa anterior.
8. Em uma janela do terminal, vá para o `server` diretório e execute  `gradlew bootRun` para iniciar o servidor.
9. Em uma janela de terminal nesse diretório e execute `ngrok http localhost:8080` para expor seu servidor local ao mundo.
10. Copie o URL de encaminhamento HTTPS, algo como https://5a4f24b2.ngrok.io .
11. No console do Dialogflow, clique na opção Cumprimento , ative a opção Webhook e adicione a URL que você acabou de copiar do ngrok, anexando o caminho do nó de extremidade do webhook (`webhook`).
12. Abra o aplicativo com o Android Studio.
13. Crie o projeto e execute-o em dois emuladores.
14. Escolha um nome de usuário e comece a enviar mensagens

### Prerequisitos

- [Android Studio 3.1.4](https://developer.android.com/studio/index.html)
  - MinSdkVersion: 15
  - TargetSdkVersion: 27
  - buildToolsVersion: 27.1.1
- [Pusher account](https://pusher.com/signup)
- [Dialogflow (Google) account](https://console.dialogflow.com/api-client/#/login)
- [ngrok](https://ngrok.com/)

## Construido com

* [Pusher](https://pusher.com/) - APIs to enable devs building realtime features
* [Dialogflow](https://dialogflow.com/) A Google-owned developer of human–computer interaction technologies based on natural language conversations

## Agradecimentos
* Obrigado a [Pusher](https://pusher.com/) pelo tutorial.

## LICENSE
MIT
