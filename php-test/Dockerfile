# Utiliser une image de base PHP
FROM php:8.1-cli

# Installer les dépendances nécessaires
RUN apt-get update && apt-get install -y \
    git \
    unzip \
    && docker-php-ext-install pdo pdo_mysql

# Copier le fichier de workflow (php-test.yml) dans l'image
COPY .github/workflows/php-test.yml /workspace/php-test.yml

# Définir le répertoire de travail
WORKDIR /workspace

# Point d'entrée par défaut
CMD ["php", "/workspace/php-test.yml"]