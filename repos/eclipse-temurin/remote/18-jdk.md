## `eclipse-temurin:18-jdk`

```console
$ docker pull eclipse-temurin@sha256:6b0a8fea9d36f851650117a2e81654feae7d98e56b79aa8da209caaa89ce839b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `eclipse-temurin:18-jdk` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:858c2056708bdc233d4bb4254ebed74af636be535f68218344217fbd68542b1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241771206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2823c5a51ada4ae109012cb8c735781a0625df2a8cc28e28049d8e9a969bba3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 01:15:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 01:18:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Mar 2022 02:21:01 GMT
ENV JAVA_VERSION=jdk-18+36
# Thu, 31 Mar 2022 02:21:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        armhf|arm)          ESUM='4cb2e1fe9a14a990ad0dc8f3afcd9c1b37a8d7750754c3a1e72665ef6beb300f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_arm_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 31 Mar 2022 02:21:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Mar 2022 02:21:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Mar 2022 02:21:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7405b632dcc496229c61b8893b6d5aa4b72bc6af4eb9977d44655da5feea38`  
		Last Modified: Sat, 19 Mar 2022 01:23:55 GMT  
		Size: 19.8 MB (19772776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31975ad2b294737e113a6de91d4ed07a0afdc70a3bab702abb2e278fa57bc3a1`  
		Last Modified: Thu, 31 Mar 2022 02:23:23 GMT  
		Size: 193.4 MB (193432360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c343962a8c5409596003967b66bf01e1b822897769f7a5eb53afe5383174de`  
		Last Modified: Thu, 31 Mar 2022 02:23:08 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jdk` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:b561c90f31f4910dfb35887025ef78b466ce7cf39a028796648c96bd28481777
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233859663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f043e6a2eb50f0c917094626f33bd59981feadc8766b1ab2bae96e6f79d38332`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 18 Mar 2022 07:32:41 GMT
ADD file:2e353e40ad52bb1b5a10aafb7912657744b02d096925b5bfc6e925ebf7cddede in / 
# Fri, 18 Mar 2022 07:32:42 GMT
CMD ["bash"]
# Sun, 20 Mar 2022 06:32:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 20 Mar 2022 06:36:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Mar 2022 05:26:30 GMT
ENV JAVA_VERSION=jdk-18+36
# Thu, 31 Mar 2022 05:27:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        armhf|arm)          ESUM='4cb2e1fe9a14a990ad0dc8f3afcd9c1b37a8d7750754c3a1e72665ef6beb300f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_arm_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 31 Mar 2022 05:27:14 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Mar 2022 05:27:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Mar 2022 05:27:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:260b2dce5be1e0d17bf9e2ec2bbde587e5023ab1b48278ddf8396dcfc8eb7e99`  
		Last Modified: Fri, 18 Mar 2022 07:36:23 GMT  
		Size: 24.1 MB (24073481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0025c0f90a7f66ad8f3026ab615333fb7de3a759f2fa27bf660ac1a823998710`  
		Last Modified: Sun, 20 Mar 2022 06:44:24 GMT  
		Size: 19.2 MB (19194875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a9164f3e2fb68e72f66f66d20b51f519f45147cedb9a30645f8a2ae807c854`  
		Last Modified: Thu, 31 Mar 2022 05:31:38 GMT  
		Size: 190.6 MB (190591146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe8a106ff1c66f29b2929193d995009a84c11ea757b45cf6c6988261d735576`  
		Last Modified: Thu, 31 Mar 2022 05:30:24 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jdk` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:001fb0cbcf2eb297e91526bc9612940ed889a69729c31b6a1aa985765cedd012
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239969593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4577a92cbfc1a498a86cf401eccac7c33011ad7fce42213bfd259ed9c6fbce2c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:28:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 15:30:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 21:08:28 GMT
ENV JAVA_VERSION=jdk-18+36
# Wed, 30 Mar 2022 21:08:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        armhf|arm)          ESUM='4cb2e1fe9a14a990ad0dc8f3afcd9c1b37a8d7750754c3a1e72665ef6beb300f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_arm_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 30 Mar 2022 21:08:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 21:08:51 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 30 Mar 2022 21:08:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d067b9022d6a81d16f23aca9c646f37e8ffcd5aa7fef5f2b4c1ba304068489c0`  
		Last Modified: Sat, 19 Mar 2022 15:34:43 GMT  
		Size: 20.5 MB (20499729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93f52f56f2d72e4b718422437b389b2673f2eaee24acab1afd0b21ab661c353`  
		Last Modified: Wed, 30 Mar 2022 21:12:01 GMT  
		Size: 192.3 MB (192300120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b873e5c8db242e77797a82a6003c598da67fa782f9a55825305fe558567ed48`  
		Last Modified: Wed, 30 Mar 2022 21:11:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jdk` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:fb2f059bd6d71f23d8d77910e98222ac50e25f4aa134c3e9d12a5f29e924c937
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247818214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f61577e8aa7c6b5b6fe1c03b373b7072faddc739cb410876dc47849f06b1295`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:09:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 20:14:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Mar 2022 02:35:58 GMT
ENV JAVA_VERSION=jdk-18+36
# Thu, 31 Mar 2022 02:36:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        armhf|arm)          ESUM='4cb2e1fe9a14a990ad0dc8f3afcd9c1b37a8d7750754c3a1e72665ef6beb300f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_arm_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 31 Mar 2022 02:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Mar 2022 02:37:00 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Mar 2022 02:37:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6497a12e20a4d667325b1e0e9651e8ed921d66c74663b4635145a0e142a9ea05`  
		Last Modified: Sat, 19 Mar 2022 20:20:11 GMT  
		Size: 21.7 MB (21691734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd01f72a2fd493472ac97841791bfcc983b438e762a4f979bcfbe0104ef6068`  
		Last Modified: Thu, 31 Mar 2022 02:41:22 GMT  
		Size: 192.8 MB (192833905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754ae4346bb80970d977a48a54230810c146866f108c2e5974be74984deffae7`  
		Last Modified: Thu, 31 Mar 2022 02:40:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jdk` - windows version 10.0.20348.587; amd64

```console
$ docker pull eclipse-temurin@sha256:8a84b5131879ef5ecfd5916f38a3a43a66c23883d7e6a9094bcf97151bae0ad9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2576474813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e15592561f9975ac94d6454323d8a1e0b2f9376f6e04db757cfaede73454d7f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Mar 2022 19:16:27 GMT
ENV JAVA_VERSION=jdk-18+36
# Tue, 29 Mar 2022 19:17:44 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_windows_hotspot_18_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_windows_hotspot_18_36.msi ;     Write-Host ('Verifying sha256 (28280dd5453a252d412894c9a5b5bcf84ea426a9ecc20135f791f3875b73f343) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '28280dd5453a252d412894c9a5b5bcf84ea426a9ecc20135f791f3875b73f343') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 29 Mar 2022 19:18:07 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 29 Mar 2022 19:18:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b398541ac61e4677466afb49d3fa757dfaab0e0f00ad0429539f57e23c5851f`  
		Last Modified: Tue, 29 Mar 2022 19:25:42 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf53b55c620aa80961ecc2d5ce39115befcf9cef14516dec17e612804988082`  
		Last Modified: Tue, 29 Mar 2022 19:26:08 GMT  
		Size: 354.7 MB (354686505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65788e54710cd66fe7da94ba7d402c6b31eef7f7b4d89be2b0b55dc95d9ec49c`  
		Last Modified: Tue, 29 Mar 2022 19:25:42 GMT  
		Size: 537.0 KB (537003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c4cd42fbdca4f40855f92188a032a8e66104a1ed924c9c90489a45ea63330f`  
		Last Modified: Tue, 29 Mar 2022 19:25:41 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jdk` - windows version 10.0.17763.2686; amd64

```console
$ docker pull eclipse-temurin@sha256:49ca01916c30ded2b246b66e77eefca3edd26ba727cc9fcc6e357d6e2fb1de6c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3073727666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24158f013192767da6e541ca70bf47a69635adbe85fcf6f54755004d113f4bcd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Mar 2022 19:18:24 GMT
ENV JAVA_VERSION=jdk-18+36
# Tue, 29 Mar 2022 19:20:04 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_windows_hotspot_18_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_windows_hotspot_18_36.msi ;     Write-Host ('Verifying sha256 (28280dd5453a252d412894c9a5b5bcf84ea426a9ecc20135f791f3875b73f343) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '28280dd5453a252d412894c9a5b5bcf84ea426a9ecc20135f791f3875b73f343') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 29 Mar 2022 19:20:59 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 29 Mar 2022 19:20:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479191988f9d7e176f618a8b18ec264f4264da6e4352fe26feb7fdd8979bcb6e`  
		Last Modified: Tue, 29 Mar 2022 19:26:21 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30788becbab576dc590adacdd46c150d5425236239162af29e33b877335a3a1`  
		Last Modified: Tue, 29 Mar 2022 19:26:48 GMT  
		Size: 354.5 MB (354473547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a85355742809af161026dee1d7a0a2fd87dba394571075553e90db39df6a2e`  
		Last Modified: Tue, 29 Mar 2022 19:26:25 GMT  
		Size: 3.8 MB (3797454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0cf80d044b4a679b93c9b910c42c59f317bb04efe0858c8d7b76bf48fa67929`  
		Last Modified: Tue, 29 Mar 2022 19:26:21 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
