## `hylang:python3.8-windowsservercore-1809`

```console
$ docker pull hylang@sha256:3089f0d6c01af612190b5cc170fc089a2395764da9875080030fc797e309bf51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `hylang:python3.8-windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull hylang@sha256:d17a5e85d44e096f84cb07b9b2ab7a9a33e48cc4cff853bf491b8333869c87af
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2698046367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3723a6e68b51431e6090376d711e46a5a57c5920a4f9c1fbd1fc1063faa7f7f0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 12:10:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 12:15:45 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Jun 2021 16:17:32 GMT
ENV PYTHON_VERSION=3.8.10
# Wed, 09 Jun 2021 16:17:34 GMT
ENV PYTHON_RELEASE=3.8.10
# Wed, 09 Jun 2021 16:19:09 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 09 Jun 2021 16:19:11 GMT
ENV PYTHON_PIP_VERSION=21.1.2
# Wed, 09 Jun 2021 16:19:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/936e08ce004d0b2fae8952c50f7ccce1bc578ce5/public/get-pip.py
# Wed, 09 Jun 2021 16:19:16 GMT
ENV PYTHON_GET_PIP_SHA256=8890955d56a8262348470a76dc432825f61a84a54e2985a86cd520f656a6e220
# Wed, 09 Jun 2021 16:20:12 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Jun 2021 16:20:15 GMT
CMD ["python"]
# Wed, 09 Jun 2021 16:33:55 GMT
ENV HY_VERSION=1.0a1
# Wed, 09 Jun 2021 16:34:38 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 09 Jun 2021 16:34:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7863ef96846d497ea06fe442ea13dcecaf5c248ce238c69800475281a4fa848e`  
		Last Modified: Wed, 09 Jun 2021 12:20:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5789912c867ed5d9d277acf797c2a9373efb14a0496fb5ec7fce90fb3907d5b7`  
		Last Modified: Wed, 09 Jun 2021 12:21:19 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe03062817e76af2526597adbbb497c0356a565a3e5f9276946c2cd4f2cbba5`  
		Last Modified: Wed, 09 Jun 2021 16:28:28 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be5371e393aee6a3e5fb9c395057036ebfa4d69acac68fd257969997b0a44d0`  
		Last Modified: Wed, 09 Jun 2021 16:28:28 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b186c9b0540606b6b4efc85f339cdfc919c2c60ccfc102c1ad8f8cb5ff9ba`  
		Last Modified: Wed, 09 Jun 2021 16:29:21 GMT  
		Size: 49.0 MB (49039995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95118e6ae35e916cda62e18fd57c047272c27cb57011cfea4cecac896d378c7f`  
		Last Modified: Wed, 09 Jun 2021 16:28:25 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5abc047e086ac7cb5afe4f5b7164d1384209d6041e4da2cb2818433322c0a0a`  
		Last Modified: Wed, 09 Jun 2021 16:28:25 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c382c8f61fce62c7d9083cc4b03807d696f008e26bc5aa0d259abd23f634212f`  
		Last Modified: Wed, 09 Jun 2021 16:28:25 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92dc0a4ea61789c71498ab2ef15ebd15e2377fcd77e80d8c963768b3f7e9a06`  
		Last Modified: Wed, 09 Jun 2021 16:28:27 GMT  
		Size: 6.2 MB (6226523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d201ce6041bf1d605e9d8e2fcf31ec8d2546afd97521c5bca8ae7478adb6d88a`  
		Last Modified: Wed, 09 Jun 2021 16:28:25 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301102e33cb860b82ebe4766eff2457603328e47a2ec066bbdea5ec38daffd4a`  
		Last Modified: Wed, 09 Jun 2021 16:42:42 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3021435eed0fd8191e7608ee55efe476e90f43369dde4fcc16670a7427ec5072`  
		Last Modified: Wed, 09 Jun 2021 16:42:42 GMT  
		Size: 1.2 MB (1180701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f2172e988a7ce7a000214ab4a05b73600e588c8d19ab1a53e18165f40e7209`  
		Last Modified: Wed, 09 Jun 2021 16:42:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
