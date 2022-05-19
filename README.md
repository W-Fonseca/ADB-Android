# ADB-Android

Documentação de utilização do terminal shell do android

<H2>Instalação Linux</h2>
<h3> Distribuições Debian</h3>
sudo apt-get install android-tools-adb
<h3> Distribuições Fedora</h3>
sudo yum install android-tools
<H2>Instalação Windows</h2>
passo a passo
https://www.showmetech.com.br/aprenda-instalar-usar-adb-do-android-windows/

<H2> Comandos Basicos </H2>

<ul>
  <li>Desconectar de todos os dispositivos</li>
  </ul>
  
```diff
adb kill-server
```
<ul>
  <li>Listar todas as partições</li>
  </ul>
  
```diff
adb shell df
```
