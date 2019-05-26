# SSH

[如何生成SSH key - 简书](https://www.jianshu.com/p/31cbbbc5f9fa)


ssh-keygen -t rsa -f ~/.ssh/id_rsa.github -C 'your-email'


# SSH setting

[ssh免密登录配置 - 简书](https://www.jianshu.com/p/0922095f69f3)

生成密钥

```bash
ssh-keygen -t rsa
```

生成的公钥在

```bash
~/.ssh/id_rsa.pub
```

将公钥写入免密服务器的

```bash
~/.ssh/authorized_keys
```

配置本地

```bash
~/.ssh/config
Host <nick\>
HostName <addr\>
User <user\>
IdentitiesOnly yes
```

## note

如何配置多个密钥且同时生效

1. 生成密钥(要不同的名字 不能使用默认的名字)

```bash
 keys ssh-keygen -t rsa -C "liu.yamn@gmail.com"
```


2. ssh-add 永久加入 Keychain

```bash
 ssh-add -K keyname
```

3. 配置 config