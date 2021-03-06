## `jetty:9-alpine`

```console
$ docker pull jetty@sha256:2a7ee6abf5b167ca227c5ec3ef2a75a2e796d136459e2a3c28d17757bde193b1
```

-	Platforms:
	-	linux; amd64

### `jetty:9-alpine` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63787893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf593d9f2d522bddebadaaf9f966cfdba2a39c9fe84a3a1958e4e290b3ea436`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Tue, 07 Mar 2017 01:03:58 GMT
ENV LANG=C.UTF-8
# Tue, 07 Mar 2017 01:03:59 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 07 Mar 2017 01:04:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Tue, 07 Mar 2017 01:04:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 07 Mar 2017 01:04:10 GMT
ENV JAVA_VERSION=8u121
# Tue, 07 Mar 2017 01:04:10 GMT
ENV JAVA_ALPINE_VERSION=8.121.13-r0
# Tue, 07 Mar 2017 01:04:15 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 07 Mar 2017 18:32:08 GMT
RUN addgroup -S jetty && adduser -D -S -H -G jetty jetty && rm -rf /etc/group- /etc/passwd- /etc/shadow-
# Tue, 07 Mar 2017 18:32:08 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 07 Mar 2017 18:32:09 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 07 Mar 2017 18:32:10 GMT
RUN mkdir -p "$JETTY_HOME"
# Tue, 07 Mar 2017 18:32:11 GMT
WORKDIR /usr/local/jetty
# Thu, 30 Mar 2017 16:54:06 GMT
ENV JETTY_VERSION=9.4.3.v20170317
# Thu, 30 Mar 2017 16:54:06 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.3.v20170317/jetty-home-9.4.3.v20170317.tar.gz
# Thu, 30 Mar 2017 16:54:07 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D
# Thu, 30 Mar 2017 16:54:14 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps gnupg curl 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -r "$GNUPGHOME" 	&& tar -xvzf jetty.tar.gz 	&& mv jetty-home-$JETTY_VERSION/* ./ 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -fr jetty-home-$JETTY_VERSION/ 	&& apk del .build-deps 	&& rm -fr .build-deps 	&& rm -rf /tmp/hsperfdata_root
# Thu, 30 Mar 2017 16:54:15 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 30 Mar 2017 16:54:15 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 30 Mar 2017 16:54:16 GMT
WORKDIR /var/lib/jetty
# Thu, 30 Mar 2017 16:54:20 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket,setuid" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 30 Mar 2017 16:54:20 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 30 Mar 2017 16:54:21 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 30 Mar 2017 16:54:22 GMT
COPY file:4f7da2906a90932cfb90db54a45ee08f86b17253747db62085f7512c9efd46ad in / 
# Thu, 30 Mar 2017 16:54:22 GMT
EXPOSE 8080/tcp
# Thu, 30 Mar 2017 16:54:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Mar 2017 16:54:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:627beaf3eaaff1c0bc3311d60fb933c17ad04fe377e1043d9593646d8ae3bfe1`  
		Last Modified: Fri, 03 Mar 2017 20:34:41 GMT  
		Size: 1.9 MB (1905270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de20f2d8b839756d5fc0ae6871096666a822b6b4205e11e9cf438a2263f3281`  
		Last Modified: Tue, 07 Mar 2017 01:12:49 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e619d348278f1e8660192734bff496a6c3e05aab6bef025e843e7413a7c9e3`  
		Last Modified: Tue, 07 Mar 2017 01:15:49 GMT  
		Size: 53.8 MB (53811092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc50397aaa0047c7318d309311d2cfc30eb6092aae3d70e18e31eeaaedb55ff`  
		Last Modified: Tue, 07 Mar 2017 18:36:58 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7103831d767254a90fc2d42a94d80076e918ad3601050efde7c1202ce66ccc8`  
		Last Modified: Tue, 07 Mar 2017 18:36:58 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1719bc507591aa8bafa49bd9b08530423acdd227e61e845af4197fdafce1b7`  
		Last Modified: Thu, 30 Mar 2017 16:57:59 GMT  
		Size: 8.1 MB (8066972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7021369e992a12d98a67767a5c96ab10024fc633b4df612944529032169649`  
		Last Modified: Thu, 30 Mar 2017 16:57:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5d5231a453329fb83af744bb1e342ec0cd2c15c30aed768bf2bfad78f2261f`  
		Last Modified: Thu, 30 Mar 2017 16:57:58 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a87ed2b2dd4800276ef690476db1c449c7a041588923639edbdb1497abba21`  
		Last Modified: Thu, 30 Mar 2017 16:57:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78670f8004e91eca1965c60b6b5c347726735674be98cb922a1d13f0ac2e23cb`  
		Last Modified: Thu, 30 Mar 2017 16:57:58 GMT  
		Size: 571.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
