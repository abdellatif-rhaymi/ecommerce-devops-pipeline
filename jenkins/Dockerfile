FROM jenkins/jenkins:lts

USER root

# Installer Java, Maven et Docker CLI
RUN apt-get update && \
    apt-get install -y maven openjdk-17-jdk docker.io && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Donner les permissions à Jenkins pour utiliser Docker
RUN groupadd -g 999 docker || true && usermod -aG docker jenkins

# Revenir à l'utilisateur Jenkins
USER jenkins
