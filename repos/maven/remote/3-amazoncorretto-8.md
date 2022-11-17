## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:a9b3fa8b1bd08cd3ad92eb62f85c6b9408ee7f555e4d2e7e5944ab4ed1d3519b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:9baf162459265b62ac7d29adecb821ad6638c969740614ccb25630305f1ee418
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150204495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f240aa369aa2e2a94c52497d417fbd9343e4f567dd0e2e5c9e82d347daa930e8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Thu, 17 Nov 2022 02:33:18 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Thu, 17 Nov 2022 02:33:18 GMT
ARG MAVEN_VERSION=3.8.6
# Thu, 17 Nov 2022 02:33:18 GMT
ARG USER_HOME_DIR=/root
# Thu, 17 Nov 2022 02:33:18 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Thu, 17 Nov 2022 02:33:18 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Thu, 17 Nov 2022 02:33:24 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 17 Nov 2022 02:33:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 17 Nov 2022 02:33:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 17 Nov 2022 02:33:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 17 Nov 2022 02:33:25 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 17 Nov 2022 02:33:25 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 17 Nov 2022 02:33:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 17 Nov 2022 02:33:25 GMT
CMD ["mvn"]
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
	-	`sha256:e849ae600a33cdcc6818dd0e932f55b2cfd4224da774c8a386c94e0719c27a79`  
		Last Modified: Thu, 17 Nov 2022 02:36:10 GMT  
		Size: 3.6 MB (3633089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cda69e246ce9214e9001f6c353d275d1b0ce4cfb386c6e6cb86cfb95fe628e0`  
		Last Modified: Thu, 17 Nov 2022 02:36:10 GMT  
		Size: 8.7 MB (8739501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f303660adea589a45a45f4c4ba931b4a3c7d5c8bad8a4a6a24d1e68430d563d`  
		Last Modified: Thu, 17 Nov 2022 02:36:09 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514768a4206b24c07c8b2be06fb537bff0edf1ce9f6bae9a6f6bf1919282eb25`  
		Last Modified: Thu, 17 Nov 2022 02:36:09 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ea77909159230f14f04ff66b03d9cac153e2a167accef77d4ffc1187a2b33752
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135804308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d184e0565037a1e0cbc1138893875edd40c32d4e1e0e2b6263cf2e857132d59`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 17 Nov 2022 01:39:24 GMT
ADD file:ff78f504eef6d6952dca0350e26f9d78bcb442569cbd5a99bdc6206091485de4 in / 
# Thu, 17 Nov 2022 01:39:26 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:56:04 GMT
ARG version=1.8.0_352.b08-1
# Thu, 17 Nov 2022 01:56:20 GMT
# ARGS: version=1.8.0_352.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Nov 2022 01:56:21 GMT
ENV LANG=C.UTF-8
# Thu, 17 Nov 2022 01:56:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 17 Nov 2022 02:16:57 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Thu, 17 Nov 2022 02:16:57 GMT
ARG MAVEN_VERSION=3.8.6
# Thu, 17 Nov 2022 02:16:57 GMT
ARG USER_HOME_DIR=/root
# Thu, 17 Nov 2022 02:16:57 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Thu, 17 Nov 2022 02:16:57 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Thu, 17 Nov 2022 02:16:59 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 17 Nov 2022 02:16:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 17 Nov 2022 02:16:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 17 Nov 2022 02:16:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 17 Nov 2022 02:16:59 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 17 Nov 2022 02:16:59 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 17 Nov 2022 02:16:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 17 Nov 2022 02:16:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4c4d0334d8224869629842fadc7a498ccbda1acc05e7995a0a7283b23fc39c24`  
		Last Modified: Wed, 16 Nov 2022 20:31:50 GMT  
		Size: 63.9 MB (63867424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe0acb86ae5726e590110068a908126dde5bd0fd831610cc698ee13dde7bac4`  
		Last Modified: Thu, 17 Nov 2022 01:58:33 GMT  
		Size: 59.6 MB (59581489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993318d41379e7a7b2372614362de1603630b3a1e86197cccc8c49d026769224`  
		Last Modified: Thu, 17 Nov 2022 02:19:03 GMT  
		Size: 3.6 MB (3614686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba86e7d25848813f27eb8fa746edb02b7fe91d1cf9f8c3971f6ef94c67f14f4a`  
		Last Modified: Thu, 17 Nov 2022 02:19:03 GMT  
		Size: 8.7 MB (8739498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3104d26bc5414834044e687eef19de0c65653b6f0970456b299fdab80812cf26`  
		Last Modified: Thu, 17 Nov 2022 02:19:03 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1e3ca36d065f0116809d426fb5a246c8dd9d60a86bb1a2fc0ad0ed2964d3c3`  
		Last Modified: Thu, 17 Nov 2022 02:19:03 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
