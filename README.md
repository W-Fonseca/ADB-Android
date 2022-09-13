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

<H2> Comandos ADB </H2>

<ul>
  <li>Conexão por IP</li>
  </ul>
  
```diff
adb Connect <ip do dispositivo>
```
<ul>
  <li>Conexão por usb</li>
  </ul>
  
```diff
adb usb
```
<ul>
  <li>Montar conexão com porta 5555</li>
  </ul>
  
```diff
adb tcpip 5555
```
<ul>
  <li>Desconectar de todos os dispositivos</li>
  </ul>
  
```diff
adb kill-server
ou 
adb disconnect
```
<ul>
  <li>Mostrar todas as conexões</li>
  </ul>
  
```diff
adb devices
```

<ul>
  <li>Remonta o sistema</li>
  </ul>
  
```diff
adb remount
```
<ul>
  <li>Reiniciar o sistema</li>
  </ul>
  
```diff
adb reboot
```
<ul>
  <li>Reiniciar no modo recuperação</li>
  </ul>
  
```diff
adb reboot recovery
```
<ul>
  <li>Reiniciar no modo bootloader</li>
  </ul>
  
```diff
adb reboot bootloader
```
<ul>
  <li>Reiniciar no modo fastboot</li>
  </ul>
  
```diff
adb reboot fastboot
```

<ul>
  <li>enviar arquivos para uma pasta</li>
  </ul>
  
```diff
adb push c:/pasta/arqivo.apk /system/preinstall
```
<ul>
  <li>copiar um arquivo para o pc</li>
  </ul>
  
```diff
adb pull c:/pasta/arqivo.apk /system/preinstall
```
<ul>
  <li>Instalar um Aplicativo</li>
  </ul>
  
```diff
adb install c:/pasta/arqivo.apk 
```

<ul>
  <li>enviar comandos em um determinado celular, caso ter mais de um celular conectado</li>
  </ul>
  
```diff
adb -s ip:5555 remount
```
---------------
<H2>Comandos em terminal</H2>

<ul>
  <li>Remonta o sistema</li>
  </ul>
  
```diff
adb shell mount -o rw,remount /
```
<ul>
  <li>Cria uma pasta(exemplo pasta SuperSU)</li>
  </ul>
  
```diff
adb shell mkdir /system/app/SuperSU
```

<ul>
  <li>remove uma pasta(exemplo pasta SuperSU)</li>
  </ul>
  
```diff
adb shell rmdir /system/app/SuperSU
```

<ul>
  <li>força a remoção de uma pasta mesmo que contenha coisas dentro(exemplo pasta SU)</li>
  </ul>
  
```diff
adb shell rm -f /system/bin/su
```
<ul>
  <li>Limpando arquivos temporarios(exemplo pasta System)</li>
  </ul>
  
```diff
adb shell rm -fR data/local/tmp/system/
```
<ul>
  <li>Forçar apagar uma pasta</li>
  </ul>
  
```diff
adb shell rm -fr data/local/tmp/system/Preinstall
```
<ul>
  <li>Detalhes do espaço do disco</li>
  </ul>
  
```diff
adb shell df
```

<ul>
  <li>Espaço em disco usado pelos arquivos e subdiretórios especificados</li>
  </ul>
  
```diff
adb shell du
```
<ul>
  <li>Detalhes do espaço em disco no formato KB/MB</li>
  </ul>
  
```diff
adb shell df -h
```

<ul>
  <li>Espaço em disco usado pelos arquivos e subdiretórios especificados no formato KB/MB</li>
  </ul>
  
```diff
adb shell du -h
```

<ul>
  <li>Para detalhes específicos do espaço da pasta</li>
  </ul>
  
```diff
adb shell df /sistema
```

<ul>
  <li>Para detalhes específicos do espaço da mesa de pastas e subsatratos</li>
  </ul>
  
```diff
adb shell du /sistema
```
