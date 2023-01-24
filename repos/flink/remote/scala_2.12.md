## `flink:scala_2.12`

```console
$ docker pull flink@sha256:214bd2f2f9ec81b82f4b8936cbcbaec8d2d48ef726e3253dc12d50b250df29a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:cf8e5e7f71fb05c881b5ac235f4719ff167fe7139b057766a942e0b357ad51c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.3 MB (571250287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5351b206e2189e2565e42b5f8556a8b670dbc921321040102797868495ec3c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:30 GMT
ADD file:481dd2da6de71525248eba186feeeafcc73cc956ade0a196a4e8b0c2424e74b9 in / 
# Fri, 09 Dec 2022 01:20:31 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:43:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:44:23 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 09 Dec 2022 01:44:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Dec 2022 01:44:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 09 Dec 2022 07:03:07 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 07:03:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 09 Dec 2022 07:03:13 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 09 Dec 2022 07:03:14 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Fri, 09 Dec 2022 07:03:14 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 09 Dec 2022 07:03:14 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 07:03:14 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 09 Dec 2022 07:03:14 GMT
WORKDIR /opt/flink
# Fri, 09 Dec 2022 07:03:33 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 09 Dec 2022 07:03:34 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 09 Dec 2022 07:03:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 07:03:35 GMT
EXPOSE 6123 8081
# Fri, 09 Dec 2022 07:03:35 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:6e3729cf69e0ce2de9e779575a1fec8b7fb5efdfa822829290ab6d5d1bc3e797`  
		Last Modified: Thu, 08 Dec 2022 14:10:00 GMT  
		Size: 30.4 MB (30428708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96aa423488f0ed1e9bf6c6da11fa7fb53568d1ea4003892416b3adeccb47e3bf`  
		Last Modified: Fri, 09 Dec 2022 01:50:02 GMT  
		Size: 12.4 MB (12432218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a149af9550da920d6e3c2939b43e257b858d65f5733af488a97f721d34f907ef`  
		Last Modified: Fri, 09 Dec 2022 01:52:09 GMT  
		Size: 46.6 MB (46632223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a0fd4e771cad4fe553a76281b2095d46b07749710d4dbbaf1b1d07c764c43d`  
		Last Modified: Fri, 09 Dec 2022 01:52:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2a04bb105e044a3466218e231d1c0f86c7d57f65116b78cc15f8b056d90fb0`  
		Last Modified: Fri, 09 Dec 2022 07:05:56 GMT  
		Size: 4.7 MB (4652792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a20da3c2b34ebf4442b29085f25abb00f35754996df2a23bdf63357f4520a2`  
		Last Modified: Fri, 09 Dec 2022 07:05:53 GMT  
		Size: 900.5 KB (900507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ec3d89729acc66e5fc1510d0ddcd3f74aa0a3128200b4972b0276a5a1aac57`  
		Last Modified: Fri, 09 Dec 2022 07:05:53 GMT  
		Size: 4.6 KB (4609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3d067f7b910ba185d38f45885f7d37af5ec90e741d177ea923c5bdcc01c5bb`  
		Last Modified: Fri, 09 Dec 2022 07:05:53 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a93e3fb317ab4c029514da74cab03022b85e269cd9af61089d08af658f07e14`  
		Last Modified: Fri, 09 Dec 2022 07:06:13 GMT  
		Size: 476.2 MB (476196815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b4e92134ab387992e2f4df84733d346dc7a0cb0ef8b7ee599210a378be7b43`  
		Last Modified: Fri, 09 Dec 2022 07:05:53 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:scala_2.12` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:62170d6c839918943265b3bc6b72acba8158dc4a092882382560beeecc2523e0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567297978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1022bd0ee42a1fa8f5baa46fc3b47a46557bdc732664271910250dd18992f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:57 GMT
ADD file:429a55a11d4bcd15647d1316d9debd9ead4b4ab5c0b9146894d07c39aa814290 in / 
# Fri, 09 Dec 2022 01:46:57 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:39:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:39:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:39:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:39:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 17:41:30 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 24 Jan 2023 17:42:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 24 Jan 2023 17:42:30 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 24 Jan 2023 21:17:33 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:17:33 GMT
ENV GOSU_VERSION=1.11
# Tue, 24 Jan 2023 21:17:55 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Tue, 24 Jan 2023 21:17:56 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Tue, 24 Jan 2023 21:17:56 GMT
ENV FLINK_HOME=/opt/flink
# Tue, 24 Jan 2023 21:17:56 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:17:56 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Tue, 24 Jan 2023 21:17:56 GMT
WORKDIR /opt/flink
# Tue, 24 Jan 2023 21:19:58 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Tue, 24 Jan 2023 21:20:01 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Tue, 24 Jan 2023 21:20:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:20:01 GMT
EXPOSE 6123 8081
# Tue, 24 Jan 2023 21:20:01 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:10175de2f0c4f7d306f660ee073bce12b824c8012dd19b3c140aae053fabd1cc`  
		Last Modified: Thu, 08 Dec 2022 18:50:01 GMT  
		Size: 28.4 MB (28384475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6940ebf96dce07e0f2d684dad9d95a74c7620e493977fa2d52970797dafd6002`  
		Last Modified: Fri, 09 Dec 2022 03:45:30 GMT  
		Size: 12.4 MB (12391491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69220f5afb64fabad669c939ae755d997370436819e4d9bee92f3b7c1e2c027`  
		Last Modified: Tue, 24 Jan 2023 17:48:09 GMT  
		Size: 45.0 MB (44979499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad77dbf6975f7cfbe63eae8465add6a49a98dd3ae3ed046dba91a957ff49ee8f`  
		Last Modified: Tue, 24 Jan 2023 17:48:04 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3870c1cd15442fb5cadfb855191da86aea0b3785c7bd672c1efcc17dd79644d6`  
		Last Modified: Tue, 24 Jan 2023 21:21:18 GMT  
		Size: 4.5 MB (4503331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c19fe97c9751dddc2bca5406183a59263b3e197f2af7a2ff71512fe5da88e`  
		Last Modified: Tue, 24 Jan 2023 21:21:15 GMT  
		Size: 835.4 KB (835388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63318f217246fe56fbbd26ea23d8444fbf23f1ed3df629912249ff6f22d3fc17`  
		Last Modified: Tue, 24 Jan 2023 21:21:15 GMT  
		Size: 4.7 KB (4653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7da224a1c42cd78dd2622705f31feba87291b5cc641dd24302b0e1c038fe9a6`  
		Last Modified: Tue, 24 Jan 2023 21:21:15 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36b4a7aa5b535890b6a860c44c7a14dbb2d558afd12128e8c8ca9b096246606`  
		Last Modified: Tue, 24 Jan 2023 21:21:32 GMT  
		Size: 476.2 MB (476196723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472426c6ea6e0d0ae9538698bb5520a2c12e425311c78eb62906419d461d858a`  
		Last Modified: Tue, 24 Jan 2023 21:21:15 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
