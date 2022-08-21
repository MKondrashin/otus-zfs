# otus-zfs

Получилось лучший gzip-6 (который по умолчанию, насколько я понял):
[root@server ~]# zfs list
NAME          USED  AVAIL     REFER  MOUNTPOINT
stripe       20.0M  5.43G     36.5K  /stripe
stripe/fs1   1.44M  5.43G     1.44M  /stripe/fs1
# stripe/fs10  3.23M  5.43G     3.23M  /stripe/fs10
stripe/fs11  2.41M  5.43G     2.41M  /stripe/fs11
stripe/fs12  2.02M  5.43G     2.02M  /stripe/fs12
stripe/fs13    24K  5.43G       24K  /stripe/fs13
stripe/fs2   1.39M  5.43G     1.39M  /stripe/fs2
stripe/fs3   1.34M  5.43G     1.34M  /stripe/fs3
stripe/fs4   1.30M  5.43G     1.30M  /stripe/fs4
stripe/fs5   1.26M  5.43G     1.26M  /stripe/fs5
# stripe/fs6   1.24M  5.43G     1.24M  /stripe/fs6
# stripe/fs7   1.23M  5.43G     1.23M  /stripe/fs7
stripe/fs8   1.23M  5.43G     1.23M  /stripe/fs8
stripe/fs9   1.23M  5.43G     1.23M  /stripe/fs9
[root@server ~]# zfs get  compression
NAME         PROPERTY     VALUE           SOURCE
stripe       compression  off             default
stripe/fs1   compression  gzip-1          local
stripe/fs10  compression  zle             local
stripe/fs11  compression  lzjb            local
stripe/fs12  compression  lz4             local
stripe/fs13  compression  off             default
stripe/fs2   compression  gzip-2          local
stripe/fs3   compression  gzip-3          local
stripe/fs4   compression  gzip-4          local
stripe/fs5   compression  gzip-5          local
stripe/fs6   compression  gzip            local
stripe/fs7   compression  gzip-7          local
stripe/fs8   compression  gzip-8          local
stripe/fs9   compression  gzip-9          local