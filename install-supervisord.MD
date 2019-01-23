

sudo apt-get update
sudo apt-get install -y supervisor
sudo service supervisor start

Configuration for Supervisord is found in /etc/supervisor/supervisord.conf:

[include]
files = /etc/supervisor/conf.d/*.conf

supervisorctl reread
supervisorctl update

create a conf file under files  /etc/supervisor/conf.d/

command=
directory=
autostart=true
autorestart=true
startretries=3
startsecs=30
stderr_logfile=/var/log/xxxxx/err.log
stdout_logfile=/var/log/xxxxx/out.log
user=ec2-user
