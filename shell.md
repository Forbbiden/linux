
# script arguments process

```bash
while [ $# -gt 0 ]
do
    case "$1" in
        -serverPort) serverPort="$2"; shift;;
        -proxyRemotePort) proxyRemotePort="$2"; shift;;
        -proxyRemoteHost) proxyRemoteHost="$2"; shift;;
        -logLevel) logLevel="$2"; shift;;
        -jvmOptions) jvmOptions="$2"; shift;;
        -*) notset="true"; break;;
        *) break;;
    esac
    shift
done
```
