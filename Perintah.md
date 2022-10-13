# List 

## Menghapus karakter tertentu dari sebuah input.

misal menghapus karakter "(" dan ")"

```
$  $output | tr -d "()"
```

## Mengetahui persentase volume melalui amixer.

```
$ amixer get Master | grep -E '[0-9]{1,3}%' | awk {'print $4'} | tr -d []
```
