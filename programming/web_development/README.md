# Web Development

[Go Back](../)

## Certificados SSL

* Para renovar certifcados de um servidor web com docker - `docker run --rm -ti   -v $(pwd)/letsencrypt:/etc/letsencrypt certbot/certbot certonly --agree-tos -n  -d “dominio.com.br”  --manual   --email=eu@aqui.com (--email=eu@aqui.com)`
* Para renovar certificados de um servidor kubernetes com traefik - https://www.thebookofjoel.com/k3s-cert-manager-letsencrypt

## DNS

Informações bem úteis sobre os tipos de mapeamento - https://registro.br/tecnologia/caracteristicas-tecnicas/
Como criar subdomínios wildcard - https://brasilcloud.com.br/tutoriais/como-criar-um-subdominio-wildcard-curinga-cpanel/
