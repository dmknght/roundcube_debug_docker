# Roundcube_debug_docker
Sort of template for docker compose to make debug environment for roundcube be easier

# Default credential:

Login with `user@example.com`:`password`. To generate different credential, modify `config/postfix-accounts.cf`. Generate hash with `doveadm pw -s SHA512-CRYPT -p password` or `docker run --rm tvial/docker-mailserver doveadm pw -s SHA512-CRYPT -p password`
