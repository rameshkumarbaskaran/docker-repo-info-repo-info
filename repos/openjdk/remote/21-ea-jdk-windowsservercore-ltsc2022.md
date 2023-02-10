## `openjdk:21-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:b7d5d8a2f41c5c4ed5e4c94833c32eb8c3bf9ad870f9476a2cf7943fd2e0a4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `openjdk:21-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull openjdk@sha256:14f68ecc8062297b8297d6a494a52ccd4251758edfc33262ee3931ddb328a97d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1581920888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4665ee85d1720a646ea87c61711c0e1668c1d2c6ff5baa521dbacc7760ccefb0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:07:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 12 Jan 2023 05:07:35 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 12 Jan 2023 05:07:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 10 Feb 2023 02:27:35 GMT
ENV JAVA_VERSION=21-ea+9
# Fri, 10 Feb 2023 02:27:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/9/GPL/openjdk-21-ea+9_windows-x64_bin.zip
# Fri, 10 Feb 2023 02:27:37 GMT
ENV JAVA_SHA256=012fada2a58fa64ab3708ede97876c32050dc6c4dd4c77d29740af88954bda8d
# Fri, 10 Feb 2023 02:28:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 10 Feb 2023 02:28:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa8e5b91e3c425a756945d0dec251c1595992592fd0dcf4df0ec0a7962717eb`  
		Last Modified: Thu, 12 Jan 2023 05:22:24 GMT  
		Size: 614.6 KB (614563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6284573ed998f0926754c8fd5dc7faff95102e54cf06b0d280cd07428b048e11`  
		Last Modified: Thu, 12 Jan 2023 05:22:23 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee2720203565dd5e40979d2f76187379d7c05254dd58609d0f974f653b1db40`  
		Last Modified: Thu, 12 Jan 2023 05:22:24 GMT  
		Size: 552.5 KB (552462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77768473679370111c8347f195303eeb940e63de9342f3fc27c5b4f425939c4`  
		Last Modified: Fri, 10 Feb 2023 08:19:19 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf24a65ae5a38e62750b15ba92cfbfa2e75c03970da78c6b0225f710328eb52`  
		Last Modified: Fri, 10 Feb 2023 08:19:20 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f608b9bd8e16cc754a4ac67afa67f2f9b2d7d94cb9b0db9b9af3e7547f3b3c`  
		Last Modified: Fri, 10 Feb 2023 08:19:19 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801bf561f508b19e8fdcf97ba53a3346cac7592211cd3c73d032cbbab5fef155`  
		Last Modified: Fri, 10 Feb 2023 08:19:44 GMT  
		Size: 194.7 MB (194716339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d86622f9504232ed7289e49e6b21f546f91d2296bf774ff9dca32b294bdcc7`  
		Last Modified: Fri, 10 Feb 2023 08:19:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
