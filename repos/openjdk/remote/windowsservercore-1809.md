## `openjdk:windowsservercore-1809`

```console
$ docker pull openjdk@sha256:31fe8ed6fac0f47bf16cd6cd9ca90f8b5eae9ed7b444a54631fef99b46842ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `openjdk:windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull openjdk@sha256:b0cc238d2ec5fb58109a0006ff9e1bcaf66a5301f49bcb8dece9599ac5be6331
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2857256315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774bc1473a4e2023b0fd4d7f21b0c3c4ede6b03b24b971efc9c191971751b038`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 15:50:04 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Jul 2022 15:59:44 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 13 Jul 2022 16:00:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 13 Jul 2022 16:00:34 GMT
ENV JAVA_VERSION=18.0.1.1
# Wed, 13 Jul 2022 16:00:35 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_windows-x64_bin.zip
# Wed, 13 Jul 2022 16:00:36 GMT
ENV JAVA_SHA256=a970b922a05a7fc2b077c89bf96c74570f65695b2ba067dc81805107517d7fed
# Wed, 13 Jul 2022 16:01:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 13 Jul 2022 16:01:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acf5949ddc551d281d19646d7dbeb4f3772073cf86c194f6d98c8afe422f3b5`  
		Last Modified: Mon, 18 Jul 2022 21:21:50 GMT  
		Size: 353.5 KB (353532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a53107fc54d6b07167f4d28e3c732e37d301032966fa143e76774137c8faa4a`  
		Last Modified: Mon, 18 Jul 2022 21:26:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14ea691370083a588e7a2b0a3cf8ec80dc9a45ee9bf4cc1042d1e4f8b07d4a5`  
		Last Modified: Mon, 18 Jul 2022 21:26:19 GMT  
		Size: 311.8 KB (311816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c708085f68b68a114263c5d641a2af7f4e0fb1f01d9531a8d967d1e588d8bed`  
		Last Modified: Mon, 18 Jul 2022 21:26:16 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893ec02694f9b7121691b901cf4e60ae5e4823a72d30227b31e83dad4134a649`  
		Last Modified: Mon, 18 Jul 2022 21:26:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7012460a2b1b290165097b3c21a2ffb00c1f1103df6763a1d7c92ea30d718a`  
		Last Modified: Mon, 18 Jul 2022 21:26:16 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78857a2df7f9a937f2f29b77307cb283ade364a6f5bd748c92c321e07bf101e`  
		Last Modified: Mon, 18 Jul 2022 21:26:37 GMT  
		Size: 184.5 MB (184539277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfed267e6dfb7f8ab8a328ba17d8cbd3c3962928e038b4ec278f5f26871693c`  
		Last Modified: Mon, 18 Jul 2022 21:26:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
