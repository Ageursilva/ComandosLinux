
## Comandos Essenciais do Linux

Aqui está uma lista ampliada de comandos essenciais em Linux, organizados por categoria, com explicações e exemplos para ajudar a entender seu uso.

### 1. **Navegação**
**hostnamectl** - Dados do sistema
 
 
 - **cd**: Muda para um diretório específico.
```
cd /home/user
```
- **ls**: Lista arquivos e diretórios.
```
ls ls -l   # Exibe detalhes dos arquivos ls -a   # Inclui arquivos ocultos
```

- **pwd**: Exibe o diretório atual.
```
pwd
```
### 2. **Manipulação de Arquivos**

- **touch**: Cria um novo arquivo vazio.
```
touch arquivo.txt
```
- **cp**: Copia arquivos ou diretórios.
```
cp arquivo.txt destino/  # Copia arquivo.txt para /destino
```
- **mv**: Move ou renomeia arquivos ou diretórios.
``` 
   mv arquivo.txt novo_nome.txt   # Renomeia arquivo 
   mv arquivo.txt /destino     # Move arquivo para /destino    
```
- **rm**: Remove arquivos.
``` 
rm arquivo.txt rm -r diretorio/    # Remove diretório e todo o seu conteúdo
``` 
### 3. **Manipulação de Diretórios**

- **mkdir**: Cria um novo diretório.
``` 
mkdir novo_diretorio
mv backup meu_backup
``` 
- **rmdir**: Remove um diretório vazio.
``` 
rmdir novo_diretorio
``` 
### 4. **Visualização de Arquivos**
- **cat**: Exibe o conteúdo de um arquivo.
``` 
cat arquivo.txt
``` 
- **less**: Exibe o conteúdo de um arquivo com rolagem.
``` 
less arquivo.txt
``` 
- **head**: Exibe as primeiras linhas de um arquivo.
``` 
head -n 10 arquivo.txt   # Exibe as 10 primeiras linhas
``` 
- **tail**: Exibe as últimas linhas de um arquivo.
``` 
tail -n 10 arquivo.txt   # Exibe as 10 últimas linhas
``` 
### 5. **Pesquisa**

- **grep**: Busca um padrão em um arquivo.
``` 
grep "padrão" arquivo.txt
``` 
- **find**: Localiza arquivos e diretórios no sistema.
``` 
find /caminho -name "arquivo.txt"
``` 
### 6. **Gerenciamento de Pacotes**
- **apt** (Debian/Ubuntu): Gerenciador de pacotes para instalar, atualizar e remover software.
```
sudo apt update        # Atualiza a lista de pacotes 
sudo apt install nome_pacote #Instala um pacore
apt list --installed #Mostra pacores intalados

sudo apt remove nome_pacote #Remove um pacote
``` 
- **yum** (CentOS/RHEL) e **dnf** (Fedora): Gerenciadores de pacotes para sistemas baseados em Red Hat.
``` 
sudo yum install nome_pacote sudo dnf install nome_pacote
``` 
### 7. **Gerenciamento de Processos**
- **ps**: Exibe processos em execução.
``` 
ps aux
``` 
- **top**: Monitora processos em tempo real.
``` 
top
``` 
- **kill**: Encerra um processo com um ID específico.
``` 
kill 1234   # Encerra o processo com ID 1234
``` 
### 8. **Ajuda**
- **man**: Abre o manual de um comando.
``` 
man ls
``` 
- **--help**: Exibe as opções de um comando específico.
 ``` 
ls --help
``` 
### 9. **Outros Comandos Úteis**
- **echo**: Exibe uma linha de texto no Terminal ou redireciona para um arquivo.
``` 
echo "Olá, Linux!" > saudacao.txt
```  
- **history**: Exibe o histórico de comandos usados.
``` 
history
``` 
- **clear**: Limpa a tela do Terminal.
``` 
clear
``` 
- **chmod**: Altera permissões de um arquivo.
``` 
chmod 755 arquivo.txt   # Permissões de leitura/escrita/execução
``` 
- **df**: Exibe o uso de disco.
``` 
df -h
``` 
- **du**: Mostra o uso de espaço por diretório.
``` 
du -sh /diretorio
``` 
## 10. **Gerenciamento de Usuários e Grupos**
- **adduser** / **useradd**: Cria um novo usuário.
```sudo adduser nome_usuario
Ver user cat /etc/passwd
```
- **passwd**: Altera a senha de um usuário.
```
sudo passwd nome_usuario
```
- **usermod**: Modifica um usuário (ex: adiciona o usuário a um grupo).
```
sudo usermod -aG grupo nome_usuario   # Adiciona o usuário ao grupo
```
- **groups**: Exibe os grupos de um usuário.

```
groups nome_usuario
```
Alterar nome do usuario
```
sudo usermod -l novo_nome_usuario nome_atual_usuario
```
Deletar usuario
```
sudo userdel nome_do_usuario
```
### 11. **Permissões de Arquivos**
- **chown**: Altera o dono de um arquivo ou diretório.
```
sudo chown nome_usuario arquivo.txt   # Altera o dono para nome_usuario 
```
- **chmod**: Altera as permissões de leitura, escrita e execução.
```
chmod 644 arquivo.txt   # Permissões de leitura e escrita para o dono, e leitura para os outros
```
### 12. **Compactação e Descompactação**
- **tar**: Arquiva e comprime arquivos.
```
tar -czvf arquivo.tar.gz /caminho/diretorio   # Cria um arquivo tar.gz compactado
```
- **unzip**: Descompacta arquivos ZIP.
```
unzip arquivo.zip
```
### 13. **Rede e Conectividade**
- **ping**: Verifica a conectividade com outro host.
```
ping google.com
```
- **ifconfig** / **ip**: Exibe informações sobre as interfaces de rede.
```
ifconfig
```
- **curl**: Faz requisições HTTP ou baixa arquivos.
```
curl http://exemplo.com   # Realiza uma requisição HTTP GET
```
- **wget**: Baixa arquivos da web.
``` 
wget http://exemplo.com/arquivo.zip
```
### 14. **Comandos de Controle de Sistema**
- **reboot**: Reinicia o sistema.
```
sudo reboot
```
- **shutdown**: Desliga o sistema.
```
sudo shutdown -h now   # Desliga imediatamente
```
- **uptime**: Exibe o tempo que o sistema está em execução.
```
uptime
```
### 15. **Logs do Sistema**
- **dmesg**: Exibe mensagens do kernel.
```
dmesg
```
- **tail**: Exibe as últimas linhas de um arquivo de log.
```
tail -f /var/log/syslog   # Monitora o log em tempo real
```
### 16. **Comandos de Compressão e Descompressão**
- **gzip**: Compacta arquivos.
``` 
gzip arquivo.txt   # Compacta arquivo.txt
```

- **gunzip**: Descompacta arquivos.
```
gunzip arquivo.txt.gz   # Descompacta arquivo.txt.gz
```
### 17. **Gerenciamento de Discos e Partições**
- **fdisk**: Ferramenta para gerenciar partições de disco.
``` 
sudo fdisk -l   # Lista todas as partições
```
- **mount**: Monta um sistema de arquivos.
``` 
sudo mount /dev/sdb1 /mnt   # Monta o dispositivo /dev/sdb1 no diretório /mnt
```
- **umount**: Desmonta um sistema de arquivos.
```
sudo umount /mnt
```

