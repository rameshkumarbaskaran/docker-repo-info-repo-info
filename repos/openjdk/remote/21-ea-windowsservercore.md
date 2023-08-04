## `openjdk:21-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:57feac59488adb000b620173b6c8f268af931f10bd8ff54b99fef9c3383b5f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `openjdk:21-ea-windowsservercore` - windows version 10.0.20348.1850; amd64

```console
$ docker pull openjdk@sha256:4ba33dd366072758a3b5b2d690b36d8b62f440f2ff6e7a2843c7fc81ac0d9403
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1936408241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a79a0b1520b65bcf1cfbea89fb0fe250ffa371b5ed6384f7e7489c28240a95`
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
# Fri, 14 Jul 2023 00:15:42 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 14 Jul 2023 00:16:02 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 04 Aug 2023 00:19:18 GMT
ENV JAVA_VERSION=21-ea+34
# Fri, 04 Aug 2023 00:19:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/34/GPL/openjdk-21-ea+34_windows-x64_bin.zip
# Fri, 04 Aug 2023 00:19:20 GMT
ENV JAVA_SHA256=535816b01c3da46efed9897c95e2198dc1d3aa4b1d3e6b06da8dbdbc2cfbd4c2
# Fri, 04 Aug 2023 00:20:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 04 Aug 2023 00:20:19 GMT
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
	-	`sha256:3560c7f3a1b013c99b5d1e56ec9d9cc88ce8b0e260e6a3c90cb93033e0e1b88c`  
		Last Modified: Fri, 14 Jul 2023 00:23:40 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6724974a7b17d90890f00ea6a6f18774ebe610a0d00b09177765fa53ffa2afad`  
		Last Modified: Fri, 14 Jul 2023 00:23:40 GMT  
		Size: 261.8 KB (261755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e55912a40716e36607dcf92354c84ffba7868d8a26086040be3a8b654a4a4c`  
		Last Modified: Fri, 04 Aug 2023 00:26:19 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86794e272d2b40c96c71d4ea3e3d2d9aabe1949dd7e44e93fc5cd6f5ec31e8fb`  
		Last Modified: Fri, 04 Aug 2023 00:26:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7447c52bfd0509e00044b2a2440a45429d31159a497bbe9f21271118556bc3`  
		Last Modified: Fri, 04 Aug 2023 00:26:19 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f3c76f0a8e1ffcad8516c8fbc918db188320f5d38084864d476aa750711c6`  
		Last Modified: Fri, 04 Aug 2023 00:26:42 GMT  
		Size: 198.3 MB (198318430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc024a02a086df4007a4fd2904ff31f4704f5d81181ee99e843929ab1d98b228`  
		Last Modified: Fri, 04 Aug 2023 00:26:19 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-windowsservercore` - windows version 10.0.17763.4645; amd64

```console
$ docker pull openjdk@sha256:7858a64bf9582b08815856a2b9467eec305650dc5013e183da0517cd53d1e10c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2138660345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c878c456a2b9eb2fa569f4381fb3c1ac291ede4238e44fda8a3a110939d82b4`
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
# Fri, 14 Jul 2023 00:17:09 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 14 Jul 2023 00:18:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 04 Aug 2023 00:20:32 GMT
ENV JAVA_VERSION=21-ea+34
# Fri, 04 Aug 2023 00:20:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/34/GPL/openjdk-21-ea+34_windows-x64_bin.zip
# Fri, 04 Aug 2023 00:20:33 GMT
ENV JAVA_SHA256=535816b01c3da46efed9897c95e2198dc1d3aa4b1d3e6b06da8dbdbc2cfbd4c2
# Fri, 04 Aug 2023 00:22:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 04 Aug 2023 00:22:18 GMT
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
	-	`sha256:54c1828d13fb4970a504d87d00a20b1161a026078eaa51e2c262eb18fbff702d`  
		Last Modified: Fri, 14 Jul 2023 00:24:20 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfd78029d97c095290bc0faeb9b61506cad9ac5608f46a4a4286206a142b8ef`  
		Last Modified: Fri, 14 Jul 2023 00:24:21 GMT  
		Size: 233.5 KB (233523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ebc947aa450e9f8d2419556ce9baa672d389f839163ff051ce556744171b06`  
		Last Modified: Fri, 04 Aug 2023 00:27:01 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9ecadf1a30c9867ebb1d8dd4757630032330092f3437cd3ddc65d4cd2ced4`  
		Last Modified: Fri, 04 Aug 2023 00:27:01 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783ccd8fc45ecbcd11d610e2a6b0c6dabda1ce324d81b2d49bac84515f02ca11`  
		Last Modified: Fri, 04 Aug 2023 00:27:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1152d1bdfdee5e1f43a731f5fee9d2902ae8d8de056d9c3708985ea34661d97e`  
		Last Modified: Fri, 04 Aug 2023 00:27:23 GMT  
		Size: 198.5 MB (198496820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25dadccb58e2ca1db8ef36ad688211be7dcd336cf560995645b91fc5f0b04e74`  
		Last Modified: Fri, 04 Aug 2023 00:27:01 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
