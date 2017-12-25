# install node and npm package in package.json
FROM mysql:5.7

#设置免密登录
ENV MYSQL_ALLOW_EMPTY_PASSWORD yes

#将所需文件放到容器中
COPY setup.sh /mysql/setup.sh
COPY sosoapi-1.0.0.sql /mysql/sosoapi-1.0.0.sql
COPY privileges.sql /mysql/privileges.sql

EXPOSE 3306

#设置容器启动时执行的命令
CMD ["sh", "/mysql/setup.sh"]