# kubectl options

The following options can be passed to any command:

+ **`--alsologtostderr=false`**:
log to standard error as well as files

+ **`--application-metrics-count-limit=100`**:
Max number of application metrics to store (per container)

+ **`--as=''`**:
Username to impersonate for the operation

+ **`--as-group=[]`**:
Group to impersonate for the operation, this flag can be repeated to specify multiple groups.

+ **`--azure-container-registry-config=''`**:
Path to the file containing Azure container registry configuration information.

+ **`--boot-id-file='/proc/sys/kernel/random/boot_id'`**:
Comma-separated list of files to check for boot-id. Use the first one that exists.

+ **`--cache-dir='/root/.kube/http-cache'`**:
Default HTTP cache directory

+ **`--certificate-authority=''`**:
Path to a cert file for the certificate authority

+ **`--client-certificate=''`**:
Path to a client certificate file for TLS

+ **`--client-key=''`**:
Path to a client key file for TLS

+ **`--cloud-provider-gce-lb-src-cidrs=130.211.0.0/22,209.85.152.0/22,209.85.204.0/22,35.191.0.0/16`**:
CIDRs opened in GCE firewall for LB traffic proxy & health checks

+ **`--cluster=''`**:
The name of the kubeconfig cluster to use

+ **`--container-hints='/etc/cadvisor/container_hints.json'`**:
location of the container hints file

+ **`--containerd='unix:///var/run/containerd.sock'`**:
containerd endpoint

+ **`--context=''`**:
The name of the kubeconfig context to use

+ **`--default-not-ready-toleration-seconds=300`**:
Indicates the tolerationSeconds of the toleration for notReady:NoExecute that is added by default to every pod that does not already have such a toleration.

+ **`--default-unreachable-toleration-seconds=300`**:
Indicates the tolerationSeconds of the toleration for unreachable:NoExecute that is added by default to every pod that does not already have such a toleration.

+ **`--docker='unix:///var/run/docker.sock'`**:
docker endpoint

+ **`--docker-env-metadata-whitelist=''`**:
a comma-separated list of environment variable keys that needs to be collected for docker containers

+ **`--docker-only=false`**:
Only report docker containers in addition to root stats

+ **`--docker-root='/var/lib/docker'`**:
DEPRECATED: docker root is read from docker info (this is a fallback, default: /var/lib/docker)

+ **`--docker-tls=false`**:
use TLS to connect to docker

+ **`--docker-tls-ca='ca.pem'`**:
path to trusted CA

+ **`--docker-tls-cert='cert.pem'`**:
path to client certificate

+ **`--docker-tls-key='key.pem'`**:
path to private key

+ **`--enable-load-reader=false`**:
Whether to enable cpu load reader

+ **`--event-storage-age-limit='default=0'`**:
Max length of time for which to store events (per type). Value is a comma separated list of key values, where the keys are event types (e.g.: creation, oom) or "default" and the value is a duration. Default is applied to all non-specified event types

+ **`--event-storage-event-limit='default=0'`**:
Max number of events to store (per type). Value is a comma separated list of key values, where the keys are event types (e.g.: creation, oom) or "default" and the value is an integer. Default is applied to all non-specified event types

+ **`--global-housekeeping-interval=1m0s`**:
Interval between global housekeepings

+ **`--housekeeping-interval=10s`**:
Interval between container housekeepings

+ **`--insecure-skip-tls-verify=false`**:
If true, the server's certificate will not be checked for validity. This will make your HTTPS connections insecure

+ **`--kubeconfig=''`**:
Path to the kubeconfig file to use for CLI requests.

+ **`--log-backtrace-at=:0`**:
when logging hits line file:N, emit a stack trace

+ **`--log-cadvisor-usage=false`**:
Whether to log the usage of the cAdvisor container

+ **`--log-dir=''`**:
If non-empty, write log files in this directory

+ **`--log-file=''`**:
If non-empty, use this log file

+ **`--log-flush-frequency=5s`**:
Maximum number of seconds between log flushes

+ **`--logtostderr=true`**:
log to standard error instead of files

+ **`--machine-id-file='/etc/machine-id,/var/lib/dbus/machine-id'`**:
Comma-separated list of files to check for machine-id. Use the first one that exists.

+ **`--match-server-version=false`**:
Require server version to match client version

+ **`--mesos-agent='127.0.0.1:5051'`**:
Mesos agent address

+ **`--mesos-agent-timeout=10s`**:
Mesos agent timeout

+ **`--namespace, -n=''`**:
If present, the namespace scope for this CLI request

+ **`--profile='none'`**:
Name of profile to capture. One of (none|cpu|heap|goroutine|threadcreate|block|mutex)

+ **`--profile-output='profile.pprof'`**:
Name of the file to write the profile to

+ **`--request-timeout='0'`**:
The length of time to wait before giving up on a single server request. Non-zero values should contain a corresponding time unit (e.g. 1s, 2m, 3h). A value of zero means don't timeout requests.

+ **`--server, -s=''`**:
The address and port of the Kubernetes API server

+ **`--skip-headers=false`**:
If true, avoid header prefixes in the log messages

+ **`--stderrthreshold=2`**:
logs at or above this threshold go to stderr

+ **`--storage-driver-buffer-duration=1m0s`**:
Writes in the storage driver will be buffered for this duration, and committed to the non memory backends as a single transaction

+ **`--storage-driver-db='cadvisor'`**:
database name

+ **`--storage-driver-host='localhost:8086'`**:
database host:port

+ **`--storage-driver-password='root'`**:
database password

+ **`--storage-driver-secure=false`**:
use secure connection with database

+ **`--storage-driver-table='stats'`**:
table name

+ **`--storage-driver-user='root'`**:
database username

+ **`--token=''`**:
Bearer token for authentication to the API server

+ **`--user=''`**:
The name of the kubeconfig user to use

+ **`--v, -v=0`**:
log level for V logs

+ **`--version=false`**:
Print version information and quit

+ **`--vmodule=`**:
comma-separated list of pattern=N settings for file-filtered logging


