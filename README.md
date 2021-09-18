# Roteiro instalação debian 11.0.0 usando o VirtualBox

## **1ª Etapa configuração Máquina Virtual**
- 1. Este tutorial presume que você tenha o [VirtualBox] (https://www.virtualbox.org/) já instalado.
- 1. Clique no link [debian.org](https://cdimage.debian.org/debian-cd/current/arm64/iso-dvd/debian-11.0.0-arm64-DVD-1.iso)  para fazer o download da versão 11.0.0, que é a versão stable na data de confecção deste roteiro
- 2. Terminado o download da iso abra o virtual box,  **Clique em novo**, escreva um nome, escolha a pasta onde será salvo os arquivos da máquina ou deixe o padrão, mude o tipo para linux e a para versão debian x64. ![image](img/1.png)![image](img/2.png)
- 3. Clique em próximo, coloque a ram em 4096mb  ![image](img/3.png)
- 4. Clique em próximo, marque a opção **criar um novo disco rigído virtual agora** e clique em criar![image](img/4.png)
- 5. Continue o processo de criação, marque a opção VDI (Virtual Disk Image) e clique em próximo.<br />![image](img/5.png)
- 6. Marque a opção Dinamicamente alocado e clique em próximo.<br />![image](img/6.png)
- 7. Selecione o tamanho da imagem de disco virtual entre 20G a 40GB <br />![image](img/7.png)
- 8. Após a máquina virtual ter sido criada clique em **configurações** e selecione a **ISO do debian** que você fez o download e **clique em abrir** <br />![image](img/8.png)![image](img/8-1.png)![image](img/8-2.png)![image](img/8-3.png)
- 9. Agora clique em iniciar para ligar a máquina virtual ![image](img/9.png)
## **Instalação da Distro do Debian 11 na máquina virtual**
- 1. Selecione a forma que você prefere que a instalação ocorra iremos usar a **Graphical install** <br />![image](img/10-1.png)
- 2. Nos próximos passos você irá configurar linguagem. localidade e teclado da distro
     - 2.1 Selecionar a linguagem da instalação
    ![image](img/10-2.png)
     - 2.2 Selecionar sua localidade (País) para configurar o fuso horário 
    ![image](img/10-3.png)
     - 2.3 Selecionar a configuração do teclado
    ![image](img/10-4.png)
- 3.  Clique em continue e aguarde o instalador carregar os componentes de instalação e configuração dos componentes de rede.
- 4.  Agora defina o hostname no exemplo foi definido **server-isw**, você pode por qualquer um desde que respeite as regras da distro apenas letras minúsculas (a-z), ou maiúsculas (A-Z), numeros de (0-9) e o sinal de hífen(-)
    ![image](img/11.png)
- 5. Defina o nome de dominio do seu servidor "exemplo.com.br"
    ![image](img/12.png)
- 6.  Defina a senha do usuário **root**
    ![image](img/13.png)
- 7. Configure uma conta para tarefas não-administrativas
      - 7.1 Defina o nome completo do usuário
    ![image](img/14.png)
      - 7.2 Defina o nome de usuário
    ![image](img/15.png)
      - 7.3 Defina a senha do usuário
    ![image](img/16.png)
- 8. Configurar o fuso horário do rélogio.
    ![image](img/17.png)
- 9.  Vamos configurar o particionamento de disco 
      - 9.1.  selecione **"Assitido - usar o disco inteiro"**
    ![image](img/18.png)
      - 9.2.  Selecione o disco que será particionado
    ![image](img/19.png)
      - 9.3 Selecione o esquema de particionamento **Todos os arquivos em uma partição ( para iniciantes )**
    ![image](img/20.png)
      - 9.4 Confirme o particionamento do disco marque a opção **Finalizar o particionamento e escrever as mudanças no disco**
    ![image](img/21.png)
      - 9.5 Confirme clicando em **SIM** para escrever as mudanças no disco que será particionado e continue
    ![image](img/22.png)
- 14.  Agora vamos configurar o gerenciador de pacotes
        - 14.1 Como não temos midias adicionais para serem lidas podemos marcar **NÃO** e continuar.
        ![image](img/23.png)
        - 14.2 Marque a opção **SIM** para usar um espelho da rede
        ![image](img/24.png)
        - 14.3 Selecione o espelho do repositório de você no nosso caso o **BRASIL** 
        ![image](img/25.png)
        - 14.4 Selecione o endereço espelho do repositório Debian normalmente é usado o padrão **deb.debian.org**
        ![image](img/26.png)
        - 14.5 Se você usar **proxy** para acessar internet informe-o nessa tela **se não deixe em branco**
        ![image](img/27.png)
- 15. Configurando popularity-contest para enviar informações sobre os pacotes mais utilizados para o desenvolvedores da distro, para esse roteiro iremos selecionar **NÃO**.
- 16. Selecionar os softwares que irão ser instalados no momento da instalação da distro, como podemos instalar após a instalação vamos selecionar apenas as opções **ambiente de área de trabalho no Debian** e **utilitários de sistema padrão** ![image](img/28.png)
- 17. Vamos instalar o **carregador de inicialização GRUB**, 
        - 17.1 Marque **SIM** e clique em continuar ![image](img/29.png)
        - 17.2 Selecionar o dispositivo que será instalado o GRUB ![image](img/30.png)
- 18. Após o passo anterior a instalação está completa, o sistema irá reinicializar ![image](img/31.png)
- 19. Na tela do GRUB selecione a opção **Debian GNU/Linux** ![image](img/32.png)


## **Instalação concluida com sucesso**
![image](img/33.png)
