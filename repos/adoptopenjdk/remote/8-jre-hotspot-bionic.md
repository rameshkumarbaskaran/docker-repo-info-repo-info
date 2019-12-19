## `adoptopenjdk:8-jre-hotspot-bionic`

```console
$ docker pull adoptopenjdk@sha256:3eb5ade3f78a79d92dd783400c496983e68d92af2d7b7f2e4ca000d4312c0e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `adoptopenjdk:8-jre-hotspot-bionic` - linux; amd64

```console
$ docker pull adoptopenjdk@sha256:9d5f3c6a954a3c3c9b71fafc524a0cc16ba774427e1fb3b23db91346df8024c3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81364928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0cbaf52a8461d92366c79de331aeb0ff66dd13de3a53509e3107c00303165`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90bb5798781d7d972ceffbb8a018b8d4a6209e6ebffef84b49ae3eb603b83b3`  
		Last Modified: Thu, 19 Dec 2019 06:47:39 GMT  
		Size: 41.3 MB (41315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8-jre-hotspot-bionic` - linux; ppc64le

```console
$ docker pull adoptopenjdk@sha256:096c59c952ef3271d7cf0e547e4e4905fa2d704498bbcf93c8b55a186da4c967
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84801636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4816efee1fc0ff3083069dd9e28028ede6f4d6acb25d2b85d9176f35f089bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:17:50 GMT
ADD file:04095d1b229274e65c9beb48f6cf33050e58d8ee2cd59c0063d23301a1b68f40 in / 
# Thu, 19 Dec 2019 04:17:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:18:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:18:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:18:08 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:46:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 08:47:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:47:21 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 08:48:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 08:48:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:fc185e8867852536dd99638d9087ed0059bd4d581436d4c2aac0d0e17666457a`  
		Last Modified: Mon, 02 Dec 2019 15:30:19 GMT  
		Size: 30.4 MB (30400283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e561dfe3fdb898460f7652cbe0a7bb83e64b240d2504cec93d1b4a1cff37951`  
		Last Modified: Thu, 19 Dec 2019 04:24:04 GMT  
		Size: 35.2 KB (35212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5731b4e21c4ef8f9ab7c0d9535bc069ed88e51e1701f2c89b9260bbabc3ab4`  
		Last Modified: Thu, 19 Dec 2019 04:24:04 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66c7d0deb99d27ed750b5a40c0b038d79913a8644af69d2954631935aab9d88`  
		Last Modified: Thu, 19 Dec 2019 04:24:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddd4570d010c9a2d4fd57c621236bfbbae04b13d8823f25bed3bdc65606e5a7`  
		Last Modified: Thu, 19 Dec 2019 08:53:54 GMT  
		Size: 14.0 MB (13969113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bcfb4d7fffff8f3df129e7283ec723e8e62f576a0eda57bc498f39705b28366`  
		Last Modified: Thu, 19 Dec 2019 08:54:31 GMT  
		Size: 40.4 MB (40395988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8-jre-hotspot-bionic` - linux; s390x

```console
$ docker pull adoptopenjdk@sha256:b2d4f821a961d7c77c477b8c652f496cdf48a587cc5f92a85e2bc9101c14aa20
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77448080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702e9ae12f6f750fe5a4f5c871eaecc34159ac18b9ca2095afdccfdc9145d84d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 01:18:53 GMT
ADD file:71a0e537d0c67d313ccdb48e99409227ca2b68d50d7b1c82b2d069057dd72491 in / 
# Thu, 19 Dec 2019 01:18:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 01:18:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 01:18:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 01:18:55 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 01:36:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 01:36:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 01:36:17 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 01:36:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 01:36:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:9015d1e9fd5bbafd5a9ab0a774dfb9d9cc36c1bd9cb89822c3416ab04878e685`  
		Last Modified: Mon, 02 Dec 2019 15:31:08 GMT  
		Size: 25.4 MB (25365188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e1186eb2726687c98475f19f4d0ed50e2da9a171069c5fcfd2f5e04fc656c2`  
		Last Modified: Thu, 19 Dec 2019 01:19:51 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86643ed2fb70b22576aa6d06dc041dbc603accc3240237d6790312c954a872c`  
		Last Modified: Thu, 19 Dec 2019 01:19:51 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2e9f669fe720fe3dae748411a09729a654978872e3f094ab10eff5c5d2d0cb`  
		Last Modified: Thu, 19 Dec 2019 01:19:51 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f3b2baa7c16965ffb114cee9776e89ca1140b0c5ffcef48ee918246fcf0a60`  
		Last Modified: Thu, 19 Dec 2019 01:38:30 GMT  
		Size: 13.0 MB (13040882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a412719eb4bf82d045a6eccfa78819fa7450913ecdb8bf8ad4666cc36f4c7399`  
		Last Modified: Thu, 19 Dec 2019 01:38:51 GMT  
		Size: 39.0 MB (39004828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
