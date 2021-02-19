## `openjdk:17-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:1e6c676170d40dc3053f793562b5ddc453f99b0eea6cb5e8fb61fa2b6bee0312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `openjdk:17-ea-windowsservercore-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull openjdk@sha256:9d202f3b3f86fd487e3e02751409469eb223832aed5843b617823a81330750f8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2634816190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6301179fb9cb901a6aa075ad2a89d44f03e34cde0cde23e65bcb8a303f1aa6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Wed, 10 Feb 2021 13:14:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Feb 2021 16:39:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Feb 2021 16:39:45 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Feb 2021 16:40:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 18 Feb 2021 23:15:16 GMT
ENV JAVA_VERSION=17-ea+10
# Thu, 18 Feb 2021 23:15:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/10/GPL/openjdk-17-ea+10_windows-x64_bin.zip
# Thu, 18 Feb 2021 23:15:19 GMT
ENV JAVA_SHA256=692da27d3f18d7b05f5df48254b9f6b629184d981e0d47dcfc22800839477b56
# Thu, 18 Feb 2021 23:16:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 18 Feb 2021 23:16:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:433d24156d44dde3b3c6c0094ba5824a315286ae537c68f272e464fc426510f6`  
		Last Modified: Wed, 10 Feb 2021 13:40:44 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9fdb3b9c58e6d398b7f6c8c351559fc536c4ad21618a63035a7223b88bd65f`  
		Last Modified: Wed, 10 Feb 2021 17:16:08 GMT  
		Size: 9.4 MB (9416675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f54c8c307aa58138a691da27e184aae054ccca2438544a5c65c7ebfc71b4d08`  
		Last Modified: Wed, 10 Feb 2021 17:16:05 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162a0c2432ae95365715187c3e2691a5006fa137d82bc3e70d40e9fb49e11e06`  
		Last Modified: Wed, 10 Feb 2021 17:16:07 GMT  
		Size: 318.6 KB (318567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b181721e1c2cf10daafb8fc97f2fb94451adb6b0585f88f8309bc73e1e374e3`  
		Last Modified: Thu, 18 Feb 2021 23:25:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df368c5894486bdecdb22f59fc9d59fc91a57bff3276b3cc9b989130306378be`  
		Last Modified: Thu, 18 Feb 2021 23:25:34 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb4b3306ecc3767ca25c49f290129ce65181abb0ff90f017608778dc65d3eb7`  
		Last Modified: Thu, 18 Feb 2021 23:25:34 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece22db25e6bb43bccf9909874c23692927be1fed22e42fa3f2fc52eb77ed577`  
		Last Modified: Thu, 18 Feb 2021 23:29:12 GMT  
		Size: 185.8 MB (185805737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7961efe1c51016d80d43ceb91ce5eef4b859337f67d63b24b846bda8f7e7eb65`  
		Last Modified: Thu, 18 Feb 2021 23:25:34 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
