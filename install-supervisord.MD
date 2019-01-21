yum install python-setuptools -y

easy_install supervisor

supervisord --version

echo_supervisord_conf > /etc/supervisord.conf

