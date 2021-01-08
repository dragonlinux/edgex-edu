## Important Dot Release Note (1.0.0 -> 1.0.1)
The Edinburgh 1.0.0 Docker Compose file was removed from this directory.  It used core, supporting, export and other 
    1.0.0 containers which contained a race condition.  Use the 1.0.1 Docker Compose file to get the same 1.0.0 
    functionality but with the critical race condition bugs removed.

使用方法：
docker-compose up -d   启动
docker-compose down    关闭
docker-compose down -v 关闭并清除保留数据

    
docker-compose -f docker-compose-localhost.yml down -v
docker-compose -f docker-compose-localhost.yml up -d
docker-compose -f docker-compose-localhost.yml down -v && docker-compose -f docker-compose-localhost.yml up -d
docker-compose -f docker-compose-localhost.yml logs -f simple-filter-json-mqtt-thingsboard-gateway 
docker-compose -f docker-compose-localhost.yml logs -f device-modbus
