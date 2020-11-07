## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:e8eb0923cedcac7d02a0ab6632f92092e3e8577f286730fe00f3c60151b14e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9e612069601762761f296c13ecb8bca198f1821ab931fa6ca7e7db6fc644ef30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208153381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29632c9add27a9957d8d19b1a32c7f6c348642106a82d8712eb3d1432a5790c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Sat, 07 Nov 2020 00:19:55 GMT
ARG version=11.0.9.12-1
# Sat, 07 Nov 2020 00:20:21 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 07 Nov 2020 00:20:22 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:20:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82215f6c82ad0f433d877cc8341441ce73e67f294b86c2998e24e34e60d272c9`  
		Last Modified: Sat, 07 Nov 2020 00:21:56 GMT  
		Size: 146.4 MB (146436841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e71b5f2be284dfaa3a19cad2370600d1205fb0a41bbbe53dc530505c3ffcb1cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207838791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8a1c8f6b10ff712d2b1142a3644948b42a91929644ff129a81ce138bda90f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 23:40:15 GMT
ARG version=11.0.9.12-1
# Fri, 06 Nov 2020 23:40:46 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 06 Nov 2020 23:40:47 GMT
ENV LANG=C.UTF-8
# Fri, 06 Nov 2020 23:40:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbd29edd12813ebfd63352f3807f9ffea1fea3148691fd8206f5abd3f044e77`  
		Last Modified: Fri, 06 Nov 2020 23:42:04 GMT  
		Size: 144.5 MB (144484655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
