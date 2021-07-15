## `maven:3-amazoncorretto-15`

```console
$ docker pull maven@sha256:20411a0146b2f1f21f948e4b3bae8bc48de9797b9c0ad296c6c079610e7e737e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-15` - linux; amd64

```console
$ docker pull maven@sha256:4e062b848f019b201fe7955c3909fadf489e314ba22830bb214349d42a6af4ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230772995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9757f4e520784d485800926a213a16a5ea0972a30e564df6aa0fb0c790e0fc26`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 30 Mar 2021 21:59:20 GMT
ADD file:3b750ce7e7425c1cb02261d65b1e301d5818cda51a80dc8ab3b915ee5ca37d4e in / 
# Tue, 30 Mar 2021 21:59:21 GMT
CMD ["/bin/bash"]
# Wed, 31 Mar 2021 16:18:21 GMT
ARG version=15.0.2.7-1
# Wed, 31 Mar 2021 16:18:48 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 31 Mar 2021 16:18:49 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 16:18:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
# Mon, 05 Apr 2021 17:54:29 GMT
ARG MAVEN_VERSION=3.8.1
# Mon, 05 Apr 2021 17:54:30 GMT
ARG USER_HOME_DIR=/root
# Mon, 05 Apr 2021 17:54:30 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Mon, 05 Apr 2021 17:54:30 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Mon, 05 Apr 2021 17:54:40 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Mon, 05 Apr 2021 17:54:47 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 05 Apr 2021 17:54:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 05 Apr 2021 17:54:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 05 Apr 2021 17:54:48 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 05 Apr 2021 17:54:48 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 05 Apr 2021 17:54:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 05 Apr 2021 17:54:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:99a21848b482c10fd4b103b7ab95e1446142e76e3dfa673efd0a23fb264ec5e5`  
		Last Modified: Tue, 30 Mar 2021 13:54:37 GMT  
		Size: 61.9 MB (61946585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3379c3b288ddbf110cbd7b0253fb21fe3f2a2d3ffd94a0e9900addbae96511`  
		Last Modified: Wed, 31 Mar 2021 16:21:36 GMT  
		Size: 155.7 MB (155665050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07081e9a675df25b30c9662f59d523524dd0f4ede219c785a103e290c3a7e626`  
		Last Modified: Mon, 05 Apr 2021 18:05:37 GMT  
		Size: 3.5 MB (3549190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee1a774b794215ce72e3d715f7a9925c32086a33cbd171e5872a3a27123bc8c`  
		Last Modified: Mon, 05 Apr 2021 18:05:38 GMT  
		Size: 9.6 MB (9610959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70f3198135a1c99a0cbed2798fec6d20fa26afc304ab8c525e9381c27c969ec`  
		Last Modified: Mon, 05 Apr 2021 18:05:37 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025559103cde0aab181f64b4e794a377b54a7ec5653979f13a6afc2fa46e61fa`  
		Last Modified: Mon, 05 Apr 2021 18:05:36 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-15` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:42362d842b5d77750831e4e03fd1ea7e11f4d2de7c24299c6e60b412d85af2e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232420988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bee2b3c49f5fd9a9bd254e8a81eec062d4ccfe19c6a29affcd4538425c2c5d1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 30 Mar 2021 21:59:58 GMT
ADD file:540e42c4903b87925bc490b00820f555e531041d1b1fcea6ee56f4cc3bbc895d in / 
# Tue, 30 Mar 2021 22:00:02 GMT
CMD ["/bin/bash"]
# Wed, 31 Mar 2021 14:32:36 GMT
ARG version=15.0.2.7-1
# Wed, 31 Mar 2021 14:33:07 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 31 Mar 2021 14:33:09 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 14:33:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
# Thu, 27 May 2021 19:08:44 GMT
ARG MAVEN_VERSION=3.8.1
# Thu, 27 May 2021 19:08:44 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 May 2021 19:08:44 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Thu, 27 May 2021 19:08:44 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Thu, 27 May 2021 19:08:52 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Thu, 27 May 2021 19:08:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 27 May 2021 19:08:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 May 2021 19:08:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 May 2021 19:08:55 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 27 May 2021 19:08:55 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 27 May 2021 19:08:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 May 2021 19:08:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7d8296f22a3c3f786ce15fb5be7dce44af09932e617f9a981183619985014031`  
		Last Modified: Tue, 30 Mar 2021 22:01:09 GMT  
		Size: 63.7 MB (63660038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfc9724882bdd07db925d6ad95126645ae01699690c670e87372a6c9452b5b8`  
		Last Modified: Wed, 31 Mar 2021 14:35:46 GMT  
		Size: 155.6 MB (155559423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4f087c879573034d5a20b2042433e2f438279ae3429952defe2ca948396a10`  
		Last Modified: Thu, 27 May 2021 19:19:59 GMT  
		Size: 3.6 MB (3589330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6397046a5d9ef2df2430684a0d725087bb4d53f30d8af95e59989f30add58056`  
		Last Modified: Thu, 27 May 2021 19:19:59 GMT  
		Size: 9.6 MB (9610982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d518970283e3992db935e3b7aa216dd14b88ab91276ffa6f27a80e30028a0f`  
		Last Modified: Thu, 27 May 2021 19:19:58 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2388ba910caafe0dc055f07c28187657c8cc284d4a1aacae0f8690a214b4b21`  
		Last Modified: Thu, 27 May 2021 19:19:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
