## `openjdk:18-jdk`

```console
$ docker pull openjdk@sha256:3e9dc18ea0c8584ca636a3f6c3af46e95286f89463172a7fbe1ef257ac2c7ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `openjdk:18-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:a7cd96ef84bfc74c2be885f525de1c31a81eb183f9c7035e9221ad5d42aeda57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244370063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eddf69230084b7bedec480a043e572807388832e91c5bef637a78d67b839ba`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 May 2022 20:51:06 GMT
ADD file:b2c3e9f338a70507ba6d9ec21f28c7023f4120a45f234ff9a28188119091c60b in / 
# Mon, 02 May 2022 20:51:06 GMT
CMD ["/bin/bash"]
# Mon, 02 May 2022 21:07:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 02 May 2022 21:08:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Mon, 02 May 2022 21:08:25 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 May 2022 21:08:25 GMT
ENV LANG=C.UTF-8
# Mon, 02 May 2022 21:08:25 GMT
ENV JAVA_VERSION=18.0.1.1
# Mon, 02 May 2022 21:08:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-x64_bin.tar.gz'; 			downloadSha256='4f81af7203fa4c8a12c9c53c94304aab69ea1551bc6119189c9883f4266a2b24'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='e667166c47e90874af3641ad4a3952d3c835627e4301fa1f0d620d9b6e366519'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 02 May 2022 21:08:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:121b730bab02bd12143950d97a621f2d2dcf4723433bbadc2777d594c871ee71`  
		Last Modified: Mon, 02 May 2022 20:51:57 GMT  
		Size: 42.1 MB (42114330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b275ba7e0da7889811d55da69069fd42118dd8875faded11d9d21a813afe7b`  
		Last Modified: Mon, 02 May 2022 21:13:42 GMT  
		Size: 13.5 MB (13531997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986241e01958a3d1fc12bc5a6c6e97f3b8c1008c0735292898156d88bf62223`  
		Last Modified: Mon, 02 May 2022 21:15:03 GMT  
		Size: 188.7 MB (188723736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:915f4924fb7ef9af2dea55d1ee0a2046740c06f45bd9a6afef4ff061a234ff27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243953754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e79a005797ea13cc8bfef3a667858d6e3a21a8011dc359f2d4336598a26658`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 May 2022 21:46:34 GMT
ADD file:e59d0ab85f777209561c628874489b9544223a23fed0755bedd408a55452b4af in / 
# Mon, 02 May 2022 21:46:35 GMT
CMD ["/bin/bash"]
# Mon, 02 May 2022 22:06:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 02 May 2022 22:07:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Mon, 02 May 2022 22:07:25 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 May 2022 22:07:26 GMT
ENV LANG=C.UTF-8
# Mon, 02 May 2022 22:07:27 GMT
ENV JAVA_VERSION=18.0.1.1
# Mon, 02 May 2022 22:07:55 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-x64_bin.tar.gz'; 			downloadSha256='4f81af7203fa4c8a12c9c53c94304aab69ea1551bc6119189c9883f4266a2b24'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='e667166c47e90874af3641ad4a3952d3c835627e4301fa1f0d620d9b6e366519'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 02 May 2022 22:07:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d35f3f87cf615a8684aa1b866b03a7078bce1beea91489effc1e6c03c83124c`  
		Last Modified: Mon, 02 May 2022 21:47:34 GMT  
		Size: 42.0 MB (42016620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e242efb2259690773e11adafa3652b3b5f5ac58742dfba66216c5527ec988`  
		Last Modified: Mon, 02 May 2022 22:17:46 GMT  
		Size: 14.3 MB (14292260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b465aca2bba621872c9adcf3e6a5a8ad81b145804735f70a52a0c71b179c4e`  
		Last Modified: Mon, 02 May 2022 22:19:23 GMT  
		Size: 187.6 MB (187644874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-jdk` - windows version 10.0.20348.643; amd64

```console
$ docker pull openjdk@sha256:c2737b934e479c8274c5c3028dadfa37145b1fcc1050d20553c724c1ec28d3bc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2412936083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673cd8df5c05aa30edd6488e20d1afc7db6723e8067820178f0c2fce5fc216bb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 16:55:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Apr 2022 17:01:20 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 13 Apr 2022 17:01:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 02 May 2022 19:15:21 GMT
ENV JAVA_VERSION=18.0.1.1
# Mon, 02 May 2022 19:15:22 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_windows-x64_bin.zip
# Mon, 02 May 2022 19:15:23 GMT
ENV JAVA_SHA256=a970b922a05a7fc2b077c89bf96c74570f65695b2ba067dc81805107517d7fed
# Mon, 02 May 2022 19:16:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 02 May 2022 19:16:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c156288a763e09322f37d1214a5fcfaa1ebfbf8a108ee1351f5321537e137ef`  
		Last Modified: Tue, 19 Apr 2022 00:49:30 GMT  
		Size: 629.6 KB (629633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4efacdfbaec31fa6b09d408321a0190182c52e7733aebf425e810589e6a002`  
		Last Modified: Tue, 19 Apr 2022 00:54:32 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d8176b8196229b69e6c6055dcfb1b8dc8defc575f480e72150dc4ea9af10c4`  
		Last Modified: Tue, 19 Apr 2022 00:54:32 GMT  
		Size: 560.3 KB (560302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe3f917052b3b8c423deee3ba550ff7744c0e2a6d1d3dfc6a68b1d9f32c49cb`  
		Last Modified: Mon, 02 May 2022 19:22:33 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2247ebf2ea0e1c60a6aa56125a450094edb67acdcf15e00445144faaff2910`  
		Last Modified: Mon, 02 May 2022 19:22:34 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e02437b125ef9f1bdbf5b06bbdf6fd3581247700e0fa3972d5c0ef7a59567d`  
		Last Modified: Mon, 02 May 2022 19:22:34 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86e03d9dbf8e1769dba2881cb055369591b2b7b407d61ca3688077775087bc5`  
		Last Modified: Mon, 02 May 2022 19:25:43 GMT  
		Size: 184.8 MB (184782825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69519208c7c9cd652fa3ef6b64e840d54c012a5ecea93e153a51cdd70a53bbbd`  
		Last Modified: Mon, 02 May 2022 19:22:33 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-jdk` - windows version 10.0.17763.2803; amd64

```console
$ docker pull openjdk@sha256:e1800d66b50a6a8c8cce048d8c71b566aad64952ac0126ac5e6f0fb84c7ef68b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2901175774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5e47cebf5e2d868a3697479b53affec73b718d1594a639b46533768a8a61c1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 16:58:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Apr 2022 17:02:47 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 13 Apr 2022 17:03:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 02 May 2022 19:16:34 GMT
ENV JAVA_VERSION=18.0.1.1
# Mon, 02 May 2022 19:16:35 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_windows-x64_bin.zip
# Mon, 02 May 2022 19:16:36 GMT
ENV JAVA_SHA256=a970b922a05a7fc2b077c89bf96c74570f65695b2ba067dc81805107517d7fed
# Mon, 02 May 2022 19:18:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 02 May 2022 19:18:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25b7048e3be90e8d3856a943edfe91e214649883ffeabdf6fcebcea7b3053e2`  
		Last Modified: Tue, 19 Apr 2022 00:53:10 GMT  
		Size: 366.7 KB (366674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9de7521db9c103d3c09b50654509330ba97ad59a10798b1689d22cf19153e4`  
		Last Modified: Tue, 19 Apr 2022 00:55:06 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e090da1b82810ceb5d7c72b193690a77d6c3248a4515b91974f90a1a5a01eee9`  
		Last Modified: Tue, 19 Apr 2022 00:55:06 GMT  
		Size: 322.7 KB (322657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9856fd43ba4d2fa11e4fd6bc26dfcad06046acb86969b9c666c63516b642e7d1`  
		Last Modified: Mon, 02 May 2022 19:26:10 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9113783055e0a636c26c556990eb614d63825012317176f9277967aa51366845`  
		Last Modified: Mon, 02 May 2022 19:26:10 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb7257e4ceba4066e01244dd0add10c7acd740d67973badcf87e87b97af3290`  
		Last Modified: Mon, 02 May 2022 19:26:10 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4612152a6111b62be06baf464018c37f5ba4b83e3f7c06a6a99ddd6c05cf3c63`  
		Last Modified: Mon, 02 May 2022 19:29:19 GMT  
		Size: 184.6 MB (184557628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21031a14c71ff71b62df17540ae7b066d67ac30147f11fe7bc3b6762cb082447`  
		Last Modified: Mon, 02 May 2022 19:26:10 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
