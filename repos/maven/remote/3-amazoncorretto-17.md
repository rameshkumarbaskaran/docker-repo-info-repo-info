## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:33c95adee9ded997f1ac94f8cf18bdf5c8158f23d88352ee9190cebe3f2a845c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:eab5b3974aa556a70abf4a4c27dc54a59dec2a1985d84cd0af3d7208d1246ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 MB (382153514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3969c10f7527c290d5a9f2ab0018833e346e82f3badd61d9a0107656784218e1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 07 Aug 2023 19:59:12 GMT
COPY dir:a1cfeec8f9b5a4b857222f4bbc7f5fb80ef351168a5f48841d4545523a0a3e1c in / 
# Mon, 07 Aug 2023 19:59:13 GMT
CMD ["/bin/bash"]
# Mon, 07 Aug 2023 20:55:35 GMT
ARG version=17.0.8.7-1
# Mon, 07 Aug 2023 20:55:59 GMT
# ARGS: version=17.0.8.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 07 Aug 2023 20:55:59 GMT
ENV LANG=C.UTF-8
# Mon, 07 Aug 2023 20:55:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 26 Jun 2023 13:48:06 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ARG MAVEN_VERSION=3.9.3
# Mon, 26 Jun 2023 13:48:06 GMT
ARG USER_HOME_DIR=/root
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 26 Jun 2023 13:48:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 26 Jun 2023 13:48:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c0184eb4a5d5dddba3605f9adcde7e4af58050e9e4ed44751e74957c2ad0f1b4`  
		Last Modified: Tue, 01 Aug 2023 21:03:56 GMT  
		Size: 62.5 MB (62467383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dedcccf91f7d4f86af5e1d7d84f55e2f4b1c426c4f1c6d031b3aa888fd9492`  
		Last Modified: Mon, 07 Aug 2023 21:06:56 GMT  
		Size: 152.1 MB (152121103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4ee76560c247a34e4a95f617b400173ab6d0467f8ca27748539bf9285df7c5`  
		Last Modified: Mon, 07 Aug 2023 22:15:34 GMT  
		Size: 158.2 MB (158236055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997336a3d3f06b7f6e621ddc3e1c5ba4cbe600796d21c45fbe8b3fdb0bdc7190`  
		Last Modified: Mon, 07 Aug 2023 22:15:21 GMT  
		Size: 9.3 MB (9327591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56a51919d21083cea0f1fbceee656a00a3faea1b7a6b3c4a5aceae9826781eb`  
		Last Modified: Mon, 07 Aug 2023 22:15:19 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcb8310ae9aaae2fb747a2d77ece4278da1f5d319c49d95fd0279304fa52e95`  
		Last Modified: Mon, 07 Aug 2023 22:15:19 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0201037b030a3074114db8d9b142fbf94202b9a8971de441791d168ace34548`  
		Last Modified: Mon, 07 Aug 2023 22:15:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d9589ca938f9e0acfb7ed3534fb7a6b3f5bd9e4a62d28df6017fb22daa3d4113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.5 MB (349543792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606ab05f330223192d72abdf88a6caf0a7884cfc84457ce5cd17320872d2e575`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 22 Aug 2023 19:39:53 GMT
COPY dir:e20aef745ed6033815440b78b98680b9989b365a1e5e12e6f94169e6de7e94c3 in / 
# Tue, 22 Aug 2023 19:39:54 GMT
CMD ["/bin/bash"]
# Tue, 22 Aug 2023 21:10:43 GMT
ARG version=17.0.8.7-1
# Tue, 22 Aug 2023 21:11:02 GMT
# ARGS: version=17.0.8.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 22 Aug 2023 21:11:04 GMT
ENV LANG=C.UTF-8
# Tue, 22 Aug 2023 21:11:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 18 Aug 2023 15:26:34 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ARG MAVEN_VERSION=3.9.4
# Fri, 18 Aug 2023 15:26:34 GMT
ARG USER_HOME_DIR=/root
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 18 Aug 2023 15:26:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 18 Aug 2023 15:26:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3e86c88b00180fc8094116a7111cfe1c0e88e04a6c513618fbde52ee5d97a51a`  
		Last Modified: Wed, 16 Aug 2023 18:15:18 GMT  
		Size: 64.1 MB (64127623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdade9436b16159fd5d9265f453ba919171c331fa1e67c9b2526c10356a38ac`  
		Last Modified: Tue, 22 Aug 2023 21:19:18 GMT  
		Size: 150.7 MB (150656913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e86c7b7334a41992df590ab1e70dd89b8544693793a1642c0cd56ec183a19f`  
		Last Modified: Mon, 28 Aug 2023 20:00:56 GMT  
		Size: 125.4 MB (125351456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84844a10da282f8debb06f5404e87cb469e2abb68d283065ee6d9b7fb90d69b1`  
		Last Modified: Mon, 28 Aug 2023 20:00:46 GMT  
		Size: 9.4 MB (9406421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4325437d664b8e89d381ec59fe15666cd3bb2c28e5756918d987c43ad9ea3255`  
		Last Modified: Mon, 28 Aug 2023 20:00:45 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452d76e25928d184093cd08fc8969d5bc7be596d50002b937e520ae18148d78`  
		Last Modified: Mon, 28 Aug 2023 20:00:45 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9d8c98a00ec8a15d7a331739703e6783b9499d51f4a8677f97b0a43018b70b`  
		Last Modified: Mon, 28 Aug 2023 20:00:45 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
