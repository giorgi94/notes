# Configurations


To increase number watches on local computer

```
sudo sysctl -w fs.inotify.max_user_watches=524288
sudo sysctl -p
```

# Fedora

## Configure Xrdp Server

https://www.server-world.info/en/note?os=Fedora_32&p=desktop&f=7

```
$ sudo dnf -y install xrdp tigervnc-server
$ sudo systemctl enable --now xrdp
$ sudo firewall-cmd --add-port=3389/tcp --permanent
$ sudo firewall-cmd --reload
```

## Fix problems on Fedora, from live USB

https://www.svennd.be/mount-unknown-filesystem-type-lvm2_member/

## Modify dnf

```
Edit the file '/etc/dnf/dnf.conf' changing clean_requirements_on_remove=True to clean_requirements_on_remove=False then run dnf clean all.
```


## Fix theme in xfce4

If selected theme doesn't highlight active workspace, you can add following to your theme css file

```
/* Workspace switcher provided by libwnck */
wnck-pager:selected { background-color: shade(#398ee7, 0.88); }

wnck-pager:hover { background-color: #398ee7; }
```

