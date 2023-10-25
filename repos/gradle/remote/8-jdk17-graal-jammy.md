## `gradle:8-jdk17-graal-jammy`

```console
$ docker pull gradle@sha256:c676cb003ebdd9504f7ad7fd17018177e8d4d230587aa711a50582875e8afa03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:8-jdk17-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:a7fc6c6dfb004cf95b737c339902f32460344c19cc940315ee063abea328c018
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.9 MB (578926523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bf2b6a707c50bbb0cba3fa7f501c301417fe40514c6e605855bf81735e535d`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 06:06:03 GMT
CMD ["gradle"]
# Fri, 13 Oct 2023 06:06:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 13 Oct 2023 06:06:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 13 Oct 2023 06:06:04 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 13 Oct 2023 06:06:04 GMT
WORKDIR /home/gradle
# Fri, 13 Oct 2023 06:06:41 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 13 Oct 2023 06:06:42 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 25 Oct 2023 00:20:09 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 25 Oct 2023 00:20:24 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_DOWNLOAD_SHA256=E47BA7229CEF02393E19D5B8F46F7F1CAB4829DD17BFE84D5431FC8FF0E22A96     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version
# Wed, 25 Oct 2023 00:20:25 GMT
ENV GRADLE_VERSION=8.4
# Wed, 25 Oct 2023 00:20:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e1af3ae886920c3ac87f7a91f816c0c7c436f276a6eefdb3da152100fef72ae
# Wed, 25 Oct 2023 00:20:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e1af3ae886920c3ac87f7a91f816c0c7c436f276a6eefdb3da152100fef72ae
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 25 Oct 2023 00:20:30 GMT
USER gradle
# Wed, 25 Oct 2023 00:20:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e1af3ae886920c3ac87f7a91f816c0c7c436f276a6eefdb3da152100fef72ae
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 25 Oct 2023 00:20:31 GMT
USER root
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b87f8379caa0c66ee56c57c6325cf7ae7cbf937e479e9328734bf67724dc8ad`  
		Last Modified: Fri, 13 Oct 2023 06:14:19 GMT  
		Size: 4.4 KB (4360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b613d28ccd16ad0c8979a793bd2b1e662e8915b6fd5e9fad4bd2933eef7246a1`  
		Last Modified: Fri, 13 Oct 2023 06:14:37 GMT  
		Size: 126.4 MB (126408966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226a08224bce2fb82b8cb615f86f2132f6e59e11ef314a0514d6aeac9240e709`  
		Last Modified: Wed, 25 Oct 2023 00:24:24 GMT  
		Size: 291.1 MB (291064200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a8aee8b3aa39f99b6acfdeae2400b234fcd72366c2e5adb1218623b4e019ff`  
		Last Modified: Wed, 25 Oct 2023 00:24:12 GMT  
		Size: 131.0 MB (131009718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b98f336c18e6758b5ab2f6d4db638046100ab9106478511b0138e41063b37ce`  
		Last Modified: Wed, 25 Oct 2023 00:24:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
