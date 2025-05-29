# 原项目
https://github.com/deepseek-ai/Janus

# 安装
```
python3.10 -m venv venv
source venv/bin/activate
pip install -r requirements.txt 
```


## frp 配置
```
cat /data/work/frp/frpc.ini 
vim /data/work/frp/frpc.ini

# 后台
[ssh-PlantBackend]
type = tcp
local_ip = 127.0.0.1
local_port = 8503
remote_port = 8503
use_encryption = false
use_compression = false

[ssh-PlantFront]
type = tcp
local_ip = 127.0.0.1
local_port = 8502
remote_port = 8502
use_encryption = false
use_compression = false


# 重启frp
sudo systemctl restart  supervisor
sudo supervisorctl reload
sudo supervisord
```