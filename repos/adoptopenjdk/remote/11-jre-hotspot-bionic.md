## `adoptopenjdk:11-jre-hotspot-bionic`

```console
$ docker pull adoptopenjdk@sha256:4c979a138f6e28705ed6d55f2e8218fe70737710f92f89af3e6c8123ccc7487e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `adoptopenjdk:11-jre-hotspot-bionic` - linux; amd64

```console
$ docker pull adoptopenjdk@sha256:379a91443597c1c775f61608e1f51c555136ce6eede51144a81bd53e40c59c1e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82902619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd72040fd3384ade9c04077433bbb26aeac7bf774bb9e38cb992fc114c140bb5`
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
# Thu, 19 Dec 2019 06:44:33 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Thu, 19 Dec 2019 06:44:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='2e5343f2046844673f88a4297f5e5796979acb9880b291f965b4c9fa33201d78';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='2f08c469c9a8adea1b6ee3444ba2a8242a7e99d87976a077faf037a9eb7f884b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:58 GMT
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
	-	`sha256:8bb8c6504c719a3a083869f0711720d4ad964c9dd22968979cbd6e6155b355c3`  
		Last Modified: Thu, 19 Dec 2019 06:48:16 GMT  
		Size: 42.9 MB (42853646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-jre-hotspot-bionic` - linux; arm64 variant v8

```console
$ docker pull adoptopenjdk@sha256:4205fec9420b6722426afb95bbd1435a1cb4c7a0d75f5f4faac31d6d8cf18d9e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75862598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40e78e3a1f560ac42a427151fac9e6ebfba92c2512c50c3bf5947789998b947`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2019 22:40:37 GMT
ADD file:4c6cab77271e86386e8f3d4ecf06c17a3e9339481bea878a706d2c5dc4a0addd in / 
# Thu, 31 Oct 2019 22:40:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:40:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:40:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:40:44 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:58:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Oct 2019 22:59:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 22:59:31 GMT
ENV JAVA_VERSION=jdk-11.0.4+11
# Thu, 31 Oct 2019 22:59:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5f7b5c110fc0f344a549cb11784a6d76838061a2b6f654f7841f60e0cd286c6a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.4_11.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5da5f86f250eeb26719ba06ae1a1133eb75933fad7b9cf1624d743fafd7a7e2b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.4_11.tar.gz';          ;;        s390x)          ESUM='274036da66b150050e23dfc87a4c0ab5331fa6f0d0804b8016621aedf8d1a1e1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.4_11.tar.gz';          ;;        amd64|x86_64)          ESUM='70d2cc675155476f1d8516a7ae6729d44681e4fad5a6fc8dfa65cab36a67b7e0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.4_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 31 Oct 2019 22:59:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:6531af3558948c8839fd7cc7eb7062aa86bfae891870ccaafd554ac65c97971b`  
		Last Modified: Thu, 31 Oct 2019 22:42:23 GMT  
		Size: 23.7 MB (23718403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f7942d2fb7381ee1735a4c972ef45c89b6521902e6eba024d4791dfd069def`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce94e690d563311eb8b102b49e94a01b2a4c965daa9e33d5e59168dc4327e0`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a89ada1c32e30a1998945a8785c18bcdce55dcfe2b666bb587d432255cb11`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb929685f4a20d12d37720cde265d3c645d4ec19fbad4db50c81055be5dc25`  
		Last Modified: Thu, 31 Oct 2019 23:01:25 GMT  
		Size: 10.3 MB (10302431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403ce56eaf5b3e8f6d958819de2613191ecb8d22c81a84c9a17ec1c423b7d4c`  
		Last Modified: Thu, 31 Oct 2019 23:02:56 GMT  
		Size: 41.8 MB (41805533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-jre-hotspot-bionic` - linux; ppc64le

```console
$ docker pull adoptopenjdk@sha256:32393679139066ad908da56fdeb73a72087cdb03ad16bd4adb905d6cdde4ef84
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83907806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454fc646ba3e3e30edaa01e69caf3b293059d6407a24c8fe2f9fc567f0370e72`
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
# Thu, 19 Dec 2019 08:48:13 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Thu, 19 Dec 2019 08:48:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='2e5343f2046844673f88a4297f5e5796979acb9880b291f965b4c9fa33201d78';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='2f08c469c9a8adea1b6ee3444ba2a8242a7e99d87976a077faf037a9eb7f884b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 08:48:55 GMT
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
	-	`sha256:b3fa83385b9dbc0f6fbb4b41e55e3e70752a8a614e2e66893c7cd4c21d2c47cb`  
		Last Modified: Thu, 19 Dec 2019 08:55:34 GMT  
		Size: 39.5 MB (39502158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-jre-hotspot-bionic` - linux; s390x

```console
$ docker pull adoptopenjdk@sha256:922bc0204ee516e546b93143c697d367e932166c8788f11fd24d2687a5a9f8d2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75094799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3579f061c16a584e4aafbe34dbfb41f8ab84e099ca29c9676bd7855129b31a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Oct 2019 23:00:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:01:04 GMT
ENV JAVA_VERSION=jdk-11.0.4+11
# Thu, 31 Oct 2019 23:01:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5f7b5c110fc0f344a549cb11784a6d76838061a2b6f654f7841f60e0cd286c6a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.4_11.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5da5f86f250eeb26719ba06ae1a1133eb75933fad7b9cf1624d743fafd7a7e2b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.4_11.tar.gz';          ;;        s390x)          ESUM='274036da66b150050e23dfc87a4c0ab5331fa6f0d0804b8016621aedf8d1a1e1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.4_11.tar.gz';          ;;        amd64|x86_64)          ESUM='70d2cc675155476f1d8516a7ae6729d44681e4fad5a6fc8dfa65cab36a67b7e0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.4_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 31 Oct 2019 23:01:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d6516ebe93aefa5d84bd151472231fda34a88c02a0c5b2ebdfa62a362ffdb3`  
		Last Modified: Thu, 31 Oct 2019 23:05:58 GMT  
		Size: 10.6 MB (10552908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b8346f33b7a78720e7cd5172e7b4f38a024424cb9dc5daba2b93de5544ff30`  
		Last Modified: Thu, 31 Oct 2019 23:07:19 GMT  
		Size: 39.1 MB (39140065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
