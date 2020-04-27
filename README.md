# Slackware 14.2 Linux nftables
#### O nftable é nativo na instalação do Slackware 14.2<br>
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
