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