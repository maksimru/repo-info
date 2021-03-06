## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:9257be802bdecc1801c651a0d5a179a22819e458439d11c3776920e2fa96b6b0
```

-	Platforms:
	-	linux; amd64

### `rabbitmq:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86339204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc5f4e7fb9033b65b943089d14ef7c0ea9b296a4f1845453a970c7b8b542ea4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 23:55:41 GMT
RUN groupadd -r rabbitmq && useradd -r -d /var/lib/rabbitmq -m -g rabbitmq rabbitmq
# Tue, 21 Mar 2017 23:55:41 GMT
ENV GOSU_VERSION=1.7
# Tue, 21 Mar 2017 23:55:56 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 21 Mar 2017 23:55:58 GMT
RUN set -ex; 	key='434975BD900CCBE4F7EE1B1ED208507CA14F4FCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/erlang-solutions.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 21 Mar 2017 23:55:59 GMT
RUN echo 'deb http://packages.erlang-solutions.com/debian jessie contrib' > /etc/apt/sources.list.d/erlang.list
# Tue, 21 Mar 2017 23:56:26 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		erlang-asn1 		erlang-base-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang-nox 		erlang-os-mon 		erlang-public-key 		erlang-ssl 		erlang-xmerl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 23:56:27 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Tue, 21 Mar 2017 23:56:28 GMT
RUN set -ex; 	key='0A9AF2115F4687BD29803A206B73A36E6026DFCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/rabbitmq.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 21 Mar 2017 23:56:29 GMT
RUN echo 'deb http://www.rabbitmq.com/debian testing main' > /etc/apt/sources.list.d/rabbitmq.list
# Thu, 30 Mar 2017 22:06:44 GMT
ENV RABBITMQ_VERSION=3.6.9
# Thu, 30 Mar 2017 22:06:44 GMT
ENV RABBITMQ_DEBIAN_VERSION=3.6.9-1
# Thu, 30 Mar 2017 22:06:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		rabbitmq-server=$RABBITMQ_DEBIAN_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 30 Mar 2017 22:06:53 GMT
ENV PATH=/usr/lib/rabbitmq/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2017 22:06:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 07 Apr 2017 19:47:23 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq
# Fri, 07 Apr 2017 19:47:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 07 Apr 2017 19:47:25 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Fri, 07 Apr 2017 19:47:26 GMT
RUN ln -sf /usr/lib/rabbitmq/lib/rabbitmq_server-$RABBITMQ_VERSION/plugins /plugins
# Tue, 11 Apr 2017 22:49:02 GMT
COPY file:e75247400159c3b996450d9b4ef7078cf9587833f465ab2904b2b7ef35be65e9 in /usr/local/bin/ 
# Tue, 11 Apr 2017 22:49:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 11 Apr 2017 22:49:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Apr 2017 22:49:06 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Tue, 11 Apr 2017 22:49:06 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd4bdc20139db8db58fec0f4a518b99398d45daf9441718486d45d9db598433`  
		Last Modified: Fri, 24 Mar 2017 00:24:05 GMT  
		Size: 4.3 KB (4339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7e941d26a17bc9c96b6a521a3158cbaaf2ea3aca820b592c48a3f161e00ad4`  
		Last Modified: Fri, 24 Mar 2017 00:24:06 GMT  
		Size: 1.3 MB (1288976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3820e0134b494cc49b4021fbf5a3e96585cbda482c3000eb7a3daaca0fea1b`  
		Last Modified: Fri, 24 Mar 2017 00:24:05 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2faf50c361a52b8fe4a1278089842b2366cc93ff43cd62f59c9008d80538e619`  
		Last Modified: Fri, 24 Mar 2017 00:24:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbe921a0db61127d93a2f75076ac5157d71720477ff223fcee62b2bd09f4a1d`  
		Last Modified: Fri, 24 Mar 2017 00:24:10 GMT  
		Size: 27.9 MB (27929946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45725958e87d117a7c30ad77199e3e9d9d3b1cfa1ee05478f77891e1eb875bf`  
		Last Modified: Fri, 24 Mar 2017 00:24:03 GMT  
		Size: 3.1 KB (3101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e6d2a1c35119945183bdbb31c9333c34193bad77e51981547853c07dfdb73f`  
		Last Modified: Fri, 24 Mar 2017 00:24:03 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043dd583fc3ed60ee63b2d1d3653d587e16971825aea72862f83ce784368353c`  
		Last Modified: Thu, 30 Mar 2017 22:07:51 GMT  
		Size: 5.7 MB (5664781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26318044f824fd82affc93cebb96c25eecba30c01e4e666b2b8b10970f5924c`  
		Last Modified: Fri, 07 Apr 2017 19:48:09 GMT  
		Size: 2.2 KB (2236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a7dc1a393fb4ed52f57f9b15d022faf4b20bfd6282431b3158349ec1fd1a81`  
		Last Modified: Fri, 07 Apr 2017 19:48:09 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ac40b7ecec0a2b788bfede2cd98d490d00fd6f37e3d528a1b4d54edd3ca52b`  
		Last Modified: Fri, 07 Apr 2017 19:48:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6918ca794075daf9110d9fc2ed8f34a89c6dafabc278732df318ad8ff15ef7d3`  
		Last Modified: Tue, 11 Apr 2017 22:49:49 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f585f9aaf4d7bdf53f851fc11faa9269a8d6389492e1f12c35ecdd120ec6014`  
		Last Modified: Tue, 11 Apr 2017 22:49:49 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
