# Publii config.json Merger

I used to split up Publii's `config.json` into multiple files, to simplify an initial config setup.

The python script searches parent directories for `.publii_theme_root` marker file. It is just an empty file. The name is important.
Then it merges `config/main.json` and `config/custom/groups/*.json`, where the last is added under key `customConfig` to the `main.json`
It will also create a `config/custom/group_order/order.json`. You can manage order of `.json` files under `customConfig` by `group` key with this file.
Newly added and removed groups are handled.
Then a merged `config.json` is created in the theme root dir.

The script was written with Python 3.12.

Execute:
```bash
./compile_config_json.sh
```
