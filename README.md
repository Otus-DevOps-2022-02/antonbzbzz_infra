# antonbzbzz_infra
Добрый день!
Видимо рано удалил отключил виртуалки в прошлый раз, тест не прошли. Повторяю коммит.
Для подключения одной командой можно использовать скрипт:
#!/usr/bin/expect
set timeout 60
spawn ssh -i /c/Users/Anton/.ssh/appuser -A appuser@51.250.15.5
#ssh -p [lindex $argv 3] [lindex $argv 1]@[lindex $argv 0]
expect ":~$ " {
        send "ssh 10.128.0.14"
        }
interact

bastion_IP = 51.250.15.5
someinternalhost_IP = 10.128.0.14