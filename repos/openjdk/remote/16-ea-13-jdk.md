## `openjdk:16-ea-13-jdk`

```console
$ docker pull openjdk@sha256:9fb391bc6c82ffdf798b9fa55ee9f947b1e8b1cb971cec9fa433ac94e83dc5c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1397; amd64
	-	windows version 10.0.14393.3866; amd64

### `openjdk:16-ea-13-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:e8465d5c284e8acf737b408d0a3b0de7baa8e5c9c10511ccb2045cfb904834ea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263323000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27170195b411939cc96e7d660115094fd5674321c7c7d7917be91f87b8899c1b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 24 Jul 2020 00:21:31 GMT
ADD file:02670bc2999f43239e261c6f4e819f10471cfababa139f0eeba033a934c44eed in / 
# Fri, 24 Jul 2020 00:21:31 GMT
CMD ["/bin/bash"]
# Wed, 26 Aug 2020 21:28:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 26 Aug 2020 21:28:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 26 Aug 2020 21:28:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Wed, 26 Aug 2020 21:28:11 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Aug 2020 22:30:07 GMT
ENV JAVA_VERSION=16-ea+13
# Thu, 27 Aug 2020 22:30:18 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/13/GPL/openjdk-16-ea+13_linux-aarch64_bin.tar.gz; 			downloadSha256=ff0e6702cc9aa6aad0d1399db28526d41e3c89d09293e3f322d3cee01b7a1d7d; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/13/GPL/openjdk-16-ea+13_linux-x64_bin.tar.gz; 			downloadSha256=c5a1067ea4822157a4476bbab01ed581d6992bd788b45505a3dd32ef4deb16b0; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		javac --version; 	java --version
# Thu, 27 Aug 2020 22:30:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1bbe67b820dbc81dda19341c188f2504cb57d03d540dc94bf12e3f752102adf8`  
		Last Modified: Fri, 24 Jul 2020 00:23:22 GMT  
		Size: 53.2 MB (53238241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c479ccfad94616e2be168f7843f91429bd9a7d0996b687d670bfe633136895a`  
		Last Modified: Wed, 26 Aug 2020 21:33:04 GMT  
		Size: 13.4 MB (13417665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c79b1ee67fe49cb991322a988e91db747f89f083eed6d25872483d2fef7bd9e`  
		Last Modified: Thu, 27 Aug 2020 22:34:19 GMT  
		Size: 196.7 MB (196667094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-13-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f98fee5563488d2b315a4eee00ab9d228b91cf8a919afe13e9d0da2cfab6981f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242893428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a929098107b65cadb649dfeaf1834ea41336acfe9d9ccbb29fad6c9fe3c64bc1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 24 Jul 2020 00:53:42 GMT
ADD file:2ad87b72223c423a2c0741208d69b5b361aabaa96bfbe1510fa44745a72c0e7f in / 
# Fri, 24 Jul 2020 00:53:46 GMT
CMD ["/bin/bash"]
# Wed, 26 Aug 2020 21:35:59 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 26 Aug 2020 21:36:01 GMT
ENV LANG=en_US.UTF-8
# Wed, 26 Aug 2020 21:36:03 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Wed, 26 Aug 2020 21:36:04 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Aug 2020 22:40:00 GMT
ENV JAVA_VERSION=16-ea+13
# Thu, 27 Aug 2020 22:40:59 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/13/GPL/openjdk-16-ea+13_linux-aarch64_bin.tar.gz; 			downloadSha256=ff0e6702cc9aa6aad0d1399db28526d41e3c89d09293e3f322d3cee01b7a1d7d; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/13/GPL/openjdk-16-ea+13_linux-x64_bin.tar.gz; 			downloadSha256=c5a1067ea4822157a4476bbab01ed581d6992bd788b45505a3dd32ef4deb16b0; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		javac --version; 	java --version
# Thu, 27 Aug 2020 22:41:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e618d2a55163b9d055a0c627bc7faff5f4210ee92e01ce1b82dd0738d8c5e12`  
		Last Modified: Fri, 24 Jul 2020 00:55:39 GMT  
		Size: 53.3 MB (53345174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed03d65a39d352a49fbfba9a4223490a35071d814a500f1e7a378ce915dd32f6`  
		Last Modified: Wed, 26 Aug 2020 21:40:32 GMT  
		Size: 14.3 MB (14331702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec44484f17e6e43a453c5bbf57ddd242457bd22262f1b913b466fc7710532eb`  
		Last Modified: Thu, 27 Aug 2020 22:44:48 GMT  
		Size: 175.2 MB (175216552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-13-jdk` - windows version 10.0.17763.1397; amd64

```console
$ docker pull openjdk@sha256:06b1384bd9673413ebfa427149e508adc1a1086f1327549353c9f8a7c1ac8ded
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2542264509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fda89b21c7e48129ea4dd0f14ecd5007c8b77a7d44d2f7741dbb94d8bc3d58`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 15:20:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 12 Aug 2020 15:20:32 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 12 Aug 2020 15:20:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 27 Aug 2020 22:14:17 GMT
ENV JAVA_VERSION=16-ea+13
# Thu, 27 Aug 2020 22:14:18 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/13/GPL/openjdk-16-ea+13_windows-x64_bin.zip
# Thu, 27 Aug 2020 22:14:19 GMT
ENV JAVA_SHA256=054db7127dd6aaf511122fb635ed2d0c77aab20ce9cfe6c6c0b0a89910d354bc
# Thu, 27 Aug 2020 22:15:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 27 Aug 2020 22:15:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43065500f09f35124a5d71517aa493fd23ad75660682600f7f6b40aa7629ac78`  
		Last Modified: Tue, 11 Aug 2020 20:54:54 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61325951c8c59861a712789969f747b1171e1a463d838cc58ec539e09209ac0e`  
		Last Modified: Wed, 12 Aug 2020 16:08:33 GMT  
		Size: 9.1 MB (9149173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b85fd778f4a6d3cd93553accf4bfc8b282ee060683d4289cdb4def2dd78a15`  
		Last Modified: Wed, 12 Aug 2020 16:08:31 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ec4e041da1cd72477b2a3db3cfa7c178f24e8fda9bd70cee26c9db8c5e5cd7`  
		Last Modified: Wed, 12 Aug 2020 16:08:29 GMT  
		Size: 300.5 KB (300490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ab39b50296f58bf4d829b4c51c498599a8ab6312beeb93c1e082dbae1ee7c5`  
		Last Modified: Thu, 27 Aug 2020 22:24:00 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5406eb0e76d114ed5e79048dc087531f3931c65912d8f6b8768ded94fc5e002`  
		Last Modified: Thu, 27 Aug 2020 22:24:00 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29557148806a3d1c322dcfcdc394256da4c43c0fa01d71fd121e8925f308ce38`  
		Last Modified: Thu, 27 Aug 2020 22:24:00 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fd8188d22655972f3cc19191501a89796bbb1d50389638a550e4eaf1506977`  
		Last Modified: Thu, 27 Aug 2020 22:24:20 GMT  
		Size: 196.9 MB (196941085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ea2ede2e8fcc77fc2f82b5e31557c45837a784acaf144dbf165dc303a25805`  
		Last Modified: Thu, 27 Aug 2020 22:24:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-13-jdk` - windows version 10.0.14393.3866; amd64

```console
$ docker pull openjdk@sha256:a3c1c2968af0c82782979591adbb442c9dfee633daac1b0bd84c72c018800f8f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5955447308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1baa1b7421dd0a720dc687b79962065bf2980903719ef12ce52cc8b8db8a12d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Aug 2020 20:31:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 15:24:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 12 Aug 2020 15:24:17 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 12 Aug 2020 15:25:29 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 27 Aug 2020 22:16:13 GMT
ENV JAVA_VERSION=16-ea+13
# Thu, 27 Aug 2020 22:16:14 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/13/GPL/openjdk-16-ea+13_windows-x64_bin.zip
# Thu, 27 Aug 2020 22:16:14 GMT
ENV JAVA_SHA256=054db7127dd6aaf511122fb635ed2d0c77aab20ce9cfe6c6c0b0a89910d354bc
# Thu, 27 Aug 2020 22:18:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 27 Aug 2020 22:18:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:32838d9637dc39d4acee78700b0f93d6c8c9d2db755f12c8009c1b51687d3fbd`  
		Last Modified: Tue, 11 Aug 2020 20:54:28 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138271f8777367b1ff54a3d43137d564baa693e3e0b71305261b35b9720e7779`  
		Last Modified: Wed, 12 Aug 2020 16:09:25 GMT  
		Size: 9.9 MB (9868368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34771dfe42ef423846ebfe01aab83001e3cc7208753079693787f39ae976a049`  
		Last Modified: Wed, 12 Aug 2020 16:09:20 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25894be8edb605a7d00928789801b5eaa84815ceb02fd359924f3252fffeae0d`  
		Last Modified: Wed, 12 Aug 2020 16:09:24 GMT  
		Size: 5.3 MB (5344121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fb6b2fd331b1812a8b9fcbd0e7eb8aef12c17242325cd3aa066e538b4fb056`  
		Last Modified: Thu, 27 Aug 2020 22:24:41 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eb4c1d1c3b25aaf8672bc7128490bface0408986c0c9cbff2f1a76a6dcee17`  
		Last Modified: Thu, 27 Aug 2020 22:24:41 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef63a0facbb497f1453bb5a98f15ac80db0ee465b3cd1984d21edaba47eaee60`  
		Last Modified: Thu, 27 Aug 2020 22:24:41 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dde91683703007fdd80a1c07ed5abe1b2838179c78ca7eac21d8103f8c2a14`  
		Last Modified: Thu, 27 Aug 2020 22:25:03 GMT  
		Size: 202.1 MB (202080489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1f87a3bfdc86b68410abd9c9f8fa40e264841a37781b05bb2c1e94571e4427`  
		Last Modified: Thu, 27 Aug 2020 22:24:41 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
