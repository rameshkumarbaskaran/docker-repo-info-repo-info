## `hylang:python3.9-windowsservercore-1809`

```console
$ docker pull hylang@sha256:d6d0225c5f23e577fac681862750038b7fcdabb0603454436472892ad6f789db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `hylang:python3.9-windowsservercore-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull hylang@sha256:a7b49b2754c3215f78e5a4618a212fe0661afb16b06732f8546d5e0aa4364097
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2770839017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57c2f988f31a78050c27ae7826bb22ec3531b1b04385017b62e5c77dd63c954`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 13:09:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 13:19:44 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Feb 2022 20:40:01 GMT
ENV PYTHON_VERSION=3.9.10
# Wed, 09 Feb 2022 20:41:57 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 09 Feb 2022 20:41:59 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 09 Feb 2022 20:42:00 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 09 Feb 2022 20:42:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/2caf84b14febcda8077e59e9b8a6ef9a680aa392/public/get-pip.py
# Wed, 09 Feb 2022 20:42:02 GMT
ENV PYTHON_GET_PIP_SHA256=7c5239cea323cadae36083079a5ee6b2b3d56f25762a0c060d2867b89e5e06c5
# Wed, 09 Feb 2022 20:43:22 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Feb 2022 20:43:24 GMT
CMD ["python"]
# Wed, 09 Feb 2022 21:07:40 GMT
ENV HY_VERSION=1.0a4
# Wed, 09 Feb 2022 21:07:41 GMT
ENV HYRULE_VERSION=0.1
# Wed, 09 Feb 2022 21:08:45 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 09 Feb 2022 21:08:51 GMT
CMD ["hy"]
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
	-	`sha256:42a7c52a40ee1a3e8513436661e94eab0212813dc541bb3fdec3e396a986d673`  
		Last Modified: Wed, 09 Feb 2022 13:27:20 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18636af143e34b43812c57e0b21385e4d35332928d3e05da13838a674908ac1`  
		Last Modified: Wed, 09 Feb 2022 20:46:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6377b29e684e9e7fe53c219331738921e9b999ec008dad2bbbfff4bd207004`  
		Last Modified: Wed, 09 Feb 2022 20:47:49 GMT  
		Size: 49.8 MB (49806445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724c1a987fd3f86f55e7b431e8f9ad3cfb16238677154593339a08466a0914d3`  
		Last Modified: Wed, 09 Feb 2022 20:46:53 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c986502fd7a23edf37577999a3cf71dbc32942d3e4b261ce0cbe78f839b7412`  
		Last Modified: Wed, 09 Feb 2022 20:46:51 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d4edc94774bed2170dcbea0b5369d7061a3b2395f5ca51e781783cc70cb515`  
		Last Modified: Wed, 09 Feb 2022 20:46:51 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1080f570faad521b8e7b037b284078d04fd12cb6c731cbe28adce2f9ebe49eec`  
		Last Modified: Wed, 09 Feb 2022 20:46:51 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701f72cfb694ce7cf2f6b3f7eac20b2d97c5e18c239b9eaca3e99137cabae2fd`  
		Last Modified: Wed, 09 Feb 2022 20:46:58 GMT  
		Size: 6.3 MB (6347805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c318a2af3665f3c54a894b673fd32ec6e102b6f2d565dc3caebe0ab5c13699`  
		Last Modified: Wed, 09 Feb 2022 20:46:51 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719f7e4dd4e9050aab1f78ccf456e6f8c5091186fb370013b44c84db944e0916`  
		Last Modified: Wed, 09 Feb 2022 21:09:40 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee264e3af935d0dd149b909c66785893f8258ad5574fa330f0005313de9fb6c4`  
		Last Modified: Wed, 09 Feb 2022 21:09:40 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7798401d4d3da3b2722132ca21c610f1e724487a382a287687a9f395a1558`  
		Last Modified: Wed, 09 Feb 2022 21:09:41 GMT  
		Size: 954.4 KB (954416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb452ff639ee3380fab28fb82ea6fa520e3cf9cbddccb1e0905ca5294f1d419`  
		Last Modified: Wed, 09 Feb 2022 21:09:40 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
