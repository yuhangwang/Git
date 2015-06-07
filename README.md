# Git
**Git version control**

This is an unofficial verbatim redistribution of the binary&source form of the Perl under its open source license (GPL 2.0) terms (see the LICENSE file).

This redistribution is under the same license as the original.

Please visit the official website for more details: https://git-scm.com

## Download
You can download the compiled binary files at the [release page](https://github.com/yuhangwang/Git/releases).

## Compilation notes
### Compilation environment
* CentOS 6.6
* x86_64 architecture 
* Kernel (GNU coreutils) 8.4
* Compiler: gcc version 4.8.4 (non-native)
* expat 2.1.0
* openssl 1.0.1m
* zlib 1.2.8
* perl 5.22.0
* python 2.7.9 
* libiconv 1.14

### Compilation steps
#### Version: 5.22.0 (2015)
```bash
wget https://www.kernel.org/pub/software/scm/git/git-2.4.2.tar.gz
tar xvf git-2.4.2
cd git-2.4.2
./configure --prefix=/Scr/scr-test-steven/install/git/2.4.2 --with-perl=/Scr/scr-test-steven/install/perl/5.22.0/bin/perl --with-python=/Scr/scr-test-steven/install/miniconda/bin/python --with-zlib=/Scr/scr-test-steven/install/zlib/1.2.8 --with-iconv=/Scr/scr-test-steven/install/libiconv/1.14 --with-expat=/Scr/scr-test-steven/install/expat/2.1.0 --with-openssl=/Scr/scr-test-steven/install/openssl/1.0.1m CC=/Scr/scr-test-steven/install/gcc/4.8.4/bin/gcc CXX=/Scr/scr-test-steven/install/gcc/4.8.4/bin/g++
make all
make test -j16 | tee QualityVerification.txt
make install
```

### Quality verification
Results:
- fixed   0
- success 11867
- failed  0
- broken  172
- total   12260

See the "QualityVerification.txt" for the output of "make check".
