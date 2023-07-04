## `openjdk:22-jdk`

```console
$ docker pull openjdk@sha256:77539e7ec9c02cff6ab62ba19ccefa94274ab26bc7a5e8b41816d837226d6622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `openjdk:22-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:0f1cfdc95cd8e4dc56ccdd5bb2d858e053085d2edca243d32d0183c7cbf78602
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264536627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2baa3e3941142c713adab6520c97792df06497fff10f68d017c02fa5213e71e4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Jul 2023 02:04:16 GMT
ADD file:7a7c6d19e1a4f691c6bd96ea6b7568f6cc041fce11298e57d51913b978e9e7e3 in / 
# Tue, 04 Jul 2023 02:04:17 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 17:47:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 04 Jul 2023 17:47:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Tue, 04 Jul 2023 17:47:25 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 17:47:25 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 17:47:25 GMT
ENV JAVA_VERSION=22-ea+4
# Tue, 04 Jul 2023 17:47:37 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/4/GPL/openjdk-22-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='111b948b388db6860600e818e37829ff19879485028ba8cf17540ce995a34f47'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/4/GPL/openjdk-22-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='69ecb18f5d29ab95fefcbb70d7a1a4c7059383e949e8c44b95c08240f56fcd18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 04 Jul 2023 17:47:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e2c03c89dcad02e83fe01768b82c438fcf60b831104614ca96ed5d8df01db295`  
		Last Modified: Tue, 04 Jul 2023 02:05:27 GMT  
		Size: 44.9 MB (44876686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1589371ef7dbf0bbba39e839420d2a593e729690f3c9a3a1cc86d3cd6b47912`  
		Last Modified: Tue, 04 Jul 2023 17:50:16 GMT  
		Size: 15.0 MB (14998167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44845a72c4f79f4c8ca58e0cea962131156abed5b979591b7a35812b09762de`  
		Last Modified: Tue, 04 Jul 2023 17:50:26 GMT  
		Size: 204.7 MB (204661774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:50c92674482d209f23a808c367564a2a1430c202091386f993013c0c94251c79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262268808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ceba5a1f24e446533bd5953a8713416f26b40628f66dd465d36e142f78d168`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Jul 2023 00:52:20 GMT
ADD file:1313260ee8b32fa94bcf06c44034cd7e4f9baf44c7df9e74facfe21323b37292 in / 
# Tue, 04 Jul 2023 00:52:21 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 01:17:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 04 Jul 2023 01:17:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Tue, 04 Jul 2023 01:17:21 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 01:17:21 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 01:17:21 GMT
ENV JAVA_VERSION=22-ea+4
# Tue, 04 Jul 2023 01:17:30 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/4/GPL/openjdk-22-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='111b948b388db6860600e818e37829ff19879485028ba8cf17540ce995a34f47'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/4/GPL/openjdk-22-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='69ecb18f5d29ab95fefcbb70d7a1a4c7059383e949e8c44b95c08240f56fcd18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 04 Jul 2023 01:17:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29e800056b7e3d5007df41c0ad55416bb45d5863affcf39316c5755e71b20a30`  
		Last Modified: Tue, 04 Jul 2023 00:53:16 GMT  
		Size: 43.6 MB (43595268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4e6eec249ed9ec194f18c4c5eda620b32132cc41a2083ec5505ff863774f15`  
		Last Modified: Tue, 04 Jul 2023 01:21:26 GMT  
		Size: 15.7 MB (15676974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b91b9babde351c99ca98df89abb6e946885e0ec6aefc34b84377ff364972c5`  
		Last Modified: Tue, 04 Jul 2023 01:21:37 GMT  
		Size: 203.0 MB (202996566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-jdk` - windows version 10.0.20348.1787; amd64

```console
$ docker pull openjdk@sha256:c226ed88e46c9a0fa9a63c76dadb85a0bebccd3dfecbf6b4da894ccac3f69fe4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1625932499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179837025578a3e83d80dbd051a16d3ee054257269bfa0cbf7752b5448e8b9ef`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:03:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:03:12 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 24 Jun 2023 03:03:36 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 04 Jul 2023 01:41:10 GMT
ENV JAVA_VERSION=22-ea+4
# Tue, 04 Jul 2023 01:41:11 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/4/GPL/openjdk-22-ea+4_windows-x64_bin.zip
# Tue, 04 Jul 2023 01:41:11 GMT
ENV JAVA_SHA256=f6f42b34f2a3c8b8589ed792d6131ad804b46c9ae10f15e14215bcd203b12ddf
# Tue, 04 Jul 2023 01:41:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 04 Jul 2023 01:41:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de10d117b5ef80c7852b0714d37536955d84892882d5f3f97a4d53631493623`  
		Last Modified: Sat, 24 Jun 2023 03:12:27 GMT  
		Size: 318.8 KB (318813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42164a02c7f5d71bd26777e64b91b0bd8307f2753488ee14e31eb3bf123f1815`  
		Last Modified: Sat, 24 Jun 2023 03:12:27 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300b25e7f376e2eb14f637c2bc345eeb47edb02cc31dd17445ef2acc2140c0ff`  
		Last Modified: Sat, 24 Jun 2023 03:12:27 GMT  
		Size: 262.6 KB (262553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d95d8911cd3f1bcacb776978e1186c9a04d259719e1c1c02969d678291f1f2`  
		Last Modified: Tue, 04 Jul 2023 01:47:22 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0f49e85a24256a634b6442b15d33be4b3448d87864595eba1266e7a0a3cb5e`  
		Last Modified: Tue, 04 Jul 2023 01:47:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd95e471842a50da22e396b2d10e1d2fffda5ea0277177056df4eaae0b671625`  
		Last Modified: Tue, 04 Jul 2023 01:47:22 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb7a8751d8015bdd17216f1c65f1ed2aeb699bd0b67e08af48fc88b952bafd`  
		Last Modified: Tue, 04 Jul 2023 01:47:39 GMT  
		Size: 199.0 MB (199044042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89dceea3101695d602f073e60b633d8a4346c2f65aa28bf97a5f5db95c4eb5`  
		Last Modified: Tue, 04 Jul 2023 01:47:22 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-jdk` - windows version 10.0.17763.4499; amd64

```console
$ docker pull openjdk@sha256:b37425e6b7e2044245aedb78497083b54537aacf01070f506acd9d8f22993705
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1850373929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d2ea05096d3ecc2b19de5b9db68a3a91ee848780c9bff34040dc5eb67d80a5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:05:10 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:05:10 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 24 Jun 2023 03:05:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 04 Jul 2023 01:42:12 GMT
ENV JAVA_VERSION=22-ea+4
# Tue, 04 Jul 2023 01:42:12 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/4/GPL/openjdk-22-ea+4_windows-x64_bin.zip
# Tue, 04 Jul 2023 01:42:13 GMT
ENV JAVA_SHA256=f6f42b34f2a3c8b8589ed792d6131ad804b46c9ae10f15e14215bcd203b12ddf
# Tue, 04 Jul 2023 01:43:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 04 Jul 2023 01:43:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aac08fa1b04894a4c928b70e656c1b7852ba8379bb8fe87ce2a32e04c6af9b`  
		Last Modified: Sat, 24 Jun 2023 03:13:06 GMT  
		Size: 307.3 KB (307316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad0afa7177a851a3fceae50db434e766370d9487c708af1fc32dd5edf289185`  
		Last Modified: Sat, 24 Jun 2023 03:13:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b054a91391984528b6740330d63cb33f1d165aa84e83ee25395d9d5645dc67f`  
		Last Modified: Sat, 24 Jun 2023 03:13:06 GMT  
		Size: 257.7 KB (257721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0c438aa83134871fdd5edd950142687c3dce086c2d79507ccaf7ab62f68a98`  
		Last Modified: Tue, 04 Jul 2023 01:47:58 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e9c8395054e2a3704b285e5c5d790f0315b52320c96a3851cdbb3a177d71c6`  
		Last Modified: Tue, 04 Jul 2023 01:47:58 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da11677586400306f99990f798d8094689cf0ff35a1007d090875c736bd31a30`  
		Last Modified: Tue, 04 Jul 2023 01:47:58 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7114144e29952d3c002b3642b10da20f58aa7fbcb7d5c86df6f13d712fbbfe`  
		Last Modified: Tue, 04 Jul 2023 01:48:17 GMT  
		Size: 199.1 MB (199063745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376074f32b3e1fc074369aedee8d95d6f67765366b47e8bc7686c7db769bd8a2`  
		Last Modified: Tue, 04 Jul 2023 01:47:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
