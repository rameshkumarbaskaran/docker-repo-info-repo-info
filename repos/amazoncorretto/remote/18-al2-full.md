## `amazoncorretto:18-al2-full`

```console
$ docker pull amazoncorretto@sha256:5b16f214b22319beece5724a7780c65c853460255a13c83d6740f8c575b5d3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:18-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:42109c6f06e5729f32aaf469c5cdcc3b40e18240a536d4cacaeca6f232c836c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (214994209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbeb164c915984751fefb405ddd5c1443f8bf0f54e7ffe6cfaa11b63ccd9de00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 21 Jun 2022 23:19:41 GMT
ADD file:e6c6bb016423b24a28b273cc76e9fbbf81934b77a0ede797ccfd0eeac465c8a4 in / 
# Tue, 21 Jun 2022 23:19:42 GMT
CMD ["/bin/bash"]
# Wed, 22 Jun 2022 00:04:32 GMT
ARG version=18.0.1.10-1
# Wed, 22 Jun 2022 00:04:57 GMT
# ARGS: version=18.0.1.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-18-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-18-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 22 Jun 2022 00:04:57 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jun 2022 00:04:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-18-amazon-corretto
```

-	Layers:
	-	`sha256:017c82d6391f0bf122516eac436a6e8d77ac13282fdd13dde7e7e47dc71d447e`  
		Last Modified: Wed, 15 Jun 2022 22:09:36 GMT  
		Size: 62.3 MB (62294977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a0a10fa0153185a284506e580f8551abed59e99bebe6589c1d1e1152182d30`  
		Last Modified: Wed, 22 Jun 2022 00:08:35 GMT  
		Size: 152.7 MB (152699232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:18-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:51b583038a4fcb9f6b89c4caf3cce9a7aacef6353f928d892f5e1d0d7fc22ad9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215267350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5252f1ad1a8687c460e0011ee37eb7a00d5375ce242c8cf293690a2769b52e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 May 2022 22:39:32 GMT
ADD file:c351a8c80719ef38e02c26849f50bb7d79c24a6347cc2a72ae1a0768964bd113 in / 
# Tue, 03 May 2022 22:39:34 GMT
CMD ["/bin/bash"]
# Wed, 04 May 2022 00:22:02 GMT
ARG version=18.0.1.10-1
# Wed, 04 May 2022 00:22:19 GMT
# ARGS: version=18.0.1.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-18-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-18-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 04 May 2022 00:22:19 GMT
ENV LANG=C.UTF-8
# Wed, 04 May 2022 00:22:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-18-amazon-corretto
```

-	Layers:
	-	`sha256:ec3b4c26678b188d3874bed5e14dd278311fc05c81e418d5f0da36ec38d9f488`  
		Last Modified: Tue, 03 May 2022 03:07:52 GMT  
		Size: 63.9 MB (63902179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e4b006e4296412de23db80958843b6fb204408bbb0567c787c90b5bc821204`  
		Last Modified: Wed, 04 May 2022 00:25:04 GMT  
		Size: 151.4 MB (151365171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
