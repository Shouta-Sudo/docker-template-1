1. docker/mysql配下にstorageフォルダを作成。


2. コンテナ作成。

 ```
docker-compose build
``` 


3. dockerスタート

```
docker-compose up -d
```


4. 下記のコマンドでコンテナに入る

```
docker-compose exec app bash
```

5. cd src

6.  git clone https://ShoutaSudou1117@bitbucket.org/apical-point-project/home-page-system.git .

7. カレントディレクトリに.vscodeフォルダを作成。<br>


8. launch.jsonファイルを作成し下記を記載する。

```
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [

        {
            "name": "Listen for Xdebug",
            "type": "php",
            "request": "launch",
            "port": 9004,
            "pathMappings": {
                "/var/www": "${workspaceRoot}/www"
            }
        },
        {
            "name": "Launch currently open script",
            "type": "php",
            "request": "launch",
            "program": "${file}",
            "cwd": "${fileDirname}",
            "port": 9004
        }
    ]
}
```

8. http://localhost/public


9. chmod -R 777 storage


10. php artisan storage:link


11. cp .env.example .env


12. php artisan key:generate


13. php artisan optimize


14. php artisan migarte


15.