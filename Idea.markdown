
# Primära, GCE

VM - Yggdrasil - Containerized: Dovecot mm
VM - Freja - Containerized: RCube (Webmail), THP.se, Zvea.se, Guldvaskarn.org osv

# Yggdrasil

    ENV COMPOSE_URL = https://github.com/docker/compose/releases/download/1.25.0-rc1/docker-compose-`uname -s`-`uname -m`
    ENV MAILCOW_REPO = https://github.com/mailcow/mailcow-dockerized

    apt update && apt upgrade

    curl -sSL https://get.docker.com/ | CHANNEL=stable sh
    curl -L $COMPOSE_URL -o /usr/local/bin/docker-compose
    chmod +x /usr/local/bin/docker-compose
    umask

    cd /opt

    git clone $MAILCOW_REPO && cd mailcow-dockerized
    docker-compose pull && docker-compose up -d


# Freja

webmail.(thp-produktion.se|ostara.se|ostaraproduktion.se|nd.se|zvea.co)
www.(thp-produktion.se|ostara.se|guldvaskarn.org|zvea.co)

    ENV COMPOSE_URL = https://github.com/docker/compose/releases/download/1.25.0-rc1/docker-compose-`uname -s`-`uname -m`

    apt update && apt upgrade

    curl -sSL https://get.docker.com/ | CHANNEL=stable sh
    curl -L $COMPOSE_URL -o /usr/local/bin/docker-compose
    chmod +x /usr/local/bin/docker-compose
