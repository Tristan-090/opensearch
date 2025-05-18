# Utiliser l'image officielle OpenSearch comme base
FROM opensearchproject/opensearch:latest

# Définir des variables d'environnement
ENV discovery.type=single-node
ENV OPENSEARCH_JAVA_OPTS="-Xms512m -Xmx512m"

# Copier un fichier de configuration personnalisé (facultatif)
#COPY opensearch.yml /usr/share/opensearch/config/
RUN echo "plugins.security.disabled: true" >> /usr/share/opensearch/config/opensearch.yml

# Exposer les ports utilisés par OpenSearch
EXPOSE 9200 9600

# Commande par défaut pour lancer OpenSearch
CMD ["/usr/share/opensearch/bin/opensearch"]