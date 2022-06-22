## `amazoncorretto:17-al2-full`

```console
$ docker pull amazoncorretto@sha256:146a92a6338d862716aaac844fdbc2560282d655bb0529823e7d848664a3adc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:afdd376caec9e7bb2b79f0974394af9cbbd0b93202578c42d465519716d088b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213982209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faec0b6e8c47a32473f13d0d90fda46a01b60ab0a52481d1bf3ca90dabc5046a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 21 Jun 2022 23:19:41 GMT
ADD file:e6c6bb016423b24a28b273cc76e9fbbf81934b77a0ede797ccfd0eeac465c8a4 in / 
# Tue, 21 Jun 2022 23:19:42 GMT
CMD ["/bin/bash"]
# Wed, 22 Jun 2022 00:03:52 GMT
ARG version=17.0.3.6-1
# Wed, 22 Jun 2022 00:04:18 GMT
# ARGS: version=17.0.3.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 22 Jun 2022 00:04:19 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jun 2022 00:04:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:017c82d6391f0bf122516eac436a6e8d77ac13282fdd13dde7e7e47dc71d447e`  
		Last Modified: Wed, 15 Jun 2022 22:09:36 GMT  
		Size: 62.3 MB (62294977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368aba68b102d7810e1273cef031aa2b8d269336955b93c1033779a40934d6ac`  
		Last Modified: Wed, 22 Jun 2022 00:07:59 GMT  
		Size: 151.7 MB (151687232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:079ef7d5850b901b6d64b882067b2824f49fb1f802e9344bda86f50fdb643450
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.2 MB (214182855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108fbc98c04dabedad5a9a6a712c891ed62789cf226e27db4c4e09e298a4add`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 May 2022 22:39:32 GMT
ADD file:c351a8c80719ef38e02c26849f50bb7d79c24a6347cc2a72ae1a0768964bd113 in / 
# Tue, 03 May 2022 22:39:34 GMT
CMD ["/bin/bash"]
# Wed, 04 May 2022 00:21:36 GMT
ARG version=17.0.3.6-1
# Wed, 04 May 2022 00:21:53 GMT
# ARGS: version=17.0.3.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 04 May 2022 00:21:54 GMT
ENV LANG=C.UTF-8
# Wed, 04 May 2022 00:21:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:ec3b4c26678b188d3874bed5e14dd278311fc05c81e418d5f0da36ec38d9f488`  
		Last Modified: Tue, 03 May 2022 03:07:52 GMT  
		Size: 63.9 MB (63902179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56929d051bcdef09602ec5a611294eb0179db14db0fc45b8ae0406d22087e0fb`  
		Last Modified: Wed, 04 May 2022 00:24:27 GMT  
		Size: 150.3 MB (150280676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
