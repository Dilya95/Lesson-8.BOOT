# Домашнее задание 8: Работа с загрузчиком

## Задания
1. Включить отображение меню Grub.
2. Попасть в систему без пароля несколькими способами.
3. Установить систему с LVM, после чего переименовать VG



## Выполнение

### Включить отображение меню Grub:
```
root@otus-homework:~# nano /etc/default/grub

root@otus-homework:~# cat /etc/default/grub
# If you change this file, run 'update-grub' afterwards to update
# /boot/grub/grub.cfg.
# For full documentation of the options in this file, see:
#   info -f grub -n 'Simple configuration'

GRUB_DEFAULT=0
#GRUB_TIMEOUT_STYLE=hidden
GRUB_TIMEOUT=20
GRUB_DISTRIBUTOR=`lsb_release -i -s 2> /dev/null || echo Debian`
GRUB_CMDLINE_LINUX_DEFAULT="autoinstall ds=nocloud-net;seedfrom=http://image-builder.3hc.io/ubuntu22.04/"
GRUB_CMDLINE_LINUX="net.ifnames=0 biosdevname=0 console=tty0 console=ttyS0,115200n8"


root@otus-homework:~# update-grub
Sourcing file `/etc/default/grub'
Sourcing file `/etc/default/grub.d/init-select.cfg'
Generating grub configuration file ...
Found linux image: /boot/vmlinuz-5.15.0-71-generic
Found initrd image: /boot/initrd.img-5.15.0-71-generic
Warning: os-prober will not be executed to detect other bootable partitions.
Systems on them will not be added to the GRUB boot configuration.
Check GRUB_DISABLE_OS_PROBER documentation entry.
done
```

### Попасть в систему без пароля несколькими способами:
```
![Попасть в систему без пароля](screenshots/recmode.jpg )
```

### Установить систему с LVM, после чего переименовать VG:
```
```
