# Ativar usuário root (VPS Oracle)

### Entrar e definir como Usuário root 

- Rode o comando abaixo para mudar o terminal para o usuário root
```bash
sudo -i
```
- Abra as portas que precisa dentro da subnet da sua instancia da Oracle, ignore essa etapa caso queira apenas ativar o SSH pro usuario root

- Rode o comando abaixo para configurar o acesso root ao SSH e definir uma senha

```bash
bash <(wget -qO- https://raw.githubusercontent.com/JobasFernandes/root/main/root.sh)
```

- Agora é só fazer o logout da VPS Oracle e fazer o login usando o usuário root e senha definida!

- Exemplo de comandos para abrir portas especificas na VPS

```bash
sudo iptables -F &&
sudo iptables -A INPUT -i lo -j ACCEPT &&
sudo iptables -A OUTPUT -o lo -j ACCEPT &&
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT &&
sudo iptables -A INPUT -p udp --dport 22 -j ACCEPT &&
sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT &&
sudo iptables -A INPUT -p udp --dport 80 -j ACCEPT &&
sudo iptables -A INPUT -p tcp --dport 443 -j ACCEPT &&
sudo iptables -A INPUT -p udp --dport 443 -j ACCEPT &&
sudo iptables -A INPUT -p tcp --dport 5432 -j ACCEPT &&
sudo iptables -A INPUT -p udp --dport 5432 -j ACCEPT &&
sudo iptables -A INPUT -p tcp --dport 6379 -j ACCEPT &&
sudo iptables -A INPUT -p udp --dport 6379 -j ACCEPT &&
sudo service netfilter-persistent save
```
