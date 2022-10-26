## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:02c7456a96fde7019b580804d084c3cf1977647934e2d8ba66297c75f3d0208c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:03ace1d5a88c2a9bba9e443ab84a11736473637d83d08ca93414cc9dbc3eab61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.4 MB (308366973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea46bbd64bf10070334d6c9ea7516a45e29aa6a84dc95636d14153d5942777c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 21:54:43 GMT
COPY dir:b50a87fd6710a805ef25d6c1dd2c5f7aa37ef63d04ab1c00c91801848dae94f0 in /opt/java/openjdk 
# Wed, 26 Oct 2022 21:54:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 21:54:45 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Oct 2022 21:54:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Oct 2022 21:54:45 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 21:54:52 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Oct 2022 21:54:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Oct 2022 21:54:52 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Oct 2022 21:55:11 GMT
RUN boot
# Wed, 26 Oct 2022 21:55:11 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 26 Oct 2022 21:55:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Oct 2022 21:55:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c779c71ed965efeafbd0884b3b2abdcb54913a73b69c6be2a18253fd1af00a5`  
		Last Modified: Wed, 26 Oct 2022 22:10:37 GMT  
		Size: 192.1 MB (192137566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ca1632ba6369f3231c962fc59e2f159627c127b7c7b43ef12ceb947a051627`  
		Last Modified: Wed, 26 Oct 2022 22:10:22 GMT  
		Size: 2.4 MB (2362094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa803a111ee1d97da31f6f27ddb214a4fe38117769c6bd044fee4c06ef4f607`  
		Last Modified: Wed, 26 Oct 2022 22:10:25 GMT  
		Size: 58.8 MB (58820582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6448163277c7f67c101c54f3814df767ebdbfbae85862aaa5a6c36f3b510f3e1`  
		Last Modified: Wed, 26 Oct 2022 22:10:21 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9e2b2311f4a735215c383b24a7a0de15f188f33b740a02514864bb169dc7541f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305779099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24a243950ac617fee291ddd3477247974cc78b7dadcb5907092ec96b2cf141b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 15:44:50 GMT
COPY dir:580c509aa131da1d31de9db8eed968c1f0ef93ad270f258b0b43d9d7d72bba84 in /opt/java/openjdk 
# Wed, 26 Oct 2022 15:44:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 15:44:54 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Oct 2022 15:44:54 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Oct 2022 15:44:54 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 15:44:59 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Oct 2022 15:44:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Oct 2022 15:44:59 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Oct 2022 15:45:18 GMT
RUN boot
# Wed, 26 Oct 2022 15:45:18 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 26 Oct 2022 15:45:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Oct 2022 15:45:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dae7f1170ef9a47cb310629f09131dfb5a10ce4efd89d8f7e2a1aad189bb61`  
		Last Modified: Wed, 26 Oct 2022 16:01:02 GMT  
		Size: 190.9 MB (190904077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ae30d2c5c9ba379f554152ba155d14a84c249adcef44ea0954c525e69378db`  
		Last Modified: Wed, 26 Oct 2022 16:00:51 GMT  
		Size: 2.4 MB (2352229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5240b2a070d295da9399ff8cf4d00d7a8bbef12835cc3201ac1f86c85d22a4`  
		Last Modified: Wed, 26 Oct 2022 16:00:54 GMT  
		Size: 58.8 MB (58820425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0757cb5d1ebf6793ac5ec1c98315687b4493933103ceb2a68bebb9ffa0035ef`  
		Last Modified: Wed, 26 Oct 2022 16:00:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
