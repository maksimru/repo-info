## `orientdb:latest`

```console
$ docker pull orientdb@sha256:c11d56f4850fd668638de877196b423360e860860fc6d0bc21f56c37890bfaa5
```

-	Platforms:
	-	linux; amd64

### `orientdb:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114778324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6597b53ff5e17415f3844fea91e01040e3ad0d1062a49bd46ca2e491d915160f`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Tue, 07 Mar 2017 01:03:58 GMT
ENV LANG=C.UTF-8
# Tue, 07 Mar 2017 01:03:59 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 07 Mar 2017 01:04:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Tue, 07 Mar 2017 01:04:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 07 Mar 2017 01:04:01 GMT
ENV JAVA_VERSION=8u121
# Tue, 07 Mar 2017 01:04:01 GMT
ENV JAVA_ALPINE_VERSION=8.121.13-r0
# Tue, 07 Mar 2017 01:04:07 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 07 Mar 2017 19:43:39 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Mar 2017 19:43:54 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 06 Apr 2017 20:14:18 GMT
ENV ORIENTDB_VERSION=2.2.18
# Thu, 06 Apr 2017 20:14:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=dc92356f8fc488208f3c5f272e418fb3
# Thu, 06 Apr 2017 20:14:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=dc866f6b8be40eec43b71fbee3548ec8b2f423e6
# Thu, 06 Apr 2017 20:14:19 GMT
ENV ORIENTDB_DOWNLOAD_URL=http://central.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.18/orientdb-community-2.2.18.tar.gz
# Thu, 06 Apr 2017 20:14:20 GMT
RUN apk add --update tar curl     && rm -rf /var/cache/apk/*
# Thu, 06 Apr 2017 20:14:25 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 06 Apr 2017 20:14:26 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 06 Apr 2017 20:14:26 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 06 Apr 2017 20:14:26 GMT
WORKDIR /orientdb
# Thu, 06 Apr 2017 20:14:27 GMT
EXPOSE 2424/tcp
# Thu, 06 Apr 2017 20:14:27 GMT
EXPOSE 2480/tcp
# Thu, 06 Apr 2017 20:14:28 GMT
CMD ["server.sh"]
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
	-	`sha256:3e00029ebfe30f96f53c89cd3c838b89876ee212cbb545e8ac5c70698c1818f1`  
		Last Modified: Tue, 07 Mar 2017 01:12:59 GMT  
		Size: 69.6 MB (69564916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23be3fafbe89ee8f43955aaf088e412340d9df64fb6f600b2f70cc6728a95754`  
		Last Modified: Thu, 06 Apr 2017 20:15:41 GMT  
		Size: 622.5 KB (622493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75607aab8914eb26c28660e076647c3fd1a4fa6913203c2c4e42f44473cf603`  
		Last Modified: Thu, 06 Apr 2017 20:15:46 GMT  
		Size: 42.7 MB (42685413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
