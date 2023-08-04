## `openjdk:22-ea-jdk`

```console
$ docker pull openjdk@sha256:c665e7faa52e49eff09c21e32296368de6c6e325b8c3e28c5e9a8b945eaade32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `openjdk:22-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:359ca59a01f1f1e7facff78481eaa6e28763351350cd859ef0e7e54a003ad043
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264784674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02faaa090684cc7d705b850f646b632174b864429da6cb3459216974707081b`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:32 GMT
ADD file:6d43f7bf7c8d8c056e6fcc566ccfa2c1e42be1ef095f94d6780d0ca7d9a02e6e in / 
# Sat, 22 Jul 2023 01:20:32 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:40:55 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 22 Jul 2023 01:40:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Sat, 22 Jul 2023 01:40:55 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 22 Jul 2023 01:40:55 GMT
ENV LANG=C.UTF-8
# Fri, 04 Aug 2023 00:28:05 GMT
ENV JAVA_VERSION=22-ea+9
# Fri, 04 Aug 2023 00:28:18 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/9/GPL/openjdk-22-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='dd11f0f96ed6992b56452eee0683b50f1b550f74c31fb39e1eb1ff8a232caf68'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/9/GPL/openjdk-22-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='47ab1fb3cbe8174c21e10880e5de0c60d754cf5ba6d5cdfbe1a1d91b53b193bc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 04 Aug 2023 00:28:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49bb46380f8cb3491e82d000b27a6eb26b2490291da814ce3363bbf2c8baeb1a`  
		Last Modified: Sat, 22 Jul 2023 01:21:47 GMT  
		Size: 44.9 MB (44915006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c78e257f8d32905a5685feaf98c164b8091b3f15fb7705c4181bd3998b783`  
		Last Modified: Sat, 22 Jul 2023 01:42:50 GMT  
		Size: 15.0 MB (15009045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8760bdae2d23c39ca224829a1f6a3c23ad77b9dbb807708a97cf9ae6512bf5a7`  
		Last Modified: Fri, 04 Aug 2023 00:32:36 GMT  
		Size: 204.9 MB (204860623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fe50740cfe6a1af06ba8eee57a9cf78c9a9a37fb06292b7fc3ac684fa248986b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262476343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63353369e5b2292a87888b98b18b632566392a7d203cd3ddc440363d9a5f88ce`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 22 Jul 2023 01:03:33 GMT
ADD file:49b1f7f2b2558f78918f26b488622ad08fa607583d0a45f4f116773e2c13cf96 in / 
# Sat, 22 Jul 2023 01:03:34 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:23:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 22 Jul 2023 01:23:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Sat, 22 Jul 2023 01:23:12 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 22 Jul 2023 01:23:12 GMT
ENV LANG=C.UTF-8
# Fri, 04 Aug 2023 00:57:34 GMT
ENV JAVA_VERSION=22-ea+9
# Fri, 04 Aug 2023 00:57:44 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/9/GPL/openjdk-22-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='dd11f0f96ed6992b56452eee0683b50f1b550f74c31fb39e1eb1ff8a232caf68'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/9/GPL/openjdk-22-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='47ab1fb3cbe8174c21e10880e5de0c60d754cf5ba6d5cdfbe1a1d91b53b193bc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 04 Aug 2023 00:57:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1817bc1e6309503caf2242a5c83a4a6e9ebfdfb378d39bc92607690883a98c66`  
		Last Modified: Sat, 22 Jul 2023 01:04:31 GMT  
		Size: 43.6 MB (43623755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87786d2b4c93ec23e4ce18586fdf1f0c0ea5f810fe7a6ea02a197bf01bc37f7`  
		Last Modified: Sat, 22 Jul 2023 01:24:59 GMT  
		Size: 15.7 MB (15670540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e9da7a8b25911f00c5e89b81efd84c88aeaf7c868519c6d39cb6620b9f715`  
		Last Modified: Fri, 04 Aug 2023 01:02:08 GMT  
		Size: 203.2 MB (203182048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk` - windows version 10.0.20348.1850; amd64

```console
$ docker pull openjdk@sha256:da59548c3724108cb29f41279e928d52e4d223bb803a5322eaef53420de0be8a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1937275100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143cc7da8ced07037b938787db65ced82f4b8496913db44da60ac8063a889768`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jul 2023 21:29:32 GMT
RUN Install update 10.0.20348.1850
# Thu, 13 Jul 2023 20:29:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 00:09:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Jul 2023 00:09:40 GMT
ENV JAVA_HOME=C:\openjdk-22
# Fri, 14 Jul 2023 00:09:59 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 04 Aug 2023 00:15:35 GMT
ENV JAVA_VERSION=22-ea+9
# Fri, 04 Aug 2023 00:15:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/9/GPL/openjdk-22-ea+9_windows-x64_bin.zip
# Fri, 04 Aug 2023 00:15:37 GMT
ENV JAVA_SHA256=86de3956f3cf843d68c473831181e873e8f4ad3aad53db980302ee94bc62ae5e
# Fri, 04 Aug 2023 00:16:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 04 Aug 2023 00:16:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a7416e1317a892f4786a89c62493b21df55e0e06b82a4bb007cc79df0f949`  
		Last Modified: Tue, 11 Jul 2023 18:03:32 GMT  
		Size: 348.8 MB (348766456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3e3828ab9c4326158b6161915d8bad87619b3107529ab32863eb31b684d127`  
		Last Modified: Thu, 13 Jul 2023 21:07:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1ec6968defeeb9b60629b6fa28ca8f8abfc69ddcc9e2f6480bed84ea25681b`  
		Last Modified: Fri, 14 Jul 2023 00:21:41 GMT  
		Size: 454.6 KB (454587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055eae92651e772da902f668e71180a641b6ba052887a985152bf509f6e5a90a`  
		Last Modified: Fri, 14 Jul 2023 00:21:41 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3935ebae1fa003b7dab4fc2aceb56090efbf4f8547f35020dd20ccd0318d2709`  
		Last Modified: Fri, 14 Jul 2023 00:21:41 GMT  
		Size: 261.4 KB (261435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339aa2beb9c217902d227fc6b73ddfaddf55456d6ce435f3dcf692af99bb72bc`  
		Last Modified: Fri, 04 Aug 2023 00:24:16 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a342a1f0b9341a5f88d08089de423b3e98e306172137e49935b72d5fd61293b`  
		Last Modified: Fri, 04 Aug 2023 00:24:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ede346d16e2168b9175eae572b97545280216a01c562e2add214ed58d25bbd0`  
		Last Modified: Fri, 04 Aug 2023 00:24:16 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c748313a953537b9e1ca54ac4ac17b4cdd74bde7a3592cd55bbec87d64b43b0e`  
		Last Modified: Fri, 04 Aug 2023 00:24:38 GMT  
		Size: 199.2 MB (199185662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30f30e4e6b1faf56808004eb4b34e0f4bf1ff4bad701d351e69e38d7c4a2b4`  
		Last Modified: Fri, 04 Aug 2023 00:24:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk` - windows version 10.0.17763.4645; amd64

```console
$ docker pull openjdk@sha256:7939d2f46f741d4f70149157cb805ec97ffd6e1041d41d6159c72188ef3e0e9a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2139524655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8db1b8b5a30853d29ed19219fd781ff270efaf95a80ee832403e7e21f80b87a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 00:12:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Jul 2023 00:12:12 GMT
ENV JAVA_HOME=C:\openjdk-22
# Fri, 14 Jul 2023 00:13:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 04 Aug 2023 00:16:49 GMT
ENV JAVA_VERSION=22-ea+9
# Fri, 04 Aug 2023 00:16:50 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/9/GPL/openjdk-22-ea+9_windows-x64_bin.zip
# Fri, 04 Aug 2023 00:16:51 GMT
ENV JAVA_SHA256=86de3956f3cf843d68c473831181e873e8f4ad3aad53db980302ee94bc62ae5e
# Fri, 04 Aug 2023 00:18:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 04 Aug 2023 00:18:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b927162ea448e018f1bd7dfb1a2bc55bf21cf56e2e9a32f46a821cc0e30dd9b`  
		Last Modified: Fri, 14 Jul 2023 00:22:20 GMT  
		Size: 232.6 KB (232553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d4e9000a3e1d4472b65f93e8d52e1ab6810d932dec9367b0bdfbcd62f895ab`  
		Last Modified: Fri, 14 Jul 2023 00:22:20 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f41cc8383e028a5579a8b1df7aef79a0d3783865d9d1eb5182a4ab3a8f448`  
		Last Modified: Fri, 14 Jul 2023 00:22:20 GMT  
		Size: 233.2 KB (233206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a167c9d941e8b7c1018bc519231019bb983722a20d56669503100e2aef003252`  
		Last Modified: Fri, 04 Aug 2023 00:24:58 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb40540c37776dbeacf9ade12a8908c2d80d307e8b20232d57db57d66fdad22a`  
		Last Modified: Fri, 04 Aug 2023 00:24:58 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c83ee63d905994640ffc1acb0103d126548910b05eaa3f00cd47f2c34d5dea`  
		Last Modified: Fri, 04 Aug 2023 00:24:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c046f978f15edd6c849c1c8007be2ecac8a8a905bdfc20a8441936430bf1d8d`  
		Last Modified: Fri, 04 Aug 2023 00:25:19 GMT  
		Size: 199.4 MB (199361487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359f606ebe408270a38a3335a4797aa3d486f0891f1552d9a7812e99c7693398`  
		Last Modified: Fri, 04 Aug 2023 00:24:58 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
