# dump Array
### php logger
```
use Nagomien\Logger\Logger;

$logger = new Logger();
$logger->dumper("strings",[2]);
```
```
$ cat /tmp/dumper.log
[2017-02-21 17:06:55] [strings] [Array
(
    [0] => 2
)
]
```
#### dump your file
```
use Nagomien\Logger\Logger;

$logger = new Logger("/path/to/file");
$logger->dumper("strings",[2]);
```
```
$ cat /path/to/file
[2017-02-21 17:06:55] [strings] [Array
(
    [0] => 2
)
]
```
# dump object
```
use Nagomien\Logger\Logger;

$logger = new Logger();
$logger->dumper("strings",$logger);
```
```
$ cat /tmp/dumper.log
[2017-02-21 17:59:37] [1] [Nagomien\Logger\Logger Object
(
    [fpath:Nagomien\Logger\Logger:private] => /tmp/dumper.log
)
]
```

