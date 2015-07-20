# InnoHub Ansible : barman
=========

* Creates a pg barman deployment
* Sets up full and/or incremental backup task/s

Requirements
------------

* Existing postgres server

Role Variables
--------------

barman_home : Not Required : defaults to /var/lib/barman

barman_user : Not Required : defaults to barman

barman_group : Not Required : defaults to barman

barman_log_file : Not Required : defaults to /var/log/barman/barman.log

barman_authorized_keys : Required : should contain postgres' public ssh key

ssh-rsa
AAAAB3NzaC1yc2EAAAADAQABAAABAQC0qnZuQr/09bqiEK4QDmfb88Z1wrQFC0ytnYFAU93Q5Ok6dK1x+RvV1CnMg8WlzA492XAlxJNJHz09riUPVEFaRQfUch+6sXWVv/iwQM7WcC2DIrh6ZV52LJg5jyKJTYJa622+jGfwebuyPCw5ymo2k4bi25JRF5eUo1ghcP+PiCEZJwksxkBt1O5CERjSzsWHT5dGpQ7FysSxT67B70MiFohNySbCAIMRt5NZUI7LCE+SbNDuv/HfVdr6VAo0IRMvqcJjTdM+0CjNEkzqNXE7ZfVWfqqg8kO+x9uRKffxqfVl6C3CMg51qCtRBu/8zSSr2ub02BWnYzhYfwZTLbj3

barman_ssh_private_key :  Required

  -----BEGIN RSA PRIVATE KEY-----
  MIIEowIBAAKCAQEAmh9xFxQj5RyLRnKFenvjAFdudMWaBKmsYnCRtPy6jgacUerq
  h3GVkr9eddGSDzL4+o2KBaF9oFX27gCAUWTT0bYayn68Kj5gaXevWr1nlyJfUlC2
  nyX6OykYOLCMqUqWCJjrq5bqMOzDF+Fg9zzhhUliriPx+BC4hm18cCN0fnt/xZXk
  orICOPUHlOeRkGlyMfJSvSpaXgBzEnBgsoxOWDH+fa7P3BKJC9pWgk0bRgk15i2T
  AXnlHyC+J+J58dKHLmA9yTDetUgsY6TRdqAahqAFbOdSoci6boJYUXmFNCJIzv6M
  Cm4V/YrsO8ZAp9kUgfei8fImN/nzdW7FLlrb9wIDAQABAoIBAFL6vLO1R0IypRXv
  0MfKbcSgTjsWrL7373UssHZmX7bZ/k3okg8Ma4CQAjai9+WxBvY3QGmZsf6iaglo
  Qa4RAC53wmLl6z8/SD9gjgvn0B9CBVpXVIvJMbmqfX0AKSt4meDVHIXNAhgHUV7J
  HKDgqXdOtI+XkM6DiiXuSsJBhJYX6B4fsK+vlEwkYPe3v1jk48VwIbj7GIDFnTuO
  Q1NKImPsx9cSZeBOD7EZmYNeEq3jU0f5g8ezw/x5AUF0S/lv+wt7+4fSA9HqzRhH
  YGeV7rPwmRZV1uKYdN7rhGus9UNrPPXLZeCoT5OLw5Y3RvFY9uit1BfXLcuWn8Fs
  SpfsaIECgYEAygLAhvk6Oax1p5ltBg4r0pu7r5vtasPyiK+z8WEztlxKrVDCI+qw
  7pDb99sqd7MHfJKaMxdQGusc1YoAT/4o4lGPJtDAc2eJCxyNyBWFUyhnewR0viK7
  EJSTBNxWG0RfhEaghXWDQG/Sxt7NxptsdB+fwboaM/fbHRIT821QTcECgYEAw1BG
  brHJprogvpUQ9Z5nWbszgHaw8XXHCDt9MwXhniwZQ35Epg+izHtvIC+O18EE7Bii
  x30MV93cGBO0OmEomXCCxQgVrHLd8zTgQT6j0f9zfwv83NtJTh74/MrviEK2lV3I
  rCFxK3/0Jx57hOexHv14AemZ9d9cqfE+mLKTB7cCgYAnr5C5M38v02Stz2NuvBv5
  3SRrJHvo7KPaHIKCWjE5kzoMgIATZEjsJUNBlynpqB9BZt+qR9sx3pykit7y2CCa
  DaHM41fblCyFJU/pTekKZDaoIUD6FYKgiD+1xb+Yzb7iEqn4bhSh9RX4gc71RJVy
  3r+Y5IG/UeMW+/U1bnVHQQKBgQCnsi8nMANh4gHnYPoUyhMW2kLYFBDM4UEo8lsH
  Cg+zzU1LxAiRRG+Vfo3lZrAQ06u0Q1rQSa/laZpmGdTvIyjGxfGh1tU1IdMr1MSP
  gIcL8XdrKBHOV4HTT4idFGkh55X5HXMFSBlxLgWl6OhJLt3HK/50Nex5TXS0fWwv
  k3PmdQKBgCfZicxrG+lnPotx8HguZEKt+clDQdATRQRMIWI5ELLToMvVLL5YYkro
  dErmcGk3unAKhIFYb6yhNXBuxyPRW9hGwpu9/p2uQxaswkxszZ1T9aWcN240YZMy
  L4gZ7v/wqUwlXvxqQebDcn8b0Xl8Vsz0KnO8YvtHfKaX5gWFFmhs
  -----END RSA PRIVATE KEY-----

barman_ssh_public_key : Required

  ssh-rsa
AAAAB3NzaC1yc2EAAAADAQABAAABAQCaH3EXFCPlHItGcoV6e+MAV250xZoEqaxicJG0/LqOBpxR6uqHcZWSv1510ZIPMvj6jYoFoX2gVfbuAIBRZNPRthrKfrwqPmBpd69avWeXIl9SULafJfo7KRg4sIypSpYImOurluow7MMX4WD3POGFSWKuI/H4ELiGbXxwI3R+e3/FleSisgI49QeU55GQaXIx8lK9KlpeAHMScGCyjE5YMf59rs/cEokL2laCTRtGCTXmLZMBeeUfIL4n4nnx0ocuYD3JMN61SCxjpNF2oBqGoAVs51KhyLpuglhReYU0IkjO/owKbhX9iuw7xkCn2RSB96Lx8iY3+fN1bsUuWtv3


barman_ssh_keyscan_domains : Required

  - sampledomain.com

barman_configuration_file_path : Not Required : defaults to /etc/barman.conf

barman_log_file : Not Required : defaults to /var/log/barman/barman.log

barman_log_file : Not Required : defaults to gzip

barman_reuse_backup : Not Required : defaults to link

barman_minimum_redundancy : Not Required : defaults to 10

barman_retention_policy : Not Required : defaults to RECOVERY WINDOW OF 4 WEEKS

barman_network_compression : Not Required : defaults to false

barman_basebackup_retry_times : Not Requried : defaults to 3

barman_basebackup_retry_sleep : Not Required : defaults to 30

barman_last_backup_maximum_age : Not Required : defaults to ""

barman_upstreams : Required : defaults to values below

  - name: main
    description: "Main postgres db server"
    hostname: "pg"
    postgres_user: "postgres"
    port: "5432"
    cron_full_backup: true
    cron_full_backup_interval: "0 0 * * *"
    cron_full_backup_reuse_backup: none
    cron_incremental_backup: true
    cron_incremental_backup_interval: "0 */6 * * *"
    cron_incremental_backup_reuse_backup: link

postgres_authorized_keys: Required : should contain barman's public ssh key

ssh-rsa
AAAAB3NzaC1yc2EAAAADAQABAAABAQCaH3EXFCPlHItGcoV6e+MAV250xZoEqaxicJG0/LqOBpxR6uqHcZWSv1510ZIPMvj6jYoFoX2gVfbuAIBRZNPRthrKfrwqPmBpd69avWeXIl9SULafJfo7KRg4sIypSpYImOurluow7MMX4WD3POGFSWKuI/H4ELiGbXxwI3R+e3/FleSisgI49QeU55GQaXIx8lK9KlpeAHMScGCyjE5YMf59rs/cEokL2laCTRtGCTXmLZMBeeUfIL4n4nnx0ocuYD3JMN61SCxjpNF2oBqGoAVs51KhyLpuglhReYU0IkjO/owKbhX9iuw7xkCn2RSB96Lx8iY3+fN1bsUuWtv3

postgres_ssh_private_key : Required

  -----BEGIN RSA PRIVATE KEY-----
  MIIEowIBAAKCAQEAmh9xFxQj5RyLRnKFenvjAFdudMWaBKmsYnCRtPy6jgacUerq
  h3GVkr9eddGSDzL4+o2KBaF9oFX27gCAUWTT0bYayn68Kj5gaXevWr1nlyJfUlC2
  nyX6OykYOLCMqUqWCJjrq5bqMOzDF+Fg9zzhhUliriPx+BC4hm18cCN0fnt/xZXk
  orICOPUHlOeRkGlyMfJSvSpaXgBzEnBgsoxOWDH+fa7P3BKJC9pWgk0bRgk15i2T
  AXnlHyC+J+J58dKHLmA9yTDetUgsY6TRdqAahqAFbOdSoci6boJYUXmFNCJIzv6M
  Cm4V/YrsO8ZAp9kUgfei8fImN/nzdW7FLlrb9wIDAQABAoIBAFL6vLO1R0IypRXv
  0MfKbcSgTjsWrL7373UssHZmX7bZ/k3okg8Ma4CQAjai9+WxBvY3QGmZsf6iaglo
  Qa4RAC53wmLl6z8/SD9gjgvn0B9CBVpXVIvJMbmqfX0AKSt4meDVHIXNAhgHUV7J
  HKDgqXdOtI+XkM6DiiXuSsJBhJYX6B4fsK+vlEwkYPe3v1jk48VwIbj7GIDFnTuO
  Q1NKImPsx9cSZeBOD7EZmYNeEq3jU0f5g8ezw/x5AUF0S/lv+wt7+4fSA9HqzRhH
  YGeV7rPwmRZV1uKYdN7rhGus9UNrPPXLZeCoT5OLw5Y3RvFY9uit1BfXLcuWn8Fs
  SpfsaIECgYEAygLAhvk6Oax1p5ltBg4r0pu7r5vtasPyiK+z8WEztlxKrVDCI+qw
  7pDb99sqd7MHfJKaMxdQGusc1YoAT/4o4lGPJtDAc2eJCxyNyBWFUyhnewR0viK7
  EJSTBNxWG0RfhEaghXWDQG/Sxt7NxptsdB+fwboaM/fbHRIT821QTcECgYEAw1BG
  brHJprogvpUQ9Z5nWbszgHaw8XXHCDt9MwXhniwZQ35Epg+izHtvIC+O18EE7Bii
  x30MV93cGBO0OmEomXCCxQgVrHLd8zTgQT6j0f9zfwv83NtJTh74/MrviEK2lV3I
  rCFxK3/0Jx57hOexHv14AemZ9d9cqfE+mLKTB7cCgYAnr5C5M38v02Stz2NuvBv5
  3SRrJHvo7KPaHIKCWjE5kzoMgIATZEjsJUNBlynpqB9BZt+qR9sx3pykit7y2CCa
  DaHM41fblCyFJU/pTekKZDaoIUD6FYKgiD+1xb+Yzb7iEqn4bhSh9RX4gc71RJVy
  3r+Y5IG/UeMW+/U1bnVHQQKBgQCnsi8nMANh4gHnYPoUyhMW2kLYFBDM4UEo8lsH
  Cg+zzU1LxAiRRG+Vfo3lZrAQ06u0Q1rQSa/laZpmGdTvIyjGxfGh1tU1IdMr1MSP
  gIcL8XdrKBHOV4HTT4idFGkh55X5HXMFSBlxLgWl6OhJLt3HK/50Nex5TXS0fWwv
  k3PmdQKBgCfZicxrG+lnPotx8HguZEKt+clDQdATRQRMIWI5ELLToMvVLL5YYkro
  dErmcGk3unAKhIFYb6yhNXBuxyPRW9hGwpu9/p2uQxaswkxszZ1T9aWcN240YZMy
  L4gZ7v/wqUwlXvxqQebDcn8b0Xl8Vsz0KnO8YvtHfKaX5gWFFmhs
  -----END RSA PRIVATE KEY-----

postgres_ssh_public_key : Required

  ssh-rsa
AAAAB3NzaC1yc2EAAAADAQABAAABAQCaH3EXFCPlHItGcoV6e+MAV250xZoEqaxicJG0/LqOBpxR6uqHcZWSv1510ZIPMvj6jYoFoX2gVfbuAIBRZNPRthrKfrwqPmBpd69avWeXIl9SULafJfo7KRg4sIypSpYImOurluow7MMX4WD3POGFSWKuI/H4ELiGbXxwI3R+e3/FleSisgI49QeU55GQaXIx8lK9KlpeAHMScGCyjE5YMf59rs/cEokL2laCTRtGCTXmLZMBeeUfIL4n4nnx0ocuYD3JMN61SCxjpNF2oBqGoAVs51KhyLpuglhReYU0IkjO/owKbhX9iuw7xkCn2RSB96Lx8iY3+fN1bsUuWtv3

postgres_ssh_keyscan_domains : Required

  - sampledomain.com

License
-------

MIT
