# =============================================
# Dockerfile - Nginx (Proxy Reverso)
# =============================================

# Usa a imagem oficial do Nginx com Alpine
FROM nginx:alpine

# Remove a configuração padrão do Nginx
# Sem isso, o Nginx carregaria a config padrão E a nossa, causando conflito
RUN rm /etc/nginx/conf.d/default.conf

# Copia nossa configuração customizada para o local correto dentro do container
COPY nginx.conf /etc/nginx/nginx.conf

# Expõe a porta 80 (HTTP padrão)
EXPOSE 80