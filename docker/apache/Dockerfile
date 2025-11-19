# Usa a imagem oficial do PHP com Apache como base
FROM php:8.2-apache 
# Exemplo: Instala a extensão mysqli do PHP (comum para MySQL)
# Você pode adicionar outras extensões aqui
RUN docker-php-ext-install mysqli
# Exemplo: Habilita o módulo rewrite do Apache
RUN a2enmod rewrite

# # Copia os arquivos da sua aplicação para o diretório padrão do Apache
# COPY ./www/ /var/www/html/