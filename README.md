    docker-compose down
    docker-compose build
    docker-compose up -d
    docker-compose logs

    docker-compose logs; while [ $? -ne 0 ]; do docker-compose logs; done;

Connect to the running container:

    docker exec -ti 665b4a1e17b6 bash

`vim /etc/dnsmasq.conf`:

    address=/.adeira.loc/127.0.0.1
    address=/.zlml.loc/127.0.0.1
    address=/.adminer.loc/127.0.0.1

`systemctl restart dnsmasq`

    ln -s /home/martin/Work/mrtnzlml/docker-stack/bin/php.sh /usr/local/bin/php

Inspiration:
- https://github.com/laradock/laradock
- https://github.com/dockette/devstack