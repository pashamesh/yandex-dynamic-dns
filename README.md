# Yandex dynamic DNS
Yandex DNS record update script. Useful when you have dynamic IP address.

## Configuration
There are next configuration options available

#### DOMAIN
2nd level domain delegated to Yandex DNS. For example `example.com`

#### SUBDOMAIN
Subdomain at `DOMAIN` which DNS record need to be updated by script. Use `@` for 2 level domain records. For example `home-pc`

#### API_TOKEN
Yandex DNS XML API token.

Visit `https://pddimp.yandex.ru/token/index.xml?domain={DOMAIN}` using your favourite web browser, fill captcha and copy new token. Please take note that you should be logged in to https://pdd.yandex.ru

#### DOMAIN_RECORD_ID
Identifier domain record that will be updated by script.

Visit `https://pddimp.yandex.ru/nsapi/get_domain_records.xml?token={API_TOKEN}&domain={DOMAIN}` using your favourite web browser, find id of apropriate DNS record and copy it. As above you should be logged in to https://pdd.yandex.ru

## Using
```
chmod u+x ya-dns-updater
./ya-dns-updater
```

## Links
[Yandex PDD API V1 documentation](https://tech.yandex.ru/pdd/doc/files/api-pdd-v1.pdf)

## Roadmap
- migrate to Yandex PDD API V2
- add ability for recurrent script execution
- add ability to configure IP adress resolve method
