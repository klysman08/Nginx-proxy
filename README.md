# NGINX Proxy Manage
É uma ferramenta de código aberto que simplifica a configuração e o gerenciamento de servidores proxy reversos baseados no servidor web NGINX. Ele fornece uma interface para configuração de proxies reversos, redirecionamentos de URL, balanceamento de carga e outras tarefas relacionadas à configuração do NGINX.

Com o NGINX Proxy Manager, é possível configurar facilmente proxies reversos para encaminhar solicitações de entrada para vários aplicativos web ou servidores internos. Isso é útil quando você deseja expor aplicativos web internos para a Internet ou quando deseja redirecionar solicitações de um domínio para diferentes serviços ou aplicativos.

## Docker compose
```bash
version: '3.8'
services:
  app:
    image: 'jc21/nginx-proxy-manager:latest'
    restart: unless-stopped
    ports:
      - '80:80'
      - '81:81'
      - '443:443'
    volumes:
      - ./data:/data
      - ./letsencrypt:/etc/letsencrypt
```

