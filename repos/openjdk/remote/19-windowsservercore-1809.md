## `openjdk:19-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:3d11cb053a2455f50f65ddf15fa6ceadff7ed0dab2f6b1e7c58d16c0448c86d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `openjdk:19-windowsservercore-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull openjdk@sha256:df6386b56be0a588cc047dbee1ff9d7ecc37691bdf9baa2f9133c914d6362b3d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2902537027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec98796f685316a5f1807055044557bd828e456f9d7a800d4f40867ee0183b42`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 13:09:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 18:42:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Feb 2022 18:42:46 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Feb 2022 18:43:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 04 Mar 2022 23:16:05 GMT
ENV JAVA_VERSION=19-ea+12
# Fri, 04 Mar 2022 23:16:06 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_windows-x64_bin.zip
# Fri, 04 Mar 2022 23:16:07 GMT
ENV JAVA_SHA256=13424e479ad28976926b63a14d003733a80cea14b863e28be122b782cdda29aa
# Fri, 04 Mar 2022 23:17:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 04 Mar 2022 23:17:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f0c1566a9285d9465334dc923e9d6fd93a51b3ef6cb8497efcacbcf64e3b93fc`  
		Last Modified: Wed, 09 Feb 2022 13:26:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b68a1fe6e4f618e81fe842c9b07d5a79ffffc2c21933db69d5c9e6105091560`  
		Last Modified: Wed, 09 Feb 2022 19:20:09 GMT  
		Size: 358.3 KB (358257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08343ea9810774eba7bea5b402b825bbbb597f2cb7dc0b9958270839899f0886`  
		Last Modified: Wed, 09 Feb 2022 19:20:08 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1318a28fd7f970bded95d3db9d726254043dd9127e1055fac6d3909627f9ab10`  
		Last Modified: Wed, 09 Feb 2022 19:20:08 GMT  
		Size: 311.5 KB (311525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e802828a432e3bba640df35c3e2ec0115ced56441e6277780f4564c68fd173`  
		Last Modified: Fri, 04 Mar 2022 23:24:02 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b86cb2829094e61a9cf2e47abe37092047244f9960fa6586f88f6a10bda180`  
		Last Modified: Fri, 04 Mar 2022 23:24:02 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b6b395918f8df1ad4aafd24c67d2e2f87fa33a96a9bc198be3cf8616f375ce`  
		Last Modified: Fri, 04 Mar 2022 23:24:02 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5c2a927115e76b3d3dd361bfb2d72d80b8a002fc0416be4bf3b652b35a5c23`  
		Last Modified: Fri, 04 Mar 2022 23:24:21 GMT  
		Size: 188.1 MB (188143960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc874f13bb35a1ff21b5fe2cea2155506d2fbcfe3cc4a085fbc1f2d192fc3269`  
		Last Modified: Fri, 04 Mar 2022 23:24:02 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
