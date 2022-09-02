## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:3c8a5d7e4326a90334e48f9a98db2e4de16d3104f18f1df774f625e0aaebe727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:d21f9b6f3255e9ac068c97b7c44ceceb961f824348d24aa405075c8888c97bba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394275333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa2091eb1e3f692ba864e213cb2a3fe85103a0aa6fd18cf62ad2f448f598d06`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:04:25 GMT
RUN apt-get update && apt-get install -y       gnupg
# Fri, 02 Sep 2022 04:04:27 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 02 Sep 2022 04:06:28 GMT
COPY file:1e70d8fd6f9643bffb703528edddba0aa02a58e95cc53e92f58a86cde29e732a in /etc/apt/sources.list.d/zend-server.list 
# Fri, 02 Sep 2022 04:07:56 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2021.0.0+b74     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 02 Sep 2022 04:07:59 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 02 Sep 2022 04:07:59 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 02 Sep 2022 04:07:59 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Fri, 02 Sep 2022 04:08:00 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Fri, 02 Sep 2022 04:08:00 GMT
WORKDIR /usr/local/zs-init
# Fri, 02 Sep 2022 04:08:05 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Fri, 02 Sep 2022 04:08:05 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Fri, 02 Sep 2022 04:08:06 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 02 Sep 2022 04:08:06 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Fri, 02 Sep 2022 04:08:06 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 02 Sep 2022 04:08:06 GMT
EXPOSE 80
# Fri, 02 Sep 2022 04:08:06 GMT
EXPOSE 443
# Fri, 02 Sep 2022 04:08:07 GMT
EXPOSE 10081
# Fri, 02 Sep 2022 04:08:07 GMT
EXPOSE 10082
# Fri, 02 Sep 2022 04:08:07 GMT
WORKDIR /var/www/html
# Fri, 02 Sep 2022 04:08:07 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2483171250a877cac43a39d4118a7a1a5352b6aa4fefdbd39cbd69436775977`  
		Last Modified: Fri, 02 Sep 2022 04:08:42 GMT  
		Size: 36.2 MB (36199533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1404aa294ceed97c2d28eb13104e183929b2c7935fc0c34b896ae860703fe97a`  
		Last Modified: Fri, 02 Sep 2022 04:08:38 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6df8f3fc6ba8f879a6dcdac11eb811f8c41f61965bf916d9e4a077ecfe5514e`  
		Last Modified: Fri, 02 Sep 2022 04:09:39 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8330bcd8a316e9236c1736f301ec45feaa66565fc44bbecd0c323b2cb8f5736`  
		Last Modified: Fri, 02 Sep 2022 04:10:23 GMT  
		Size: 326.0 MB (326016250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce4ca4ccfc68d03419fdd378ffecca724e359d004fd9717bcb2c0a6ddcef397`  
		Last Modified: Fri, 02 Sep 2022 04:09:39 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45772804b31cf62c805a6b9f5b3bc784aa16c8bdf961091800d187a87af58866`  
		Last Modified: Fri, 02 Sep 2022 04:09:39 GMT  
		Size: 18.9 KB (18930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a67ed4a2f1525e2fca5045c9dff3f051b3d8945abe0a7a2d673254684d0aa3`  
		Last Modified: Fri, 02 Sep 2022 04:09:38 GMT  
		Size: 5.3 MB (5310172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1ad981d5935ab7df541768b10b45e50a868498a27b8204cb158cfa048d7c33`  
		Last Modified: Fri, 02 Sep 2022 04:09:37 GMT  
		Size: 14.3 KB (14292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d3c898a290691b0987473437a6579b8458765998b5642f18ac154ea28c1b62`  
		Last Modified: Fri, 02 Sep 2022 04:09:37 GMT  
		Size: 2.6 KB (2558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff58dea59e8d66348ef47f7f3d481737fb6b174666b9e2f897c58fb6ae26a865`  
		Last Modified: Fri, 02 Sep 2022 04:09:37 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426b72c63169409f8b5566deb8e02dfdb441576194f9517a84449ca408a5ba6b`  
		Last Modified: Fri, 02 Sep 2022 04:09:37 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
