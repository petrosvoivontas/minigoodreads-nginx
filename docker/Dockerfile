FROM nginx:1.27.0-perl
LABEL org.opencontainers.image.source https://github.com/petrosvoivontas/minigoodreads-nginx

# Environment variables
ENV BE_HOST=minigoodreads_be
ENV BE_PORT=8081
ENV FRONTEND_ROOT_DIR='/app'

# Copy to the templates folder so that the variables get substituded
COPY ../nginx.conf /etc/nginx/templates/nginx.conf.template

# Delete the default conf file
RUN rm /etc/nginx/conf.d/default.conf