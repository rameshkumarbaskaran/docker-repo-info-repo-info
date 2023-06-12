## `openjdk:22-ea-1-jdk`

```console
$ docker pull openjdk@sha256:5ac2abc48990d1f50be7d4be24a4c82e0ca655e5d065208feaf5449f6212448d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `openjdk:22-ea-1-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:4d8c5b5ebbed517c5285a7fbb17720b063d5dd3a4858e6e435e1405cb3950d25
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264597842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7dcdf456e88050cd77dca1aad45b3f79eebe5778727e87a02ae0accb57f1701`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 04 Jun 2023 17:54:32 GMT
ADD file:39d09c6c7c3a0f64981f5cbcb12cc8f0128979c3d4b91d74c84fe62aca5ea87e in / 
# Sun, 04 Jun 2023 17:54:32 GMT
CMD ["/bin/bash"]
# Sun, 04 Jun 2023 19:01:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 12 Jun 2023 22:26:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Mon, 12 Jun 2023 22:26:29 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jun 2023 22:26:29 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 22:26:29 GMT
ENV JAVA_VERSION=22-ea+1
# Mon, 12 Jun 2023 22:26:40 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='50bf6303955ea128be3eb7ad9bc10f5e7eeacf9d3f81349a4d60a164fe7d0318'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ca14677cb2db094acbc9b084d0a85c9e004aff9826977e0b9b35e5f9a55b550'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Jun 2023 22:26:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e0c3751e6482e67b70ffad144b2cb9aec9be672df2642a322e875e51b748aeb`  
		Last Modified: Sun, 04 Jun 2023 17:55:32 GMT  
		Size: 44.9 MB (44872720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5b8981d150f5706ec1b30f459a99b1c25abb86225512911608e4175546c8d9`  
		Last Modified: Sun, 04 Jun 2023 19:02:11 GMT  
		Size: 15.0 MB (15004426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede12e8bc9615c77ffdc13709569c7eea1c5e9f139b87d298d66056e999aebbd`  
		Last Modified: Mon, 12 Jun 2023 22:29:14 GMT  
		Size: 204.7 MB (204720696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-1-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c9570e934c44ed253516668006de9447398f919d7e01574a0694291754bf9ba3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262678261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6212db0c2caf6323075f3b0c1cede93424132cc0c709ac56e1fb1ef20e6cc440`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 02 Jun 2023 22:40:44 GMT
ADD file:ae7c6036695430900f5ff735197e9c0281881b97faaea00e40263ca539fe7fff in / 
# Fri, 02 Jun 2023 22:40:45 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 22:57:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 12 Jun 2023 21:45:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Mon, 12 Jun 2023 21:45:38 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jun 2023 21:45:38 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 21:45:38 GMT
ENV JAVA_VERSION=22-ea+1
# Mon, 12 Jun 2023 21:45:54 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='50bf6303955ea128be3eb7ad9bc10f5e7eeacf9d3f81349a4d60a164fe7d0318'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ca14677cb2db094acbc9b084d0a85c9e004aff9826977e0b9b35e5f9a55b550'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Jun 2023 21:45:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ae143351a4fc570e80462825e827f3afbbabc4488aeae617542d42b521e5248`  
		Last Modified: Fri, 02 Jun 2023 22:41:37 GMT  
		Size: 43.8 MB (43787831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76745f42ba06c52f3c8c98a56266981889c3e5541a95f8478f09f378b9807208`  
		Last Modified: Fri, 02 Jun 2023 22:58:08 GMT  
		Size: 15.8 MB (15841478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb9326c55c0ee4fa3118e56f2a7daf288cdc0518a08b4be5cb16a1caf06e9cb`  
		Last Modified: Mon, 12 Jun 2023 21:48:34 GMT  
		Size: 203.0 MB (203048952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-1-jdk` - windows version 10.0.20348.1726; amd64

```console
$ docker pull openjdk@sha256:e6e33a3fa0de28e4bfbba484b83750306fabf0503ef20d700375e81f89a94a1c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1974831011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fbfcf710ee042c2b3748736a7ba418fa524b66eb63e44104171351792bbc08`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 02:50:46 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Jun 2023 22:15:18 GMT
ENV JAVA_HOME=C:\openjdk-22
# Mon, 12 Jun 2023 22:15:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Jun 2023 22:15:39 GMT
ENV JAVA_VERSION=22-ea+1
# Mon, 12 Jun 2023 22:15:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_windows-x64_bin.zip
# Mon, 12 Jun 2023 22:15:40 GMT
ENV JAVA_SHA256=9348aa2fc8344b25baad9b614627983b4e900ab0293ecfa3ec7f9b5d911a90a7
# Mon, 12 Jun 2023 22:16:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Jun 2023 22:16:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6500851308f2a80744cfa1cca578e46041bad797f47ea2d8c83f894349fac438`  
		Last Modified: Wed, 10 May 2023 03:00:03 GMT  
		Size: 448.7 KB (448735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1b04d8e86e4fc820778c292565a927a7c0b8ab6e1485798be522acb1563f99`  
		Last Modified: Mon, 12 Jun 2023 22:21:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aa27f4debf297ef66d2791e5d0af76f9dc4fcac1d414654f55c9b39cb94a61`  
		Last Modified: Mon, 12 Jun 2023 22:21:54 GMT  
		Size: 277.5 KB (277469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38bd61921c415cf3c98572bb9bc5439936ca29afde180c04aa52ca52a7ab19a`  
		Last Modified: Mon, 12 Jun 2023 22:21:52 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45407f149dbf3373d601485ca6637450b7723ecc4a1a073606db489cf06bc78c`  
		Last Modified: Mon, 12 Jun 2023 22:21:52 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cc61bf231d80c6aba410b215c5b6ae89436263117e417e953502921f3c38c0`  
		Last Modified: Mon, 12 Jun 2023 22:21:52 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2723c53892b2a4204019188c3cf473db6debd89ad87b02ecfeebcb54c03308f4`  
		Last Modified: Mon, 12 Jun 2023 22:22:12 GMT  
		Size: 199.1 MB (199114912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92b36563970ba8c57a18a3f8fef1ffd9244fe979ebc049fd31ce9f68e214cd1`  
		Last Modified: Mon, 12 Jun 2023 22:21:52 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-1-jdk` - windows version 10.0.17763.4377; amd64

```console
$ docker pull openjdk@sha256:d6ea93f44d7bfb01ce8c63611279925939f9789e6ae091041eefc6010d7d6c7e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2271891888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d416d56812fcba564d8e5807a6ea8a3358c83109b04944b02d71cc77a88cdbbc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 02:54:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Jun 2023 22:16:46 GMT
ENV JAVA_HOME=C:\openjdk-22
# Mon, 12 Jun 2023 22:17:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Jun 2023 22:17:52 GMT
ENV JAVA_VERSION=22-ea+1
# Mon, 12 Jun 2023 22:17:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_windows-x64_bin.zip
# Mon, 12 Jun 2023 22:17:54 GMT
ENV JAVA_SHA256=9348aa2fc8344b25baad9b614627983b4e900ab0293ecfa3ec7f9b5d911a90a7
# Mon, 12 Jun 2023 22:19:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Jun 2023 22:19:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8712378a27a3538d7991a50dcb72abb565959575008a538c012500547b6acf3a`  
		Last Modified: Wed, 10 May 2023 03:00:47 GMT  
		Size: 441.2 KB (441178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935d762527d6f1add4088cc0ab3991053e000bfd4560c108c26a7035e7696c89`  
		Last Modified: Mon, 12 Jun 2023 22:22:33 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd9ec7f7d94b4eea218042df62b1b72b17c8b7d20fe097e10af338974242be2`  
		Last Modified: Mon, 12 Jun 2023 22:22:34 GMT  
		Size: 287.9 KB (287921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39dbcca709d578723c523e59b3f235cf74fbf1ee2e7f56b8af7ca583dbeb32b`  
		Last Modified: Mon, 12 Jun 2023 22:22:31 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d587e0b256f7c4877b2f3118fc72b255b77a3ef4e341fab27cd2ead3ecd72f`  
		Last Modified: Mon, 12 Jun 2023 22:22:32 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372f7b50b5360f599037ce9eaebf620382483c241121de3f1f613420629a3695`  
		Last Modified: Mon, 12 Jun 2023 22:22:31 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ae92cac99b99c329d5f9ec33593fbaa0af02373d585b50ea26e7f6b2f5cdd`  
		Last Modified: Mon, 12 Jun 2023 22:22:51 GMT  
		Size: 199.1 MB (199119075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2a4c9ef5bdff03bd226a83669251226e8617a54111e639f2b811dc963f9c57`  
		Last Modified: Mon, 12 Jun 2023 22:22:32 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
