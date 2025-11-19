FROM nginx:latest
LABEL maintainer="henriquemota"
# Diretório da aplicação
WORKDIR /var/www/html
# Copia os arquivos da aplicação (se houver) e a configuração do nginx
COPY ./nginx.conf /etc/nginx/conf.d/default.conf
# Garante permissões corretas para o usuário nginx
RUN chown -R nginx:nginx /var/www/html
EXPOSE 80
# # Healthcheck simples
# HEALTHCHECK --interval=30s --timeout=3s --retries=3 CMD wget -qO- http://localhost/ >/dev/null || exit 1
# O CMD padrão da imagem já inicia o nginx em foreground (nginx -g 'daemon off;')