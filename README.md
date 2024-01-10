# pandora-refresh-token

用于刷新 pandora 所用的 session_token, 初始代码由[不良林](https://www.youtube.com/@bulianglin)大佬开发，修改由 crontab 来确保定期执行

## Usage

1. 将 `pandora-get-token.py` 放在 `pandora` 目录下，也即和 `config.json` 和 `license.jwt` 同一个目录，最后 `crontab -e` 添加以下代码

    ```
    23 4 * * 3 python3 FILE_PATH -e API_ENDPOINT
    ```

    1. 将 `FILE_PATH` 替换为pandora-get-token.py文件路径
    2. 将 `API_ENDPOINT` 替换为自己服务器的地址，如 `http://127.0.0.1:8181/test111`

2. (可选) 支持使用 `-p` 指定 `pool_token`

    ```
    23 4 * * 3 python3 FILE_PATH -e API_ENDPOINT -p POOL_TOKEN
    ```

## Credits

- [bulianglin](https://www.youtube.com/watch?v=IXA6IJY6ZW8&t=9s)
- [pandora](https://github.com/pandora-next/deploy)
