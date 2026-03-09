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
PowerShell
Active Directory Module (RSAT)
WMI / CIM
PS2EXE (opcional para geração de executável)

📂 Estrutura do Projeto
---------------------------------------------------------------------------------
inventario-ad-lojas
│
├─ Inventario-Loja.ps1     # Script principal
├─ Inventario-Loja.bat     # Launcher para execução facilitada
├─ README.md               # Documentação do projeto

⚙️ Requisitos
--------------------------------------------------------------------------------------
Para executar o script é necessário:

Windows 10 / 11 ou Windows Server
PowerShell 5+
RSAT instalado
Módulo ActiveDirectory
Permissão de leitura no Active Directory
Permissão de consulta remota nas máquinas (WMI / CIM)

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
