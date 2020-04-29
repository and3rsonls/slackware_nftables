<p align="center"><img src="https://i.imgur.com/K7SLZM9.png" width="700"/></p>

## [pt](#pt)-[en](#en)
# Slackware 14.2 Linux nftables
#### O nftable é nativo na instalação do Slackware 14.2 <a name="pt"></a>
```
# mv -v nftables.conf /etc/nftables/
  - copiar ou mover o nftables.conf (arquivo de configuração) para "/etc/nftables/"
```
```
# chmod +x /etc/nftables/nftables.conf
  - mudando as permissões
```
```
# mv -v rc.nftables /etc/rc.d/
  - copiar ou mover o rc.nftables (arquivo de inicialização) para "/etc/rc.d/"
```
```
# chmod +x /etc/rc.d/rc.nftables
  - tornar o script executável durante a inicialização
```
```
# vim /etc/rc.d/rc.inet2
	|   if [ -x /etc/rc.d/rc.nftables ]; then
	|     /etc/rc.d/rc.nftables start
	|   fi
  - adicione as linhas acima em "/etc/rc.d/r.inet2" para a inicialização durante o boot
```
<p align="center"><img src="https://i.imgur.com/lemKfiW.jpg" width="150"/></p>

## [en](#en)-[pt](#pt)
#### nftable is native to Slackware 14.2 installation <a name="en"></a>
```
# mv -v nftables.conf /etc/nftables/
   - copy or move nftables.conf (configuration file) to "/etc/nftables/"
```
```
# chmod + x /etc/nftables/nftables.conf
   - changing permissions
```
```
# mv -v rc.nftables /etc/rc.d/
   - copy or move rc.nftables (initialization file) to "/etc/rc.d/"
```
```
# chmod + x /etc/rc.d/rc.nftables
   - make the script executable at startup
```
```
# vim /etc/rc.d/rc.inet2

	| if [-x /etc/rc.d/rc.nftables]; then
	| /etc/rc.d/rc.nftables start
	| fi
   - add the lines above in "/etc/rc.d/r.inet2" for boot-up
```
##### Slackware® is a registered trademark of [Patrick Volkerding](http://slackware.com/trademark/trademark.php), Inc. All logos and graphics are copyrighted.
##### Linux® is a registered trademark of Linus [Torvalds](http://www.linuxmark.org/)
