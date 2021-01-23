## `openjdk:17-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:fd7f97eba8ec652773350236fc8822965dd95bf1ac7d9cdb2f8d055f8fab58df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:17-jdk-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:436863f1745b66618cf36fa9279fb9ced60d6793e105487f3a7587585ec67436
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2631184596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd600bebaf93a08a29442383574a5cffdefda9351813aabb560f188e36a7be61`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 19:49:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 13 Jan 2021 19:49:02 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Jan 2021 19:49:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Sat, 23 Jan 2021 01:15:17 GMT
ENV JAVA_VERSION=17-ea+6
# Sat, 23 Jan 2021 01:15:18 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/6/GPL/openjdk-17-ea+6_windows-x64_bin.zip
# Sat, 23 Jan 2021 01:15:19 GMT
ENV JAVA_SHA256=092515916b17daf4049c14e69c0505a18150be4896e190d82c68aa962275feaa
# Sat, 23 Jan 2021 01:16:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 23 Jan 2021 01:16:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095bdf2ec48c97c5c3f23fd49bb117d66d72f8b46f5707f3c1b77227c6ca013e`  
		Last Modified: Wed, 13 Jan 2021 21:11:37 GMT  
		Size: 9.4 MB (9362296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec8ba32ad11b92749181d846d26ac913a25bbb39776d6faab16181b6f9a347`  
		Last Modified: Wed, 13 Jan 2021 21:11:32 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b643c361856e1ee8e404e05d6b434af548c27323c5c644e6f21820ba4f0d86`  
		Last Modified: Wed, 13 Jan 2021 21:11:32 GMT  
		Size: 297.9 KB (297887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b20bd81107811151d68e6c46288f32cc9c6426a2732267bf552a7b827b7321c`  
		Last Modified: Sat, 23 Jan 2021 01:31:49 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd578eebbeeff06e73b61c3a7f95894db2ee7c4bf742b4cc9b8d7f131a67cfbc`  
		Last Modified: Sat, 23 Jan 2021 01:31:49 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8367d14215cd0e686a365953d71b593d37f567540fcd52f5f929ab9ee845c742`  
		Last Modified: Sat, 23 Jan 2021 01:31:49 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66254e0a24f297561f68d63b40bdcbbae323cb585d4fd0ae9765a9acc6e9a472`  
		Last Modified: Sat, 23 Jan 2021 01:35:11 GMT  
		Size: 185.7 MB (185744643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417545cb22af9bb181caba9958294d628f23e4a63538900d1ecc37dfc957e43e`  
		Last Modified: Sat, 23 Jan 2021 01:31:49 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
