### Конфигурация SSH на сервере

**Настройка /etc/ssh/sshd_config:**
- порт изменен;
- доступ по root отключен;
- доступ по паролю отключен;
- доступ по ключу включен;
- указаны файлы ключей;
- включено приветствие из motd.

```sshd_config
# Сохранены только измененные или раскомментированные параметры

Port 44916
PermitRootLogin no
PubkeyAuthentication yes
AuthorizedKeysFile	.ssh/authorized_keys .ssh/authorized_keys2
PasswordAuthentication no
PrintMotd yes
```

```motd
You are welcome!
```



