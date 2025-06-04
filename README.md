# Roundcube_debug_docker
Sort of template for docker compose to make debug environment for roundcube be easier. The point is to help security researcher to pull, modify basic valua in settings, run docker and enjoy hacking instead of wasting **days** deploying, debuging simple environment.

Default connection of roundcube webpage is `http://127.0.0.1:8000`

# Default credential (modify is optional):

Login with `user@example.com`:`password`. To generate different credential, modify `config/postfix-accounts.cf`. Generate hash with `doveadm pw -s SHA512-CRYPT -p password` or `docker run --rm tvial/docker-mailserver doveadm pw -s SHA512-CRYPT -p password`

# Settings for remote debugging with vscode (required)

Modify value of IP address in `php-fpm/xdebug.ini` (`xdebug.client_host`). Value of IP should be IP address of machine that's running VScode.

# Start:

`docker-compose up` with any extra flags you like (`docker compose` should work too)
