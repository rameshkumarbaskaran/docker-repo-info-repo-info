## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:24814f1b4cfe12e3aaa104aed181c6aee3b00148ef4492bcfdc31152f4a9dc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:6bbe477fe3c81def043ce3aa3e6f082d51a9983e6c906ff3c2f6201d9b230df8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.3 MB (391250990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab00502b2a986700b2fafdc89faf5444016260b4b6919501afab35ee391704b1`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:43:09 GMT
RUN apt-get update && apt-get install -y       gnupg
# Fri, 18 Jun 2021 04:43:10 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 18 Jun 2021 04:45:27 GMT
COPY file:1e70d8fd6f9643bffb703528edddba0aa02a58e95cc53e92f58a86cde29e732a in /etc/apt/sources.list.d/zend-server.list 
# Fri, 18 Jun 2021 04:46:59 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2021.0.0+b74     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 18 Jun 2021 04:47:02 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 18 Jun 2021 04:47:03 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 18 Jun 2021 04:47:03 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Fri, 18 Jun 2021 04:47:04 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Fri, 18 Jun 2021 04:47:04 GMT
WORKDIR /usr/local/zs-init
# Fri, 18 Jun 2021 04:47:09 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Fri, 18 Jun 2021 04:47:10 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Fri, 18 Jun 2021 04:47:10 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 18 Jun 2021 04:47:11 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Fri, 18 Jun 2021 04:47:11 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 18 Jun 2021 04:47:11 GMT
EXPOSE 80
# Fri, 18 Jun 2021 04:47:12 GMT
EXPOSE 443
# Fri, 18 Jun 2021 04:47:12 GMT
EXPOSE 10081
# Fri, 18 Jun 2021 04:47:12 GMT
EXPOSE 10082
# Fri, 18 Jun 2021 04:47:12 GMT
WORKDIR /var/www/html
# Fri, 18 Jun 2021 04:47:12 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536290a811a9179d6382b466707053ad0ee85c0fb032e75084cef77ac6a03136`  
		Last Modified: Fri, 18 Jun 2021 04:49:29 GMT  
		Size: 32.9 MB (32876343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747fc8577b5436cf166399a6ba5d19e8940c3764202c8b6e14479eb84bc8ede9`  
		Last Modified: Fri, 18 Jun 2021 04:49:24 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c0cfe7cb1351190c998322ca84c71f9eb02a5caa63a6e3b24c61fb8523c8a0`  
		Last Modified: Fri, 18 Jun 2021 04:50:30 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc25dfee1254c12262639d59e81f91e2b0b3357b5aa68bf962a386b138e3efc`  
		Last Modified: Fri, 18 Jun 2021 04:51:16 GMT  
		Size: 326.5 MB (326487090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8822f69ca2d8d4c45249a89e247bf0ff48acc7c880092a169eb60cff39fa6b87`  
		Last Modified: Fri, 18 Jun 2021 04:50:30 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3850592cb1b1b6d570795961d01695c39a4ad3ac4da644051b809bd234ae798`  
		Last Modified: Fri, 18 Jun 2021 04:50:30 GMT  
		Size: 18.9 KB (18929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ec9e33ded17542b8212353a810d27e82040894fec444348050495b9953e86f`  
		Last Modified: Fri, 18 Jun 2021 04:50:28 GMT  
		Size: 5.1 MB (5147556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e454f2ddb5ddfffcbd3569923b7190dc5af1d2f7662c5340bd2bddaaa563469`  
		Last Modified: Fri, 18 Jun 2021 04:50:27 GMT  
		Size: 14.3 KB (14294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8ec627b06a03993ebc4f374563b74fa1d58b527fb86684c40821dd10a892b1`  
		Last Modified: Fri, 18 Jun 2021 04:50:27 GMT  
		Size: 2.6 KB (2558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf7b2de152519be95a495cb7999fe6ed75077b48dbb199ea8e17f4ffd3407`  
		Last Modified: Fri, 18 Jun 2021 04:50:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c06ee456c1830192299e86f72813e0ea4c6dd9c48c61a25bf390826dc04a1ef`  
		Last Modified: Fri, 18 Jun 2021 04:50:27 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
