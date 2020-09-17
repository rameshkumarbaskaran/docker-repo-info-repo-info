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
$ docker pull php-zendserver@sha256:b3bf2b349a7756056d2dace69c3e653c2defd729361c95326e1d3a4f07d4cd42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:4d46007342bde3ff0d83b7bb0a50f2646c8e4fe0b381a73a5597dc59ee9f250d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.8 MB (491763735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49c6af601e36f310eda14ee4cfb477b10d6bf4ba5c31895a7567b4f0b4282e`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 01:02:08 GMT
RUN apt-get update && apt-get install -y       gnupg
# Thu, 17 Sep 2020 01:02:09 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Thu, 17 Sep 2020 01:02:09 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Thu, 17 Sep 2020 01:04:01 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.4+b392     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Thu, 17 Sep 2020 01:04:01 GMT
ENV ZS_INIT_VERSION=0.3
# Thu, 17 Sep 2020 01:04:02 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Thu, 17 Sep 2020 01:04:02 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Thu, 17 Sep 2020 01:04:03 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Thu, 17 Sep 2020 01:04:03 GMT
WORKDIR /usr/local/zs-init
# Thu, 17 Sep 2020 01:04:12 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Thu, 17 Sep 2020 01:04:12 GMT
COPY dir:7937a6223a1e7805720eca1fbf8c2ccd37938f8f8aa175ae003d409459d49380 in /usr/local/bin 
# Thu, 17 Sep 2020 01:04:12 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Thu, 17 Sep 2020 01:04:13 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Thu, 17 Sep 2020 01:04:13 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Thu, 17 Sep 2020 01:04:14 GMT
EXPOSE 80
# Thu, 17 Sep 2020 01:04:14 GMT
EXPOSE 443
# Thu, 17 Sep 2020 01:04:14 GMT
EXPOSE 10081
# Thu, 17 Sep 2020 01:04:14 GMT
EXPOSE 10082
# Thu, 17 Sep 2020 01:04:14 GMT
WORKDIR /var/www/html
# Thu, 17 Sep 2020 01:04:15 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690eb663e60d138e6ddb36d11f406741177269cba3b139845dad1a753529cd62`  
		Last Modified: Thu, 17 Sep 2020 01:06:48 GMT  
		Size: 28.4 MB (28429634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9118478cf308d3968e0ae2c73280ea7a3619cdb5d680cb94e8ad831d5d617563`  
		Last Modified: Thu, 17 Sep 2020 01:06:44 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3585a6d92bb3b75ee19e5e747a4e1c1d0393b972f0e41a3d5cf6510950fd0b13`  
		Last Modified: Thu, 17 Sep 2020 01:06:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130b3ef1df2e6d5c8b0814f1f8fc79a8c8019f0625a1fed131f961282c7f3b5b`  
		Last Modified: Thu, 17 Sep 2020 01:07:55 GMT  
		Size: 417.6 MB (417565733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9565536583cf2201abe81f1455d22525ea4d06671d3bb987ed0e7b884ceb07e2`  
		Last Modified: Thu, 17 Sep 2020 01:06:43 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b522a5811c153bffa290168612d5c878eedf25ba63efcc6f907c59e1fad4808`  
		Last Modified: Thu, 17 Sep 2020 01:06:42 GMT  
		Size: 18.9 KB (18899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96621481461da25509e2103346030642cb78c8ea5d97958c2d8317ec7a864ce0`  
		Last Modified: Thu, 17 Sep 2020 01:06:46 GMT  
		Size: 19.0 MB (19028548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d8f3e43703aedd4c23f8d0acb19645c9460213db50f33d32c764d54e9f9906`  
		Last Modified: Thu, 17 Sep 2020 01:06:42 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e92f93825ef14f6abdae58da3a7680a8e67270494857bc1f870bd9b218cb135`  
		Last Modified: Thu, 17 Sep 2020 01:06:42 GMT  
		Size: 2.5 KB (2530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ca689f6058bc7a36baf8356c4aa91b04819f06ece45ee62ba8e1a2487d11e5`  
		Last Modified: Thu, 17 Sep 2020 01:06:41 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6386474079e4b4224fee04a5f4873b11fa12a5d2edd282d94d2c3f38206bbfb4`  
		Last Modified: Thu, 17 Sep 2020 01:06:41 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:5.6`

```console
$ docker pull php-zendserver@sha256:988a8a7218ea37113037291fc1b5d62f1cb39d0bb662898746e3c7fb2479a27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:75e3f674570abc7089564156b62c83edad484cb3f6226922004b0d4e1c09d050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327430427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803e9e6ee3c37bfa93d739e3cc650ee7ead2cab60b66b9588d6922b713f7a352`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 16 Sep 2020 22:22:41 GMT
ADD file:22e6fa4e90b4c26ba962a4fe57e5784d8923885e6eb39435cb121c716c42f7ff in / 
# Wed, 16 Sep 2020 22:22:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:22:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:22:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:22:44 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:57:28 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Thu, 17 Sep 2020 00:57:28 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Thu, 17 Sep 2020 00:57:29 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Thu, 17 Sep 2020 00:59:16 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Thu, 17 Sep 2020 00:59:17 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Thu, 17 Sep 2020 00:59:17 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Thu, 17 Sep 2020 00:59:18 GMT
RUN /usr/sbin/a2enmod headers
# Thu, 17 Sep 2020 00:59:18 GMT
ENV ZS_INIT_VERSION=0.3
# Thu, 17 Sep 2020 00:59:19 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Thu, 17 Sep 2020 00:59:19 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Thu, 17 Sep 2020 00:59:20 GMT
WORKDIR /usr/local/zs-init
# Thu, 17 Sep 2020 00:59:33 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Thu, 17 Sep 2020 00:59:34 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Thu, 17 Sep 2020 00:59:34 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Thu, 17 Sep 2020 00:59:35 GMT
RUN rm /var/www/html/index.html
# Thu, 17 Sep 2020 00:59:35 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Thu, 17 Sep 2020 00:59:35 GMT
EXPOSE 80
# Thu, 17 Sep 2020 00:59:35 GMT
EXPOSE 443
# Thu, 17 Sep 2020 00:59:35 GMT
EXPOSE 10081
# Thu, 17 Sep 2020 00:59:36 GMT
EXPOSE 10082
# Thu, 17 Sep 2020 00:59:36 GMT
WORKDIR /var/www/html
# Thu, 17 Sep 2020 00:59:36 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:001ecc9468da6632359722ccefa732463486659ee07daacd31602ec3bf4d862f`  
		Last Modified: Fri, 04 Sep 2020 13:20:12 GMT  
		Size: 44.5 MB (44490811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9667498691604756cf3601ba44360f2b1f6ba8b5745eee963847d2a4ea736`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe474042557a4bffb655cd6079656d79e2ecfb0d0fad367c610ca1ec65d0e86`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf2fb0fbbc55e614a3391455d772eae373e0136b7cba4d79dd72f28fb347f0`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0509212ca52b402fa07a1ec381caacf37cea92fc1b64a4d113b32760023c`  
		Last Modified: Thu, 17 Sep 2020 01:04:40 GMT  
		Size: 14.7 KB (14705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835a28cbde933709941a55999fe6fe6a386142529e2e6ed10561bd4c071aaf06`  
		Last Modified: Thu, 17 Sep 2020 01:04:40 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6ed2a490fdef0907b14341600eaf2745580f3dc95ce118988a77c67047da97`  
		Last Modified: Thu, 17 Sep 2020 01:04:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18952c356d25fc58ff2b33d1471129df53dd37f6d268d01dc5028e3927eebf17`  
		Last Modified: Thu, 17 Sep 2020 01:05:32 GMT  
		Size: 263.9 MB (263865051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b87bd904b7b8709baa8c244d0f5ebb31b431a5a889c34ce2788cfd239bfb0f8`  
		Last Modified: Thu, 17 Sep 2020 01:04:39 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2921a72766066fe326e0209b1b5904d04742d0ac3cfa2ddda4ba620c662b564`  
		Last Modified: Thu, 17 Sep 2020 01:04:39 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfa1d48eab59c782f5f1e6fa4b636e6592d8a81a87916b361f907cfeb8aac04`  
		Last Modified: Thu, 17 Sep 2020 01:04:39 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42f531fb9b14bfc11b1bbf72eea5e6d84641f4053020865421b279fb98f4a9a`  
		Last Modified: Thu, 17 Sep 2020 01:04:39 GMT  
		Size: 18.8 KB (18834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c08e6ec787e2a4a770e1e903c16d32ec7066c1223086e19129340820b37805`  
		Last Modified: Thu, 17 Sep 2020 01:04:42 GMT  
		Size: 19.0 MB (19020774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba694e093d6760ee318f9e2fbb61db02984b2bcf39775a5efab6f7792033f7a`  
		Last Modified: Thu, 17 Sep 2020 01:04:38 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426cf4b9c7aa3ffc557965ed654f6028f80d45c7b21995ded275f93deeb6b8d1`  
		Last Modified: Thu, 17 Sep 2020 01:04:37 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f5afd9ae99849545a4ce0e6f5eb766e2f5dffc983b6b984121a41446017734`  
		Last Modified: Thu, 17 Sep 2020 01:04:37 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e5a29fa66ec83cb392e1454a98367e2faebb5c50aa137603fd8779d620289e`  
		Last Modified: Thu, 17 Sep 2020 01:04:38 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5`

```console
$ docker pull php-zendserver@sha256:988a8a7218ea37113037291fc1b5d62f1cb39d0bb662898746e3c7fb2479a27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5` - linux; amd64

```console
$ docker pull php-zendserver@sha256:75e3f674570abc7089564156b62c83edad484cb3f6226922004b0d4e1c09d050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327430427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803e9e6ee3c37bfa93d739e3cc650ee7ead2cab60b66b9588d6922b713f7a352`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 16 Sep 2020 22:22:41 GMT
ADD file:22e6fa4e90b4c26ba962a4fe57e5784d8923885e6eb39435cb121c716c42f7ff in / 
# Wed, 16 Sep 2020 22:22:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:22:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:22:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:22:44 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:57:28 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Thu, 17 Sep 2020 00:57:28 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Thu, 17 Sep 2020 00:57:29 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Thu, 17 Sep 2020 00:59:16 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Thu, 17 Sep 2020 00:59:17 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Thu, 17 Sep 2020 00:59:17 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Thu, 17 Sep 2020 00:59:18 GMT
RUN /usr/sbin/a2enmod headers
# Thu, 17 Sep 2020 00:59:18 GMT
ENV ZS_INIT_VERSION=0.3
# Thu, 17 Sep 2020 00:59:19 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Thu, 17 Sep 2020 00:59:19 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Thu, 17 Sep 2020 00:59:20 GMT
WORKDIR /usr/local/zs-init
# Thu, 17 Sep 2020 00:59:33 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Thu, 17 Sep 2020 00:59:34 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Thu, 17 Sep 2020 00:59:34 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Thu, 17 Sep 2020 00:59:35 GMT
RUN rm /var/www/html/index.html
# Thu, 17 Sep 2020 00:59:35 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Thu, 17 Sep 2020 00:59:35 GMT
EXPOSE 80
# Thu, 17 Sep 2020 00:59:35 GMT
EXPOSE 443
# Thu, 17 Sep 2020 00:59:35 GMT
EXPOSE 10081
# Thu, 17 Sep 2020 00:59:36 GMT
EXPOSE 10082
# Thu, 17 Sep 2020 00:59:36 GMT
WORKDIR /var/www/html
# Thu, 17 Sep 2020 00:59:36 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:001ecc9468da6632359722ccefa732463486659ee07daacd31602ec3bf4d862f`  
		Last Modified: Fri, 04 Sep 2020 13:20:12 GMT  
		Size: 44.5 MB (44490811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9667498691604756cf3601ba44360f2b1f6ba8b5745eee963847d2a4ea736`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe474042557a4bffb655cd6079656d79e2ecfb0d0fad367c610ca1ec65d0e86`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf2fb0fbbc55e614a3391455d772eae373e0136b7cba4d79dd72f28fb347f0`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0509212ca52b402fa07a1ec381caacf37cea92fc1b64a4d113b32760023c`  
		Last Modified: Thu, 17 Sep 2020 01:04:40 GMT  
		Size: 14.7 KB (14705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835a28cbde933709941a55999fe6fe6a386142529e2e6ed10561bd4c071aaf06`  
		Last Modified: Thu, 17 Sep 2020 01:04:40 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6ed2a490fdef0907b14341600eaf2745580f3dc95ce118988a77c67047da97`  
		Last Modified: Thu, 17 Sep 2020 01:04:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18952c356d25fc58ff2b33d1471129df53dd37f6d268d01dc5028e3927eebf17`  
		Last Modified: Thu, 17 Sep 2020 01:05:32 GMT  
		Size: 263.9 MB (263865051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b87bd904b7b8709baa8c244d0f5ebb31b431a5a889c34ce2788cfd239bfb0f8`  
		Last Modified: Thu, 17 Sep 2020 01:04:39 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2921a72766066fe326e0209b1b5904d04742d0ac3cfa2ddda4ba620c662b564`  
		Last Modified: Thu, 17 Sep 2020 01:04:39 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfa1d48eab59c782f5f1e6fa4b636e6592d8a81a87916b361f907cfeb8aac04`  
		Last Modified: Thu, 17 Sep 2020 01:04:39 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42f531fb9b14bfc11b1bbf72eea5e6d84641f4053020865421b279fb98f4a9a`  
		Last Modified: Thu, 17 Sep 2020 01:04:39 GMT  
		Size: 18.8 KB (18834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c08e6ec787e2a4a770e1e903c16d32ec7066c1223086e19129340820b37805`  
		Last Modified: Thu, 17 Sep 2020 01:04:42 GMT  
		Size: 19.0 MB (19020774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba694e093d6760ee318f9e2fbb61db02984b2bcf39775a5efab6f7792033f7a`  
		Last Modified: Thu, 17 Sep 2020 01:04:38 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426cf4b9c7aa3ffc557965ed654f6028f80d45c7b21995ded275f93deeb6b8d1`  
		Last Modified: Thu, 17 Sep 2020 01:04:37 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f5afd9ae99849545a4ce0e6f5eb766e2f5dffc983b6b984121a41446017734`  
		Last Modified: Thu, 17 Sep 2020 01:04:37 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e5a29fa66ec83cb392e1454a98367e2faebb5c50aa137603fd8779d620289e`  
		Last Modified: Thu, 17 Sep 2020 01:04:38 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5-php5.6`

```console
$ docker pull php-zendserver@sha256:988a8a7218ea37113037291fc1b5d62f1cb39d0bb662898746e3c7fb2479a27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5-php5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:75e3f674570abc7089564156b62c83edad484cb3f6226922004b0d4e1c09d050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327430427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803e9e6ee3c37bfa93d739e3cc650ee7ead2cab60b66b9588d6922b713f7a352`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 16 Sep 2020 22:22:41 GMT
ADD file:22e6fa4e90b4c26ba962a4fe57e5784d8923885e6eb39435cb121c716c42f7ff in / 
# Wed, 16 Sep 2020 22:22:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:22:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:22:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:22:44 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:57:28 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Thu, 17 Sep 2020 00:57:28 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Thu, 17 Sep 2020 00:57:29 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Thu, 17 Sep 2020 00:59:16 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Thu, 17 Sep 2020 00:59:17 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Thu, 17 Sep 2020 00:59:17 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Thu, 17 Sep 2020 00:59:18 GMT
RUN /usr/sbin/a2enmod headers
# Thu, 17 Sep 2020 00:59:18 GMT
ENV ZS_INIT_VERSION=0.3
# Thu, 17 Sep 2020 00:59:19 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Thu, 17 Sep 2020 00:59:19 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Thu, 17 Sep 2020 00:59:20 GMT
WORKDIR /usr/local/zs-init
# Thu, 17 Sep 2020 00:59:33 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Thu, 17 Sep 2020 00:59:34 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Thu, 17 Sep 2020 00:59:34 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Thu, 17 Sep 2020 00:59:35 GMT
RUN rm /var/www/html/index.html
# Thu, 17 Sep 2020 00:59:35 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Thu, 17 Sep 2020 00:59:35 GMT
EXPOSE 80
# Thu, 17 Sep 2020 00:59:35 GMT
EXPOSE 443
# Thu, 17 Sep 2020 00:59:35 GMT
EXPOSE 10081
# Thu, 17 Sep 2020 00:59:36 GMT
EXPOSE 10082
# Thu, 17 Sep 2020 00:59:36 GMT
WORKDIR /var/www/html
# Thu, 17 Sep 2020 00:59:36 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:001ecc9468da6632359722ccefa732463486659ee07daacd31602ec3bf4d862f`  
		Last Modified: Fri, 04 Sep 2020 13:20:12 GMT  
		Size: 44.5 MB (44490811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9667498691604756cf3601ba44360f2b1f6ba8b5745eee963847d2a4ea736`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe474042557a4bffb655cd6079656d79e2ecfb0d0fad367c610ca1ec65d0e86`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf2fb0fbbc55e614a3391455d772eae373e0136b7cba4d79dd72f28fb347f0`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0509212ca52b402fa07a1ec381caacf37cea92fc1b64a4d113b32760023c`  
		Last Modified: Thu, 17 Sep 2020 01:04:40 GMT  
		Size: 14.7 KB (14705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835a28cbde933709941a55999fe6fe6a386142529e2e6ed10561bd4c071aaf06`  
		Last Modified: Thu, 17 Sep 2020 01:04:40 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6ed2a490fdef0907b14341600eaf2745580f3dc95ce118988a77c67047da97`  
		Last Modified: Thu, 17 Sep 2020 01:04:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18952c356d25fc58ff2b33d1471129df53dd37f6d268d01dc5028e3927eebf17`  
		Last Modified: Thu, 17 Sep 2020 01:05:32 GMT  
		Size: 263.9 MB (263865051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b87bd904b7b8709baa8c244d0f5ebb31b431a5a889c34ce2788cfd239bfb0f8`  
		Last Modified: Thu, 17 Sep 2020 01:04:39 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2921a72766066fe326e0209b1b5904d04742d0ac3cfa2ddda4ba620c662b564`  
		Last Modified: Thu, 17 Sep 2020 01:04:39 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfa1d48eab59c782f5f1e6fa4b636e6592d8a81a87916b361f907cfeb8aac04`  
		Last Modified: Thu, 17 Sep 2020 01:04:39 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42f531fb9b14bfc11b1bbf72eea5e6d84641f4053020865421b279fb98f4a9a`  
		Last Modified: Thu, 17 Sep 2020 01:04:39 GMT  
		Size: 18.8 KB (18834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c08e6ec787e2a4a770e1e903c16d32ec7066c1223086e19129340820b37805`  
		Last Modified: Thu, 17 Sep 2020 01:04:42 GMT  
		Size: 19.0 MB (19020774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba694e093d6760ee318f9e2fbb61db02984b2bcf39775a5efab6f7792033f7a`  
		Last Modified: Thu, 17 Sep 2020 01:04:38 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426cf4b9c7aa3ffc557965ed654f6028f80d45c7b21995ded275f93deeb6b8d1`  
		Last Modified: Thu, 17 Sep 2020 01:04:37 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f5afd9ae99849545a4ce0e6f5eb766e2f5dffc983b6b984121a41446017734`  
		Last Modified: Thu, 17 Sep 2020 01:04:37 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e5a29fa66ec83cb392e1454a98367e2faebb5c50aa137603fd8779d620289e`  
		Last Modified: Thu, 17 Sep 2020 01:04:38 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:06fd4daf629469c90d09ea4ba9099f1e0aaf3b2c21f70f3d7a87c459645a0609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:e27255ddb5993b6267367dc9259c141b6778ea51d25e4eb8ad074357be8772a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407658371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7316259f6dc85e534d679cfb39b544474a2288bef3b87f19861518169168b37c`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 16 Sep 2020 22:22:41 GMT
ADD file:22e6fa4e90b4c26ba962a4fe57e5784d8923885e6eb39435cb121c716c42f7ff in / 
# Wed, 16 Sep 2020 22:22:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:22:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:22:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:22:44 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:57:28 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Thu, 17 Sep 2020 00:59:45 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Thu, 17 Sep 2020 01:01:07 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.10+b202     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Thu, 17 Sep 2020 01:01:08 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Thu, 17 Sep 2020 01:01:09 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Thu, 17 Sep 2020 01:01:09 GMT
RUN /usr/sbin/a2enmod headers
# Thu, 17 Sep 2020 01:01:10 GMT
ENV ZS_INIT_VERSION=0.3
# Thu, 17 Sep 2020 01:01:10 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Thu, 17 Sep 2020 01:01:10 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Thu, 17 Sep 2020 01:01:11 GMT
WORKDIR /usr/local/zs-init
# Thu, 17 Sep 2020 01:01:27 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Thu, 17 Sep 2020 01:01:27 GMT
COPY dir:864637d3fa0817ce3be0c7e34e1298851fa2ea4cfb86583e2ec811f00c6a95fd in /usr/local/bin 
# Thu, 17 Sep 2020 01:01:27 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Thu, 17 Sep 2020 01:01:28 GMT
RUN rm /var/www/html/index.html
# Thu, 17 Sep 2020 01:01:28 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Thu, 17 Sep 2020 01:01:29 GMT
EXPOSE 80
# Thu, 17 Sep 2020 01:01:30 GMT
EXPOSE 443
# Thu, 17 Sep 2020 01:01:33 GMT
EXPOSE 10081
# Thu, 17 Sep 2020 01:01:35 GMT
EXPOSE 10082
# Thu, 17 Sep 2020 01:01:36 GMT
WORKDIR /var/www/html
# Thu, 17 Sep 2020 01:01:37 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:001ecc9468da6632359722ccefa732463486659ee07daacd31602ec3bf4d862f`  
		Last Modified: Fri, 04 Sep 2020 13:20:12 GMT  
		Size: 44.5 MB (44490811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9667498691604756cf3601ba44360f2b1f6ba8b5745eee963847d2a4ea736`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe474042557a4bffb655cd6079656d79e2ecfb0d0fad367c610ca1ec65d0e86`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf2fb0fbbc55e614a3391455d772eae373e0136b7cba4d79dd72f28fb347f0`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0509212ca52b402fa07a1ec381caacf37cea92fc1b64a4d113b32760023c`  
		Last Modified: Thu, 17 Sep 2020 01:04:40 GMT  
		Size: 14.7 KB (14705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e377aecabf3f6bef7127b388a2fbc59effe8493d3a5f08e9e0af30df411dcdb4`  
		Last Modified: Thu, 17 Sep 2020 01:05:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d6cca27e2378c6065f1b575f719b1639cc3f0e35b33fdebaff8d37454fa031`  
		Last Modified: Thu, 17 Sep 2020 01:06:38 GMT  
		Size: 344.1 MB (344084755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff94ca36344dfa12f2a6de27a47aa03b2844bc7fd454194a3e2f272a3967ff41`  
		Last Modified: Thu, 17 Sep 2020 01:05:39 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061333c9f5e08e15ed44c06727e8605ad25ccb594b373463085a3c5fa4ab9326`  
		Last Modified: Thu, 17 Sep 2020 01:05:39 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0853902c3365ecc045741007d7a3a8f8d356b886491a22d50de54d5768d5d6f`  
		Last Modified: Thu, 17 Sep 2020 01:05:39 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33dcede6aecf6a524b2439cde82e93cc53e07dd32972353feaeddb41a6e2f60d`  
		Last Modified: Thu, 17 Sep 2020 01:05:39 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a23d2752e87b65e2bf5b47f71f5c93c76a4d1a37bb3edf78ad1c85eaff7edc3`  
		Last Modified: Thu, 17 Sep 2020 01:05:41 GMT  
		Size: 19.0 MB (19028345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb928aa11b11bcf8535f76d258148c100df77ebf37230c25f3ce4941f10dd5c5`  
		Last Modified: Thu, 17 Sep 2020 01:05:38 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce0123cb95fbfa4d74693d00dd1f1ccba15eec0821ebff1f0ef8060ed5a3100`  
		Last Modified: Thu, 17 Sep 2020 01:05:38 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf2de2ba549a39d462b9d719cebcea26f0e2fefe7cba77fc624b48ca44be5a4`  
		Last Modified: Thu, 17 Sep 2020 01:05:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcd98acd04d32fe3292ca2f416aea3cead069a8aafd63ead7b08e79368b6edd`  
		Last Modified: Thu, 17 Sep 2020 01:05:38 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:b3bf2b349a7756056d2dace69c3e653c2defd729361c95326e1d3a4f07d4cd42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:4d46007342bde3ff0d83b7bb0a50f2646c8e4fe0b381a73a5597dc59ee9f250d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.8 MB (491763735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49c6af601e36f310eda14ee4cfb477b10d6bf4ba5c31895a7567b4f0b4282e`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 01:02:08 GMT
RUN apt-get update && apt-get install -y       gnupg
# Thu, 17 Sep 2020 01:02:09 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Thu, 17 Sep 2020 01:02:09 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Thu, 17 Sep 2020 01:04:01 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.4+b392     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Thu, 17 Sep 2020 01:04:01 GMT
ENV ZS_INIT_VERSION=0.3
# Thu, 17 Sep 2020 01:04:02 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Thu, 17 Sep 2020 01:04:02 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Thu, 17 Sep 2020 01:04:03 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Thu, 17 Sep 2020 01:04:03 GMT
WORKDIR /usr/local/zs-init
# Thu, 17 Sep 2020 01:04:12 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Thu, 17 Sep 2020 01:04:12 GMT
COPY dir:7937a6223a1e7805720eca1fbf8c2ccd37938f8f8aa175ae003d409459d49380 in /usr/local/bin 
# Thu, 17 Sep 2020 01:04:12 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Thu, 17 Sep 2020 01:04:13 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Thu, 17 Sep 2020 01:04:13 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Thu, 17 Sep 2020 01:04:14 GMT
EXPOSE 80
# Thu, 17 Sep 2020 01:04:14 GMT
EXPOSE 443
# Thu, 17 Sep 2020 01:04:14 GMT
EXPOSE 10081
# Thu, 17 Sep 2020 01:04:14 GMT
EXPOSE 10082
# Thu, 17 Sep 2020 01:04:14 GMT
WORKDIR /var/www/html
# Thu, 17 Sep 2020 01:04:15 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690eb663e60d138e6ddb36d11f406741177269cba3b139845dad1a753529cd62`  
		Last Modified: Thu, 17 Sep 2020 01:06:48 GMT  
		Size: 28.4 MB (28429634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9118478cf308d3968e0ae2c73280ea7a3619cdb5d680cb94e8ad831d5d617563`  
		Last Modified: Thu, 17 Sep 2020 01:06:44 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3585a6d92bb3b75ee19e5e747a4e1c1d0393b972f0e41a3d5cf6510950fd0b13`  
		Last Modified: Thu, 17 Sep 2020 01:06:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130b3ef1df2e6d5c8b0814f1f8fc79a8c8019f0625a1fed131f961282c7f3b5b`  
		Last Modified: Thu, 17 Sep 2020 01:07:55 GMT  
		Size: 417.6 MB (417565733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9565536583cf2201abe81f1455d22525ea4d06671d3bb987ed0e7b884ceb07e2`  
		Last Modified: Thu, 17 Sep 2020 01:06:43 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b522a5811c153bffa290168612d5c878eedf25ba63efcc6f907c59e1fad4808`  
		Last Modified: Thu, 17 Sep 2020 01:06:42 GMT  
		Size: 18.9 KB (18899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96621481461da25509e2103346030642cb78c8ea5d97958c2d8317ec7a864ce0`  
		Last Modified: Thu, 17 Sep 2020 01:06:46 GMT  
		Size: 19.0 MB (19028548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d8f3e43703aedd4c23f8d0acb19645c9460213db50f33d32c764d54e9f9906`  
		Last Modified: Thu, 17 Sep 2020 01:06:42 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e92f93825ef14f6abdae58da3a7680a8e67270494857bc1f870bd9b218cb135`  
		Last Modified: Thu, 17 Sep 2020 01:06:42 GMT  
		Size: 2.5 KB (2530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ca689f6058bc7a36baf8356c4aa91b04819f06ece45ee62ba8e1a2487d11e5`  
		Last Modified: Thu, 17 Sep 2020 01:06:41 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6386474079e4b4224fee04a5f4873b11fa12a5d2edd282d94d2c3f38206bbfb4`  
		Last Modified: Thu, 17 Sep 2020 01:06:41 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
