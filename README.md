1. カレントディレクトリに.vscodeファイルを作成。<br>
2. launch.jsonファイルを作成し下記を記載する。

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
<br>


3. docker/mysql配下にstorageフォルダを作成。

<br>

4. コンテナ作成。
 ```
docker-compose build
``` 

<br>

5. dockerスタート
```
docker-compose up -d
```

<br>

6. 下記のコマンドでコンテナに入る
```
docker-compose exec app bash
```

7.  プロジェクトをダウンロード。

<br>

8. http://localhost/public