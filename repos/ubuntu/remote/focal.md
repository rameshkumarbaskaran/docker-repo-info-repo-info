## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:6035d1ac40c04f73752139d5c3db688ea605e6688fc5430390eef3ad0b3062e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

```console
$ docker pull ubuntu@sha256:9c2b5e9c6bc05e63875f68a4295af49399c9ea7bfc6908b2880c1380b44e2fc1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28359601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611c14c8c20797f1e83764024d3378abb9345b0ce6481f456440613168052fd8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:23:16 GMT
ADD file:313024b5cf55edbc2a5804a2000516a581cea278d31b4232050889af00db05e4 in / 
# Thu, 19 Dec 2019 04:23:17 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:23:18 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:23:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:23:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b6ea110572053dea2a331bd22b1a9892370ea765f1a2e53f0f56870daa39e76b`  
		Last Modified: Mon, 02 Dec 2019 15:36:40 GMT  
		Size: 28.3 MB (28327971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70e5e5e771c2cc6911e116937467415641a3b20961af36f37becfacf6f3db4`  
		Last Modified: Thu, 19 Dec 2019 04:25:29 GMT  
		Size: 30.6 KB (30624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87d55335709377cbe36b97025840286bb6ce3db2690126b17a73779948b318a`  
		Last Modified: Thu, 19 Dec 2019 04:25:29 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac97c047f450d89bde54d10c362609ba5f24706397df1fe983895f26c1a759e`  
		Last Modified: Thu, 19 Dec 2019 04:25:30 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f29e5164beb9eece21968b6392c65394e739953bb6f1afe0ab292b6a02bd079f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23836713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3f2a1d3068db1c36dddb2ea7107a2dbf034df6de6259c3f8f1de7aefec6c06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:12:01 GMT
ADD file:a83a5ca41e5d338077de0100edb1eeb1270147fb92480334009a6bf60d77ed55 in / 
# Thu, 19 Dec 2019 06:12:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:12:11 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:12:13 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:12:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7a0f5ae94065e1ed84123f74da1c43b7615043cd0703476aa5d3964646741ed2`  
		Last Modified: Mon, 02 Dec 2019 15:37:27 GMT  
		Size: 23.8 MB (23805081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce60abded96d3844e8100be41eb0efd81e3dc5095465c20c75a5614516d942f7`  
		Last Modified: Thu, 19 Dec 2019 06:15:26 GMT  
		Size: 30.6 KB (30598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf0ece898bded66a70bbfcc9b3a71f72154f8a7313ac8a8da9245c13421bd3a`  
		Last Modified: Thu, 19 Dec 2019 06:15:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e9bc5f1170de67d9befe861b7c1d697e41059b5df99c390bd006d0a02a597e`  
		Last Modified: Thu, 19 Dec 2019 06:15:27 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:64a3d51cb381a58adf45f5037a03deee2e22668d8e2f19a222e78c16969229a6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26978462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb1d69f19cd3f982e87a8dfaf75277516c426a7b0f2b633ffa2607d61cc4346`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:42:08 GMT
ADD file:3f5a5ff4e005ffd96a9a56c4234117276101fd4cd6b87b503fad5d3f02319d92 in / 
# Thu, 16 Jan 2020 00:42:11 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 00:42:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:42:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:42:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d0804342421c30932eee7f90821efd1e7dac9398a9cac78b662e33b2a3faeeb3`  
		Last Modified: Thu, 16 Jan 2020 00:44:12 GMT  
		Size: 26.9 MB (26946995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d926bd5118332af73957eb2925d9433286ec09620aa22ed01eaca19e89d76a`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 30.4 KB (30431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3420a5d9e296a9e1a3d258bef98c8dd8f40f3b0767cdb42b424acdee2b47b2b9`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86fe98d56e47198b1f7b547c1dfac333460f1aa23177768180ca62714aaa1d2`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:bd50192eb59804dbe3c90d2ea88eb96bc4a4613b026f9c43664fdd9411b75a2f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33052181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080259067c173153a361b6f2548a4da09bfb1401f47f5d8aaae949e8a101268e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:19:56 GMT
ADD file:437e0dd068bae1687e4e04e19ec96243aa4afebbab660b1b5bdba8eb5e91f050 in / 
# Thu, 19 Dec 2019 04:20:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:20:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:20:20 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:20:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9af97d6b262669f0a51c75da370ddb33c65b7e7ad545f9a4a28b9c69ae3fcd6b`  
		Last Modified: Mon, 02 Dec 2019 15:38:34 GMT  
		Size: 33.0 MB (33020635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb39a6993f6cc585b3a0610af82965873a030d940f186262498c01f583f18cc`  
		Last Modified: Thu, 19 Dec 2019 04:26:04 GMT  
		Size: 30.5 KB (30510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fe3a933635c2b53543e636825818e38c0637805ed3b268d71de4140148b984`  
		Last Modified: Thu, 19 Dec 2019 04:26:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9229b1ca1966e1e3d889dd099e41076b9832b790da0c37314ab2d3a45a8507c0`  
		Last Modified: Thu, 19 Dec 2019 04:26:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:7345a0001b12b9d537ae2936205827ddd6a9aac6616943e67f9623d2ef338c52
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26957237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9394f7a1e4c93e9b65700e3412aff5cd02302a0d4db349809f9257fdd411c040`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:45:47 GMT
ADD file:5fbe981ed0834a4a7ca86c449eacf27c014fe832bba12eda0aa98718b927fc45 in / 
# Thu, 16 Jan 2020 00:45:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 00:45:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:45:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:45:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9718365a56944fa9db6c418110acfb6a7170f892e2f5d8bb0b66b3dbb538ad2a`  
		Last Modified: Thu, 16 Jan 2020 00:46:51 GMT  
		Size: 26.9 MB (26925143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1be672e2a8be868977dac18b2ad998262f7716cc1bda9f79c380e87d70c8d8`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 31.1 KB (31089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08de0d4260b235271919468fdd3074a90da7692eb0d0575521cb1b18dd36525d`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d5d6c35a086753c3e88803888682d2da2f6cea21681a1d304e5cd8c8f0846`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
