给客户弄的监控bot
自动识别波场地址 支持多链监听
批量添加地址 毫秒级回馈 自己拿去玩吧
运行指令：
cd /www/wwwroot/你的网站目录

cp config.php /root/lm_config_backup.php
cp -r storage /root/lm_storage_backup

mkdir -p /tmp/lm_v16
unzip -o /root/LM_MultiChain_Telegram_Bot_v1.6.zip -d /tmp/lm_v16

rsync -av --exclude=config.php --exclude=storage /tmp/lm_v16/LM_MultiChain_Telegram_Bot_v1.6/ /你的网站目录/

php install.php
bash scripts/install_systemd.sh /www/wwwroot/你的网站目录

运行机器人指令：
php check_telegram.php
