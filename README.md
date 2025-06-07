<h1>
  <p align="center" width="100%">
    <img width="30%" src="https://softex.br/wp-content/uploads/2024/09/EmbarcaTech_logo_Azul-1030x428.png">
  </p>
</h1>

# ✨Tecnologias
Esse projeto foi desenvolvido com as seguintes tecnologias.
- Placa Raspberry Pi Pico W
- Raspberry Pi Pico SDK
- C/C++

# 💻Projeto
Projeto Desenvolvido durante a residência em microcontrolados e sistemas embarcados para estudantes de nível superior ofertado pela CEPEDI e SOFTEX, polo Juazeiro-BA, na Universidade Federal do Vale do São Francisco (UNIVASF), que tem como objetivo simular o controle de uma lâmpada inteligente por Wi-Fi utilizando a placa BitDogLab com Raspberry PI-Pico, e fortalecer o aprendizado sobre IOT na plataforma supracitada.

# 🚀Como rodar
### **Softwares Necessários**
1. **VS Code** com a extensão **Raspberry Pi Pico** instalada.
2. **CMake** e **Ninja** configurados.
3. **SDK do Raspberry Pi Pico** corretamente configurado.

### **Clonando o Repositório**
Para começar, clone o repositório no seu computador:
```bash
git clone https://github.com/DevMaic/MQTT-Smart_Light
cd MQTT-Smart_Light
```
---


### **Execução na Placa BitDogLab**
### **1. Substituindo nome e senha da rede Wi-Fi**
1. Substitua no cabeçalho do arquivo `mqtt_client.c` o nome da sua rede Wi-Fi 2.4Ghz e a senha da mesma.
2. Substitua também o ip do seu server MQTT, junto com o nome do host e senha
#### **2. Upload de Arquivo `mqtt_client.uf2`**
1. Importe o projeto utilizando a extensão do VSCode, e o compile.
2. Abra a pasta `build` que será gerada na compilação.
3. Aperte o botão **BOOTSEL** no microcontrolador Raspberry Pi Pico W.
4. Ao mesmo tempo, aperte o botão de **Reset**..
5. Mova o arquivo `mqtt_client.uf2` para a placa de desenvolvimento.
#### **4. Acompanhar Execução do Programa**
1. No aplicativo IoT MQTT Panel, crie um botão e o inscreva no tópico /led com payload "on" e "off"
2. Ainda no aplicativo crie um slider que vai de 0 a 100, e o inscreva no tópico /pwm.
3. Pressione o botão de ligar e desligar luz no aplicativo, o led na parte de trás da BitDogLab obedecerá esses comandos como uma lâmpada comum.
4. Mova o slider e veja o led do pino 13 simular por sua vez uma lâmpada inteligente, com diversos níveis de animação.
   