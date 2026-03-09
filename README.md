# 📦 Inventário Automatizado de Computadores via Active Directory
Ferramenta desenvolvida em PowerShell para coletar automaticamente informações de computadores presentes em uma OU de loja dentro do Active Directory, gerando um relatório de inventário em CSV.

O script permite que o técnico informe o número da loja, localize automaticamente a OU correta no AD e extraia dados relevantes das máquinas.

🎯 Objetivo
-----------------------------------------------------------------------------------------------------------------------
Facilitar o levantamento de inventário de equipamentos em filiais ou lojas, automatizando a coleta de informações como:

- Hostname
- Número de série
- Modelo do equipamento
- Sistema operacional
- Data do último logon ou da máquina no Active Directory

🖥️ Tecnologias utilizadas
---------------------------------------------------------------------------------
- PowerShell
- Active Directory Module (RSAT)
- WMI / CIM
- PS2EXE (opcional para geração de executável)

📂 Estrutura do Projeto
---------------------------------------------------------------------------------
```
 inventario-ad-lojas
 │
 ├─ Inventario-Loja.ps1     # Script principal
 ├─ Inventario-Loja.bat     # Launcher para execução facilitada
 ├─ README.md               # Documentação do projeto
```
⚙️ Requisitos
--------------------------------------------------------------------------------------
Para executar o script é necessário:

- Windows 10 / 11 ou Windows Server
- PowerShell 5+
- RSAT instalado
- Módulo ActiveDirectory
- Permissão de leitura no Active Directory
- Permissão de consulta remota nas máquinas (WMI / CIM)

🚀 Como usar
-----------------------------------------------------------------------------------
## 1️⃣ Baixar o projeto
### Clone o repositório:
> git clone https://github.com/seuusuario/inventario-ad-lojas.git
Ou faça download do ZIP.
________________________________________________
## 2️⃣ Executar o script
### Execute o arquivo:
> `#97119c`Inventario-Loja.bat
Ou diretamente via PowerShell:
> `#97119c` .\Inventario-Loja.ps1
_________________________________________________
## 3️⃣ Informar a loja
O sistema solicitará o número da loja:

> Digite o numero da loja (ex: 15)

O script irá:
- Localizar a OU da loja no AD
- Buscar todos os computadores
- Coletar informações do hardware
- Gerar o relatório automaticamente

📊 Saída do sistema
---------------------------------------------
Será gerado um arquivo CSV em:
> C:\Temp\

Exemplo:
> Inventario_Loja_15_20260309.csv

## Campos gerados:

```Descrição
Hostname
Serial Number
Número de série do equipamento
Modelo 
Sistema Operacional
Ultimo Logon
Unidade organizacional da loja
```

⚠️ Tratamento de erros
`Caso alguma máquina esteja offline ou inacessível:
O inventário continua normalmente
A máquina será marcada como Offline
Um arquivo .log pode ser gerado com os erros`

🔐 Permissões necessárias

Para funcionamento correto:
[✅]Permissão de leitura no Active Directory
[✅]Acesso WMI/CIM às máquinas do domínio
[✅]Firewall permitindo comunicação remota

📦 Gerar versão executável (.EXE)
- Opcionalmente o script pode ser convertido para .exe utilizando PS2EXE:

> Install-Module ps2exe
>Invoke-ps2exe Inventario-Loja.ps1 Inventario-Loja.exe

📌 Possíveis melhorias futuras
-------------------------------------------------------------------------------------------------------
- Interface gráfica (GUI)
- Inventário de memória RAM
- Inventário de disco
- Exportação para Excel
- Integração com GLPI / CMDB
- Execução paralela para maior velocidade


_____________________________________________________________________
👨‍💻 Autor
Felipe Silva
Analista / Técnico de TI
_____________________________________________________________________
📄 Licença
Este projeto é distribuído para fins educacionais e de automação de infraestrutura de TI.
