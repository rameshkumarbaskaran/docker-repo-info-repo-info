<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `php-zendserver`

-	[`php-zendserver:2019.0`](#php-zendserver20190)
-	[`php-zendserver:5.6`](#php-zendserver56)
-	[`php-zendserver:8.5`](#php-zendserver85)
-	[`php-zendserver:8.5-php5.6`](#php-zendserver85-php56)
-	[`php-zendserver:9.1`](#php-zendserver91)
-	[`php-zendserver:latest`](#php-zendserverlatest)

## `php-zendserver:2019.0`

```console
$ docker pull php-zendserver@sha256:d6d8150ca026599fc9cfcd43bf4a400a69d65d843ae2b2ee8c38fa4655e9b8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:7ae43d5f682b305bd6bf7ecba54e0be70588e9b8e455de81dd23a0117eac27a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.3 MB (482291313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a99bb4946e695c411a209507267e76309635f1884eee72178f185e98ff281a`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:19:48 GMT
RUN apt-get update && apt-get install -y       gnupg
# Fri, 26 Mar 2021 12:19:49 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 26 Mar 2021 12:19:49 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 26 Mar 2021 12:21:43 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.7+b403     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 26 Mar 2021 12:21:46 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 26 Mar 2021 12:21:46 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 26 Mar 2021 12:21:47 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Fri, 26 Mar 2021 12:21:48 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Fri, 26 Mar 2021 12:21:48 GMT
WORKDIR /usr/local/zs-init
# Fri, 26 Mar 2021 12:21:53 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Fri, 26 Mar 2021 12:21:53 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Fri, 26 Mar 2021 12:21:54 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 26 Mar 2021 12:21:54 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Fri, 26 Mar 2021 12:21:55 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 26 Mar 2021 12:21:55 GMT
EXPOSE 80
# Fri, 26 Mar 2021 12:21:55 GMT
EXPOSE 443
# Fri, 26 Mar 2021 12:21:55 GMT
EXPOSE 10081
# Fri, 26 Mar 2021 12:21:55 GMT
EXPOSE 10082
# Fri, 26 Mar 2021 12:21:56 GMT
WORKDIR /var/www/html
# Fri, 26 Mar 2021 12:21:56 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09e9fb21ea14f3d4fd3e0eb488f5fbf7e4b0ab58cdb70cb7caa708fe04c3ed8`  
		Last Modified: Fri, 26 Mar 2021 12:24:49 GMT  
		Size: 32.3 MB (32313870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d842d28e5b2934da62e3393a05d3ca8905f51b2abf4652e0098bd4f8cb5c8570`  
		Last Modified: Fri, 26 Mar 2021 12:24:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1bef7a9258fbbc984d3d84da120330fb50816634221752630f98e20d9de157`  
		Last Modified: Fri, 26 Mar 2021 12:24:43 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2430d61861afed165bec80e5395d05d244229764018cabf8bb8667a41762a3`  
		Last Modified: Fri, 26 Mar 2021 12:26:02 GMT  
		Size: 418.1 MB (418085079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e994fa72fcecb985b9f316c77dfb9ff6803c74cb9fc342f2b61a8b4e51a6e052`  
		Last Modified: Fri, 26 Mar 2021 12:24:42 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6d603ea63961f890aceb5d9626d1d4457ae482f29d27ad7f1ed2ebe398fa99`  
		Last Modified: Fri, 26 Mar 2021 12:24:42 GMT  
		Size: 18.9 KB (18928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6084673048196810d230d49e5f235fa815c086d8468451e5302f7f27492ecf50`  
		Last Modified: Fri, 26 Mar 2021 12:24:40 GMT  
		Size: 5.1 MB (5141254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2951fc02fdf1e381fc6a8ef9e59c421b5bab3e4bcc5c3bb566268c692854bbe`  
		Last Modified: Fri, 26 Mar 2021 12:24:40 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7e9ccf42ae3ade52793d46430d753b09efb4c587f3d0064f3db6de3da3b006`  
		Last Modified: Fri, 26 Mar 2021 12:24:39 GMT  
		Size: 2.6 KB (2556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b953d70d86e29477f45306d26c65f39f1c3bbed4b69c5a38629eacd8d1b2f8`  
		Last Modified: Fri, 26 Mar 2021 12:24:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc2296c2ef763ad8cf55b5d2ff3d435857fa215481f2ea84a6ef49de24f27cf`  
		Last Modified: Fri, 26 Mar 2021 12:24:39 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:5.6`

```console
$ docker pull php-zendserver@sha256:f2d94b35b1c3ec31852e7af4addaed8e22d696d3c4b116b3f4438980c71cc16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:2098726c37868a61a26c88e56a6afc079e228b78ff0c1cfe1cb7b40db7c680a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315053224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfab47bee7a0b78d23540d97b5b7c2ab951c5f96bf9609491df0c212c3be281f`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:14:46 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 26 Mar 2021 12:14:47 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 26 Mar 2021 12:14:47 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Fri, 26 Mar 2021 12:17:12 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 26 Mar 2021 12:17:15 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 26 Mar 2021 12:17:16 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 26 Mar 2021 12:17:17 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 26 Mar 2021 12:17:17 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 26 Mar 2021 12:17:18 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 26 Mar 2021 12:17:19 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 26 Mar 2021 12:17:19 GMT
WORKDIR /usr/local/zs-init
# Fri, 26 Mar 2021 12:17:25 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 26 Mar 2021 12:17:26 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Fri, 26 Mar 2021 12:17:26 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 26 Mar 2021 12:17:27 GMT
RUN rm /var/www/html/index.html
# Fri, 26 Mar 2021 12:17:27 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 26 Mar 2021 12:17:27 GMT
EXPOSE 80
# Fri, 26 Mar 2021 12:17:27 GMT
EXPOSE 443
# Fri, 26 Mar 2021 12:17:27 GMT
EXPOSE 10081
# Fri, 26 Mar 2021 12:17:28 GMT
EXPOSE 10082
# Fri, 26 Mar 2021 12:17:28 GMT
WORKDIR /var/www/html
# Fri, 26 Mar 2021 12:17:28 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ed2a06918c59f99afa96b26b1048e13a36edfd0d339f2219cafc52ed3e35bd`  
		Last Modified: Fri, 26 Mar 2021 12:22:21 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf8cf273b118511038c36413cedc7b8038dca97c11a94a18b5f750492024d26`  
		Last Modified: Fri, 26 Mar 2021 12:22:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e773af4a7db297c6c81102f7a28b05d615cfbda22843b2712859b1a2a4bf754`  
		Last Modified: Fri, 26 Mar 2021 12:22:19 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db2c30b3d8eed72807bc4644eea9b964545dca7c26a236494f0569142f19a29`  
		Last Modified: Fri, 26 Mar 2021 12:22:54 GMT  
		Size: 263.9 MB (263899625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a86f7bd15171ed896e62af2b55a4a2951f830f892b5bb4c4e1f480a54c05beb`  
		Last Modified: Fri, 26 Mar 2021 12:22:19 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219c8d091928daa2f5a00bae617f9001f5a8cc5a98e914a145bc06f1a738b5c`  
		Last Modified: Fri, 26 Mar 2021 12:22:18 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a18bc500dca062574ff9117727e1fc68d205dcc832a3b2f83eaf2f09979d94`  
		Last Modified: Fri, 26 Mar 2021 12:22:17 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b484de6008de19b916b6ab647d61ab6244fec6deca555abe66ac20b687b8102c`  
		Last Modified: Fri, 26 Mar 2021 12:22:17 GMT  
		Size: 18.9 KB (18858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e7aa9741d48f2c8dd29d7bb560afc801c3bfc4e698d34ab18d86edb0f30595`  
		Last Modified: Fri, 26 Mar 2021 12:22:15 GMT  
		Size: 5.1 MB (5137391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a556126f0399975b398d3c78e9f3072902ed7ae804e7d536963ab2912e026d15`  
		Last Modified: Fri, 26 Mar 2021 12:22:17 GMT  
		Size: 13.3 KB (13348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761f90ca44a1452aca0727a1c837e71855512b2d81b5db8623c71015bb9258ea`  
		Last Modified: Fri, 26 Mar 2021 12:22:14 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a292ed6a0d56d9db966547179c378ec0f61dab48738f2eb25420f12406687b`  
		Last Modified: Fri, 26 Mar 2021 12:22:15 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712cf0f1c4988d608e22090fcfb16531c1fd25fc63fa0b3e3ddba6aad93d819a`  
		Last Modified: Fri, 26 Mar 2021 12:22:14 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5`

```console
$ docker pull php-zendserver@sha256:f2d94b35b1c3ec31852e7af4addaed8e22d696d3c4b116b3f4438980c71cc16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5` - linux; amd64

```console
$ docker pull php-zendserver@sha256:2098726c37868a61a26c88e56a6afc079e228b78ff0c1cfe1cb7b40db7c680a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315053224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfab47bee7a0b78d23540d97b5b7c2ab951c5f96bf9609491df0c212c3be281f`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:14:46 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 26 Mar 2021 12:14:47 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 26 Mar 2021 12:14:47 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Fri, 26 Mar 2021 12:17:12 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 26 Mar 2021 12:17:15 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 26 Mar 2021 12:17:16 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 26 Mar 2021 12:17:17 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 26 Mar 2021 12:17:17 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 26 Mar 2021 12:17:18 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 26 Mar 2021 12:17:19 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 26 Mar 2021 12:17:19 GMT
WORKDIR /usr/local/zs-init
# Fri, 26 Mar 2021 12:17:25 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 26 Mar 2021 12:17:26 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Fri, 26 Mar 2021 12:17:26 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 26 Mar 2021 12:17:27 GMT
RUN rm /var/www/html/index.html
# Fri, 26 Mar 2021 12:17:27 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 26 Mar 2021 12:17:27 GMT
EXPOSE 80
# Fri, 26 Mar 2021 12:17:27 GMT
EXPOSE 443
# Fri, 26 Mar 2021 12:17:27 GMT
EXPOSE 10081
# Fri, 26 Mar 2021 12:17:28 GMT
EXPOSE 10082
# Fri, 26 Mar 2021 12:17:28 GMT
WORKDIR /var/www/html
# Fri, 26 Mar 2021 12:17:28 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ed2a06918c59f99afa96b26b1048e13a36edfd0d339f2219cafc52ed3e35bd`  
		Last Modified: Fri, 26 Mar 2021 12:22:21 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf8cf273b118511038c36413cedc7b8038dca97c11a94a18b5f750492024d26`  
		Last Modified: Fri, 26 Mar 2021 12:22:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e773af4a7db297c6c81102f7a28b05d615cfbda22843b2712859b1a2a4bf754`  
		Last Modified: Fri, 26 Mar 2021 12:22:19 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db2c30b3d8eed72807bc4644eea9b964545dca7c26a236494f0569142f19a29`  
		Last Modified: Fri, 26 Mar 2021 12:22:54 GMT  
		Size: 263.9 MB (263899625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a86f7bd15171ed896e62af2b55a4a2951f830f892b5bb4c4e1f480a54c05beb`  
		Last Modified: Fri, 26 Mar 2021 12:22:19 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219c8d091928daa2f5a00bae617f9001f5a8cc5a98e914a145bc06f1a738b5c`  
		Last Modified: Fri, 26 Mar 2021 12:22:18 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a18bc500dca062574ff9117727e1fc68d205dcc832a3b2f83eaf2f09979d94`  
		Last Modified: Fri, 26 Mar 2021 12:22:17 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b484de6008de19b916b6ab647d61ab6244fec6deca555abe66ac20b687b8102c`  
		Last Modified: Fri, 26 Mar 2021 12:22:17 GMT  
		Size: 18.9 KB (18858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e7aa9741d48f2c8dd29d7bb560afc801c3bfc4e698d34ab18d86edb0f30595`  
		Last Modified: Fri, 26 Mar 2021 12:22:15 GMT  
		Size: 5.1 MB (5137391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a556126f0399975b398d3c78e9f3072902ed7ae804e7d536963ab2912e026d15`  
		Last Modified: Fri, 26 Mar 2021 12:22:17 GMT  
		Size: 13.3 KB (13348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761f90ca44a1452aca0727a1c837e71855512b2d81b5db8623c71015bb9258ea`  
		Last Modified: Fri, 26 Mar 2021 12:22:14 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a292ed6a0d56d9db966547179c378ec0f61dab48738f2eb25420f12406687b`  
		Last Modified: Fri, 26 Mar 2021 12:22:15 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712cf0f1c4988d608e22090fcfb16531c1fd25fc63fa0b3e3ddba6aad93d819a`  
		Last Modified: Fri, 26 Mar 2021 12:22:14 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5-php5.6`

```console
$ docker pull php-zendserver@sha256:f2d94b35b1c3ec31852e7af4addaed8e22d696d3c4b116b3f4438980c71cc16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5-php5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:2098726c37868a61a26c88e56a6afc079e228b78ff0c1cfe1cb7b40db7c680a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315053224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfab47bee7a0b78d23540d97b5b7c2ab951c5f96bf9609491df0c212c3be281f`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:14:46 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 26 Mar 2021 12:14:47 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 26 Mar 2021 12:14:47 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Fri, 26 Mar 2021 12:17:12 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 26 Mar 2021 12:17:15 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 26 Mar 2021 12:17:16 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 26 Mar 2021 12:17:17 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 26 Mar 2021 12:17:17 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 26 Mar 2021 12:17:18 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 26 Mar 2021 12:17:19 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 26 Mar 2021 12:17:19 GMT
WORKDIR /usr/local/zs-init
# Fri, 26 Mar 2021 12:17:25 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 26 Mar 2021 12:17:26 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Fri, 26 Mar 2021 12:17:26 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 26 Mar 2021 12:17:27 GMT
RUN rm /var/www/html/index.html
# Fri, 26 Mar 2021 12:17:27 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 26 Mar 2021 12:17:27 GMT
EXPOSE 80
# Fri, 26 Mar 2021 12:17:27 GMT
EXPOSE 443
# Fri, 26 Mar 2021 12:17:27 GMT
EXPOSE 10081
# Fri, 26 Mar 2021 12:17:28 GMT
EXPOSE 10082
# Fri, 26 Mar 2021 12:17:28 GMT
WORKDIR /var/www/html
# Fri, 26 Mar 2021 12:17:28 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ed2a06918c59f99afa96b26b1048e13a36edfd0d339f2219cafc52ed3e35bd`  
		Last Modified: Fri, 26 Mar 2021 12:22:21 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf8cf273b118511038c36413cedc7b8038dca97c11a94a18b5f750492024d26`  
		Last Modified: Fri, 26 Mar 2021 12:22:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e773af4a7db297c6c81102f7a28b05d615cfbda22843b2712859b1a2a4bf754`  
		Last Modified: Fri, 26 Mar 2021 12:22:19 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db2c30b3d8eed72807bc4644eea9b964545dca7c26a236494f0569142f19a29`  
		Last Modified: Fri, 26 Mar 2021 12:22:54 GMT  
		Size: 263.9 MB (263899625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a86f7bd15171ed896e62af2b55a4a2951f830f892b5bb4c4e1f480a54c05beb`  
		Last Modified: Fri, 26 Mar 2021 12:22:19 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219c8d091928daa2f5a00bae617f9001f5a8cc5a98e914a145bc06f1a738b5c`  
		Last Modified: Fri, 26 Mar 2021 12:22:18 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a18bc500dca062574ff9117727e1fc68d205dcc832a3b2f83eaf2f09979d94`  
		Last Modified: Fri, 26 Mar 2021 12:22:17 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b484de6008de19b916b6ab647d61ab6244fec6deca555abe66ac20b687b8102c`  
		Last Modified: Fri, 26 Mar 2021 12:22:17 GMT  
		Size: 18.9 KB (18858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e7aa9741d48f2c8dd29d7bb560afc801c3bfc4e698d34ab18d86edb0f30595`  
		Last Modified: Fri, 26 Mar 2021 12:22:15 GMT  
		Size: 5.1 MB (5137391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a556126f0399975b398d3c78e9f3072902ed7ae804e7d536963ab2912e026d15`  
		Last Modified: Fri, 26 Mar 2021 12:22:17 GMT  
		Size: 13.3 KB (13348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761f90ca44a1452aca0727a1c837e71855512b2d81b5db8623c71015bb9258ea`  
		Last Modified: Fri, 26 Mar 2021 12:22:14 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a292ed6a0d56d9db966547179c378ec0f61dab48738f2eb25420f12406687b`  
		Last Modified: Fri, 26 Mar 2021 12:22:15 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712cf0f1c4988d608e22090fcfb16531c1fd25fc63fa0b3e3ddba6aad93d819a`  
		Last Modified: Fri, 26 Mar 2021 12:22:14 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:dc07b7c48894b5d193a7963a2267de5bfcd56709ee5857ccf263d8ba05c7f16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:2d89ee1518bc6ddf8afec68078fa7868fa996be3ba80150291cbb38f0802c58f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 MB (398693770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027c368ac13cea51d20660feaa913cab747541d9a17750bb105095a8d96917d3`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:14:46 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 26 Mar 2021 12:17:41 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 26 Mar 2021 12:19:05 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.12+b211     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 26 Mar 2021 12:19:09 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 26 Mar 2021 12:19:10 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 26 Mar 2021 12:19:11 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 26 Mar 2021 12:19:11 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 26 Mar 2021 12:19:11 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 26 Mar 2021 12:19:12 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 26 Mar 2021 12:19:12 GMT
WORKDIR /usr/local/zs-init
# Fri, 26 Mar 2021 12:19:18 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 26 Mar 2021 12:19:18 GMT
COPY dir:5966ca4828c37f68d48d11da814350a590451453f42aa83ef2eab6893db3e4cc in /usr/local/bin 
# Fri, 26 Mar 2021 12:19:18 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 26 Mar 2021 12:19:19 GMT
RUN rm /var/www/html/index.html
# Fri, 26 Mar 2021 12:19:19 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 26 Mar 2021 12:19:20 GMT
EXPOSE 80
# Fri, 26 Mar 2021 12:19:20 GMT
EXPOSE 443
# Fri, 26 Mar 2021 12:19:20 GMT
EXPOSE 10081
# Fri, 26 Mar 2021 12:19:20 GMT
EXPOSE 10082
# Fri, 26 Mar 2021 12:19:20 GMT
WORKDIR /var/www/html
# Fri, 26 Mar 2021 12:19:21 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ed2a06918c59f99afa96b26b1048e13a36edfd0d339f2219cafc52ed3e35bd`  
		Last Modified: Fri, 26 Mar 2021 12:22:21 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfb01b32cd06e344e544aa3e8f280d8612b887ae76b37ac7bf2e25143730b00`  
		Last Modified: Fri, 26 Mar 2021 12:23:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088098f50d18efbe5eae439c8e8b6752e211e73740ce655a0ad57735424b5a5e`  
		Last Modified: Fri, 26 Mar 2021 12:24:24 GMT  
		Size: 347.5 MB (347535624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c669a1ed2b168b464a41e75f618574f167d07f07e39737322d1d8612f88bff`  
		Last Modified: Fri, 26 Mar 2021 12:23:21 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17440dc2ba4e05de7a76fb636bf21284d0b523bc733e92f9d69304c9fdf1713f`  
		Last Modified: Fri, 26 Mar 2021 12:23:22 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0ad2751bade6bc189de1e875631559ce86f9990f765ccdc8b2af7d3b946cf4`  
		Last Modified: Fri, 26 Mar 2021 12:23:22 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7113598f1826ca542ea6a3d920b386a28b5abefc16fd88fef14bb645b0ef454c`  
		Last Modified: Fri, 26 Mar 2021 12:23:22 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1ff45c99b43826fd2f588f5075888a0d83e59e666589d954a17e29c94ea982`  
		Last Modified: Fri, 26 Mar 2021 12:23:20 GMT  
		Size: 5.1 MB (5141266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7b5e1394ffbc5109c938a314b6ecd322d02007b62526bfeb5bd089c39f5ae3`  
		Last Modified: Fri, 26 Mar 2021 12:23:19 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b4ddb706c813d47abab24969f065c11d70ac33078cf0c86d6bcad52428cb8`  
		Last Modified: Fri, 26 Mar 2021 12:23:19 GMT  
		Size: 2.6 KB (2557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33c0f72f5b0ff630b6df44ff822c12e2ff8a3c9ea8f29d3ad000fd42812b8ab`  
		Last Modified: Fri, 26 Mar 2021 12:23:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ad80f03f4eb564fec7a725209d95f23ea2074c2094cc8f5e8fb1d77740aebf`  
		Last Modified: Fri, 26 Mar 2021 12:23:19 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:d6d8150ca026599fc9cfcd43bf4a400a69d65d843ae2b2ee8c38fa4655e9b8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:7ae43d5f682b305bd6bf7ecba54e0be70588e9b8e455de81dd23a0117eac27a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.3 MB (482291313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a99bb4946e695c411a209507267e76309635f1884eee72178f185e98ff281a`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:19:48 GMT
RUN apt-get update && apt-get install -y       gnupg
# Fri, 26 Mar 2021 12:19:49 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 26 Mar 2021 12:19:49 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 26 Mar 2021 12:21:43 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.7+b403     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 26 Mar 2021 12:21:46 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 26 Mar 2021 12:21:46 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 26 Mar 2021 12:21:47 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Fri, 26 Mar 2021 12:21:48 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Fri, 26 Mar 2021 12:21:48 GMT
WORKDIR /usr/local/zs-init
# Fri, 26 Mar 2021 12:21:53 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Fri, 26 Mar 2021 12:21:53 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Fri, 26 Mar 2021 12:21:54 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 26 Mar 2021 12:21:54 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Fri, 26 Mar 2021 12:21:55 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 26 Mar 2021 12:21:55 GMT
EXPOSE 80
# Fri, 26 Mar 2021 12:21:55 GMT
EXPOSE 443
# Fri, 26 Mar 2021 12:21:55 GMT
EXPOSE 10081
# Fri, 26 Mar 2021 12:21:55 GMT
EXPOSE 10082
# Fri, 26 Mar 2021 12:21:56 GMT
WORKDIR /var/www/html
# Fri, 26 Mar 2021 12:21:56 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09e9fb21ea14f3d4fd3e0eb488f5fbf7e4b0ab58cdb70cb7caa708fe04c3ed8`  
		Last Modified: Fri, 26 Mar 2021 12:24:49 GMT  
		Size: 32.3 MB (32313870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d842d28e5b2934da62e3393a05d3ca8905f51b2abf4652e0098bd4f8cb5c8570`  
		Last Modified: Fri, 26 Mar 2021 12:24:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1bef7a9258fbbc984d3d84da120330fb50816634221752630f98e20d9de157`  
		Last Modified: Fri, 26 Mar 2021 12:24:43 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2430d61861afed165bec80e5395d05d244229764018cabf8bb8667a41762a3`  
		Last Modified: Fri, 26 Mar 2021 12:26:02 GMT  
		Size: 418.1 MB (418085079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e994fa72fcecb985b9f316c77dfb9ff6803c74cb9fc342f2b61a8b4e51a6e052`  
		Last Modified: Fri, 26 Mar 2021 12:24:42 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6d603ea63961f890aceb5d9626d1d4457ae482f29d27ad7f1ed2ebe398fa99`  
		Last Modified: Fri, 26 Mar 2021 12:24:42 GMT  
		Size: 18.9 KB (18928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6084673048196810d230d49e5f235fa815c086d8468451e5302f7f27492ecf50`  
		Last Modified: Fri, 26 Mar 2021 12:24:40 GMT  
		Size: 5.1 MB (5141254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2951fc02fdf1e381fc6a8ef9e59c421b5bab3e4bcc5c3bb566268c692854bbe`  
		Last Modified: Fri, 26 Mar 2021 12:24:40 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7e9ccf42ae3ade52793d46430d753b09efb4c587f3d0064f3db6de3da3b006`  
		Last Modified: Fri, 26 Mar 2021 12:24:39 GMT  
		Size: 2.6 KB (2556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b953d70d86e29477f45306d26c65f39f1c3bbed4b69c5a38629eacd8d1b2f8`  
		Last Modified: Fri, 26 Mar 2021 12:24:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc2296c2ef763ad8cf55b5d2ff3d435857fa215481f2ea84a6ef49de24f27cf`  
		Last Modified: Fri, 26 Mar 2021 12:24:39 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
