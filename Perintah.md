# List 

## Menghapus karakter tertentu dari sebuah input.

misal menghapus karakter "(" dan ")"

```
$  $output | tr -d "()"
```

## Mengetahui persentase volume melalui amixer.

Opsi 1 (distro crux 3.7).

```
$ amixer get Master | grep -E '[0-9]{1,3}%' | awk {'print $4'} | tr -d []
```
Opsi 2 (debian unstable).

```
$ amixer get Master | grep -E '[0-9]{1,3}%' | awk {'print $5'} | tr -d [] | tail -n1
```

## Mengetahui jumlah paket yang terinstall (debian dan turunannya).

```
$ dpkg -l | wc -l
```
