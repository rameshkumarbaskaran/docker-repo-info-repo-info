## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:08b992411dad7c8ba928e6c6cc775b9c6667fa0d2304d7718626cf4c298804d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fecce5dd42e4a22eb17bad71708ddc46c1b6ad840e1a56f3157335f3c3be7ff9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137830693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d885899b12131609af53eee34147a6493d3c697135be11585d91a69fdc769e87`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:32:34 GMT
ADD file:d5f7c1dc2e62cbd216adb0c4ff82770915f2b4e4660989515782faeca4e486ed in / 
# Thu, 17 Nov 2022 01:32:35 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:49:48 GMT
ARG version=1.8.0_352.b08-1
# Thu, 17 Nov 2022 01:50:08 GMT
# ARGS: version=1.8.0_352.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Nov 2022 01:50:09 GMT
ENV LANG=C.UTF-8
# Thu, 17 Nov 2022 01:50:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:68028ec3b506bca4d81560b5fcbd408dc7cc49f4b1717a69d5396ff22700f80a`  
		Last Modified: Wed, 16 Nov 2022 20:32:28 GMT  
		Size: 62.3 MB (62262225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34cf93602c3cc903e430dc668610135919ed5282725f1e24640cf42482d35c0`  
		Last Modified: Thu, 17 Nov 2022 01:54:34 GMT  
		Size: 75.6 MB (75568468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1b269447fa2db7853607c1a2323898e2ca7bf806a5b757af7bd0db14681a2053
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123564985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e3da38a00e3f99ab4e92b7d0dc0aaf495a047fb6d7e3a207e09d8040940a91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:05 GMT
ADD file:26a6bf75c84c408d289e5569f13b1c65206966f875cdfc53ded0670cb85e35bf in / 
# Fri, 16 Dec 2022 00:41:07 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 00:58:43 GMT
ARG version=1.8.0_352.b08-1
# Fri, 16 Dec 2022 00:58:59 GMT
# ARGS: version=1.8.0_352.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 16 Dec 2022 00:59:00 GMT
ENV LANG=C.UTF-8
# Fri, 16 Dec 2022 00:59:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:6cbfee25f0741b3d3f4d2474d904a200cd8404a01aa17813bf3fc3d4ebb551a4`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 64.0 MB (63964214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a121fca9c95ea048128fa2a5b56995a6dc72e90529f4fa242e9f7c3e9b2cc56d`  
		Last Modified: Fri, 16 Dec 2022 01:02:51 GMT  
		Size: 59.6 MB (59600771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
