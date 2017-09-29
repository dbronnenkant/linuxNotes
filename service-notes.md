cd /etc/supervisor/conf.d
sudo vim wanderdragon.conf
sudo service supervisor stop
sudo service supervisor start
sudo tail -f /var/log/supervisor/supervisord.log 
suod tail -f /var/log/wanderdragon.out.log
sudo tail -f /var/log/wanderdragon.out.log


from /etc/supervisor/conf.d/wanderdragon

[program:wanderdragon]
command=/usr/bin/dotnet /var/websites/WanderDragon/WanderDragon.dll
directory=/var/websites/WanderDragon
autostart=true
autorestart=true
stderr_logfile=/var/log/wanderdragon.err.log
stdout_logfile=/var/log/wanderdragon.out.log
environment=ASPNETCORE_ENVIRONMENT=Production
user=www-data
stopsignal=INT
