## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:02fd3f5049a9314f37dba4d9490740c2e4cef275c0d610fa0fc00d7cc0d86939
```

-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444a7a74ca1d5f7c2e5aaf0d3bcb30c885ecb62f3b4f9b8dad5d07de266c4eea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Wed, 12 Apr 2017 18:58:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 12 Apr 2017 19:05:20 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 12 Apr 2017 19:05:36 GMT
ENV KAPACITOR_VERSION=1.2.0
# Wed, 12 Apr 2017 19:05:43 GMT
RUN apk add --no-cache --virtual .build-deps wget gnupg tar &&     gpg --keyserver hkp://ha.pool.sks-keyservers.net         --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 12 Apr 2017 19:05:44 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Wed, 12 Apr 2017 19:05:45 GMT
EXPOSE 9092/tcp
# Wed, 12 Apr 2017 19:05:46 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 12 Apr 2017 19:05:47 GMT
COPY file:440a837280df72a19ed72b91fab9bdcfd268250b241bbc22509699f880fe0d17 in /entrypoint.sh 
# Wed, 12 Apr 2017 19:05:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Apr 2017 19:05:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:627beaf3eaaff1c0bc3311d60fb933c17ad04fe377e1043d9593646d8ae3bfe1`  
		Last Modified: Fri, 03 Mar 2017 20:34:41 GMT  
		Size: 1.9 MB (1905270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827570184fa82dc6defc05bcf5838dba590096d8add32bb847191bd7232cfcba`  
		Last Modified: Wed, 12 Apr 2017 19:02:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a07567aee09be1af1aec1476fe3261b0b717c05954d31456c578c63429e532`  
		Last Modified: Wed, 12 Apr 2017 19:06:54 GMT  
		Size: 352.8 KB (352777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628cbe9044eaaf81aec82c9f6850ad571553d6fdfa7385b14ae3ec2af712c93f`  
		Last Modified: Wed, 12 Apr 2017 19:08:47 GMT  
		Size: 7.0 MB (6965173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d790bb33714ae68b1c1a7fd00cdbf2972f9a1d564651f1880a7caf330edfb05`  
		Last Modified: Wed, 12 Apr 2017 19:08:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c519489147d06c28fcd9ac8638eea05d1f062ad041141d81c3fe4f6b946d744`  
		Last Modified: Wed, 12 Apr 2017 19:08:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
