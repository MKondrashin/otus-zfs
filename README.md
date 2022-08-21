# otus-zfs<br/>
<br/>
Получилось лучший gzip-6 (который по умолчанию, насколько я понял):<br/>
[root@server ~]# zfs list<br/>
NAME          USED  AVAIL     REFER  MOUNTPOINT<br/>
stripe       20.0M  5.43G     36.5K  /stripe<br/>
stripe/fs1   1.44M  5.43G     1.44M  /stripe/fs1<br/>
# stripe/fs10  3.23M  5.43G     3.23M  /stripe/fs10<br/>
stripe/fs11  2.41M  5.43G     2.41M  /stripe/fs11<br/>
stripe/fs12  2.02M  5.43G     2.02M  /stripe/fs12<br/>
stripe/fs13    24K  5.43G       24K  /stripe/fs13<br/>
stripe/fs2   1.39M  5.43G     1.39M  /stripe/fs2<br/>
stripe/fs3   1.34M  5.43G     1.34M  /stripe/fs3<br/>
stripe/fs4   1.30M  5.43G     1.30M  /stripe/fs4<br/>
stripe/fs5   1.26M  5.43G     1.26M  /stripe/fs5<br/>
# stripe/fs6   1.24M  5.43G     1.24M  /stripe/fs6<br/>
# stripe/fs7   1.23M  5.43G     1.23M  /stripe/fs7<br/>
stripe/fs8   1.23M  5.43G     1.23M  /stripe/fs8<br/>
stripe/fs9   1.23M  5.43G     1.23M  /stripe/fs9<br/>
[root@server ~]# zfs get  compression<br/>
NAME         PROPERTY     VALUE           SOURCE<br/>
stripe       compression  off             default<br/>
stripe/fs1   compression  gzip-1          local<br/>
stripe/fs10  compression  zle             local<br/>
stripe/fs11  compression  lzjb            local<br/>
stripe/fs12  compression  lz4             local<br/>
stripe/fs13  compression  off             default<br/>
stripe/fs2   compression  gzip-2          local<br/>
stripe/fs3   compression  gzip-3          local<br/>
stripe/fs4   compression  gzip-4          local<br/>
stripe/fs5   compression  gzip-5          local<br/>
stripe/fs6   compression  gzip            local<br/>
stripe/fs7   compression  gzip-7          local<br/>
stripe/fs8   compression  gzip-8          local<br/>
stripe/fs9   compression  gzip-9          local
