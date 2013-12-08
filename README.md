docker-psql
===========


#!/bin/sh

set -e

echo "----------------------------------------------------------------"
echo "PostgreSQL 9.2 Development Docker Container"
echo
echo "Username: pgdeveloper"
echo "Password: pgdeveloper"
echo "Database: pgdeveloper"
echo
echo "Connect with psql:"
echo "  psql -h localhost -p <port> -U pgdeveloper -d pgdeveloper"
echo
echo "Find the mapped <port> with Docker:"
echo " docker ps"
echo "----------------------------------------------------------------"

/etc/init.d/postgresql start

tail -f /var/log/postgresql/postgresql-9.2-main.log
