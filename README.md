## Laboratory work I

<a href="https://yandex.ru/efir/?stream_id=vsVJzkz4i9-s"><img src="https://raw.githubusercontent.com/tp-labs/lab01/master/preview.png" width="640"/></a>

Данная лабораторная работа посвещена изучению утилит для разработки проектов

## Tasks

- [x] 1. Ознакомиться со ссылками учебного материала
- [x] 2. Выполнить инструкцию учебного материала
- [x] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Tutorial

```bash
$ export GITHUB_USERNAME=scorpy2013
$ export GIST_TOKEN=0dc94d9c9fe7556bc832fbc82e5b22c21b58328c 
$ alias edit=<nano|vi|vim|subl>
```

```sh
$ mkdir -p ${GITHUB_USERNAME}/workspace
$ cd ${GITHUB_USERNAME}/workspace
$ pwd
/c/Users/User/Documents/Vuse Downloads/ТиМП/workspace
$ cd ..
$ pwd
/c/Users/User/Documents/Vuse Downloads/ТиМП
```

```sh
$ mkdir -p workspace/tasks/
$ mkdir -p workspace/projects/
$ mkdir -p workspace/reports/
$ cd workspace
```

```sh
# Debian
$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
--2020-04-11 18:20:27--  https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
Resolving nodejs.org (nodejs.org)... 104.20.22.46, 104.20.23.46
Connecting to nodejs.org (nodejs.org)|104.20.22.46|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9356460 (8,9M) [application/x-xz]
Saving to: 'node-v6.11.5-linux-x64.tar.xz'
node-v6.11.5-linux-x64.tar.xz                      100%[================================================================================================================>]   8,92M   124KB/s    in 73s
2020-04-11 18:23:18 (128 KB/s) - 'node-v6.11.5-linux-x64.tar.xz' saved [9356460/9356460]

$ tar -xf node-v6.11.5-linux-x64.tar.xz
$ rm -rf node-v6.11.5-linux-x64.tar.xz
$ mv node-v6.11.5-linux-x64 node
```

```sh
$ ls node/bin
node  npm
$ echo ${PATH} 
/mingw64/bin:/usr/bin:/c/Users/User/bin:/c/Ruby26-x64/bin:/c/Program Files (x86)/Common Files/Oracle/Java/javapath:/c/Program Files (x86)/NVIDIA Corporation/PhysX/Common:/c/Windows/system32:/c/Windows:/c/Windows/System32/Wbem:/c/Windows/System32/WindowsPowerShell/v1.0:/c/Program Files (x86)/Microsoft SQL Server/110/Tools/Binn:/c/Program Files/Microsoft SQL Server/110/Tools/Binn:/c/Program Files (x86)/mingw-w64/i686-8.1.0-posix-dwarf-rt_v6-rev0/mingw32/bin:/c/Program Files/Microsoft SQL Server/110/DTS/Binn:/c/Program Files/dotnet:/c/Program Files/Microsoft SQL Server/130/Tools/Binn:/c/Program Files/MATLAB/R2019b/bin:/cmd:/mingw64/bin:/usr/bin:/c/Program Files/CMake/bin:/c/Program Files/wget
$ export PATH=${PATH}:`pwd`/node/bin
$ echo ${PATH}
/mingw64/bin:/usr/bin:/c/Users/User/bin:/c/Ruby26-x64/bin:/c/Program Files (x86)/Common Files/Oracle/Java/javapath:/c/Program Files (x86)/NVIDIA Corporation/PhysX/Common:/c/Windows/system32:/c/Windows:/c/Windows/System32/Wbem:/c/Windows/System32/WindowsPowerShell/v1.0:/c/Program Files (x86)/Microsoft SQL Server/110/Tools/Binn:/c/Program Files/Microsoft SQL Server/110/Tools/Binn:/c/Program Files (x86)/mingw-w64/i686-8.1.0-posix-dwarf-rt_v6-rev0/mingw32/bin:/c/Program Files/Microsoft SQL Server/110/DTS/Binn:/c/Program Files/dotnet:/c/Program Files/Microsoft SQL Server/130/Tools/Binn:/c/Program Files/MATLAB/R2019b/bin:/cmd:/mingw64/bin:/usr/bin:/c/Program Files/CMake/bin:/c/Program Files/wget:/c/Users/User/scorpy2013/scorpy2013/node/bin
$ mkdir scripts
$ cat > scripts/activate<<EOF
export PATH=\${PATH}:`pwd`/node/bin
EOF
$ source scripts/activate
```

```sh
$ gem install gist
```
Successfully installed gist-5.1.0
Parsing documentation for gist-5.1.0
Done installing documentation for gist after 0 seconds
1 gem installed
```sh
$ (umask 0077 && echo ${GIST_TOKEN} > ~/.gist)
```

## Report

```sh
$ export LAB_NUMBER=01
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gist REPORT.md
```

## Links

### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix))
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix))
- [cd](https://en.wikipedia.org/wiki/Cd_(command))
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix))
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix))
- [echo](https://en.wikipedia.org/wiki/Echo_(command))
- [env](https://en.wikipedia.org/wiki/Env_(shell))
- [ex](https://en.wikipedia.org/wiki/Ex_(editor))
- [file](https://en.wikipedia.org/wiki/File_(command))
- [find](https://en.wikipedia.org/wiki/Find)
- [ls](https://en.wikipedia.org/wiki/Ls)
- [man](https://en.wikipedia.org/wiki/Man_page)
- [mkdir](https://en.wikipedia.org/wiki/Mkdir)
- [mv](https://en.wikipedia.org/wiki/Mv)
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix))
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix))
- [pwd](https://en.wikipedia.org/wiki/Pwd)
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix))
- [sed](https://en.wikipedia.org/wiki/Sed)
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix))

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software)) | [yum](https://fedoraproject.org/wiki/Yum/ru)
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh)
- [npm](https://docs.npmjs.com)

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details)
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf)
- [clang](https://clang.llvm.org)
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html)
- [make](https://en.wikipedia.org/wiki/Make_(software))
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html)
- [openssl](https://www.openssl.org)
- [nano](https://www.nano-editor.org)
- [tree](https://linux.die.net/man/1/tree)
- [vim](http://www.vim.org)

## Homework

- [x] 1. Скачайте библиотеку *boost* с помощью утилиты **wget**. Адрес для скачивания `https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz`.
- [x] 2. Разархивируйте скаченный файл в директорию `~/boost_1_69_0`
- [x] 3. Подсчитайте количество файлов в директории `~/boost_1_69_0` **не включая** вложенные директории.
- [x] 4. Подсчитайте количество файлов в директории `~/boost_1_69_0` **включая** вложенные директории.
- [x] 5. Подсчитайте количество заголовочных файлов, файлов с расширением `.cpp`, сколько остальных файлов (не заголовочных и не `.cpp`).
- [x] 6. Найдите полный пусть до файла `any.hpp` внутри библиотеки *boost*.
- [x] 7. Выведите в консоль все файлы, где упоминается последовательность `boost::asio`.
- [x] 8. Скомпилирутйе *boost*. Можно воспользоваться [инструкцией](https://www.boost.org/doc/libs/1_61_0/more/getting_started/unix-variants.html#or-build-custom-binaries) или [ссылкой](https://codeyarns.com/2017/01/24/how-to-build-boost-on-linux/).
- [x] 9. Перенесите все скомпилированные на предыдущем шаге статические библиотеки в директорию `~/boost-libs`.
- [x] 10. Подсчитайте сколько занимает дискового пространства каждый файл в этой директории.
- [x] 11. Найдите *топ10* самых "тяжёлых".
1 ```sh
--2020-04-11 19:25:05--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
Resolving sourceforge.net (sourceforge.net)... 216.105.38.13
Connecting to sourceforge.net (sourceforge.net)|216.105.38.13|:443... connected.
HTTP request sent, awaiting response... 301 Moved Permanently
Location: https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/ [following]
--2020-04-11 19:25:07--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/
Connecting to sourceforge.net (sourceforge.net)|216.105.38.13|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/download [following]
--2020-04-11 19:25:11--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/download
Connecting to sourceforge.net (sourceforge.net)|216.105.38.13|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: https://downloads.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?r=&ts=1586252046&use_mirror=netix [following]
--2020-04-11 19:25:13--  https://downloads.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?r=&ts=1586252046&use_mirror=netix
Resolving downloads.sourceforge.net (downloads.sourceforge.net)... 216.105.38.13
Connecting to downloads.sourceforge.net (downloads.sourceforge.net)|216.105.38.13|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: https://netix.dl.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz [following]
--2020-04-11 19:25:15--  https://netix.dl.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz
Resolving netix.dl.sourceforge.net (netix.dl.sourceforge.net)... 87.121.121.2
Connecting to netix.dl.sourceforge.net (netix.dl.sourceforge.net)|87.121.121.2|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 111710205 (107M) [application/x-gzip]
Saving to: 'boost_1_69_0.tar.gz'
boost_1_69_0.tar.gz                                100%[================================================================================================================>] 106,53M   112KB/s    in 12m 10s
2020-04-11 19:37:26 (128 KB/s) - 'boost_1_69_0.tar.gz' saved [111710205/111710205]
```
2.
```sh
$ tar -xf boost_1_69_0.tar.gz # распаковываем архив
```

```sh
$ cd boost_1_69_0 
$ pwd
/c/Users/User/scorpy2013/scorpy2013/boost_1_69_0 
```

3.

```sh
 $ ls -f . | wc -l # Считаем количество файлов в директории **boost**
20
   ```
  4.
   $ find . -type f | wc -l
61191
5.
```sh
User@ScorpyDesktop MINGW64 ~/scorpy2013/scorpy2013/boost_1_69_0 (master)
$ find . -type f -name '*.h' | wc -l # Находим все файлы с расширением '*.h' (заголовочный файл)
241
User@ScorpyDesktop MINGW64 ~/scorpy2013/scorpy2013/boost_1_69_0 (master) 
$ find . -type f -name '*.cpp' | wc -l  # Находим все файлы с расширением '*.сpp' (файл на с++)
12464
User@ScorpyDesktop MINGW64 ~/scorpy2013/scorpy2013/boost_1_69_0 (master) 
$ find . -type f '!' -name '*.cpp' -a '!' -name '*.cpp' | wc -l # Находим все файлы, кроме расширения '*.cpp' и '*.cpp'
36472
```
```sh
6.
$ find . -type f -name 'any.hpp' # Полный пусть до файла 'any.hpp' 
./boost/any.hpp
./boost/fusion/algorithm/query/any.hpp
./boost/fusion/algorithm/query/detail/any.hpp
./boost/fusion/include/any.hpp
./boost/hana/any.hpp
./boost/hana/fwd/any.hpp
./boost/proto/detail/any.hpp
./boost/spirit/home/support/algorithm/any.hpp
./boost/type_erasure/any.hpp
./boost/xpressive/detail/utility/any.hpp
```

7.
```sh
boot_1_69_0/boost/asio/async_result.hpp
...
boost_1_69_0/doc/html/process/reference.html
```

8.
 ```sh
mv boost_1_69_0/=boost_output/lib/ boost-libs/ 
```

9.
 ```sh
mv boost_1_69_0/=boost_output/lib/ boost-libs/# Перенесем статические библиотеки в директорию ~/boost-libs
```

10. 
```sh
$ find . type -f -exec du -h {} +; # дисковое пространство файла в директории
100K ./libboost_stacktrace_basic.a
2,4M ./libboost_wave.dylib
7,8M ./libboost_math_tr1.a
5,4M ./libboost_python27.a 164K ./libboost_thread.dylib 100K ./libboost_math_c99f.dylib
480K ./libboost_$
1,9M ./libboost_math_c99f.a
1,8M ./libboost_math_c99l.a
1,3M ./libboost_iostreams.a
1,1M ./libboost_thread.a
7,3M ./libboost_program_options.a
188K ./libboost_iostreams.dylib
300K ./libboost_coroutine.a
276K ./libboost_timer.a
412K ./libboost_wserialization.dylib 940K ./libboost_contract.a
172K ./libboost_contract.dylib 892K ./libboost_numpy27.a
740K ./libboost_type_erasure.a
21M ./libboost_log_setup.a
16K ./libboost_atomic.a
208K ./libboost_random.a
104K ./libboost_prg_exec_monitor.dylib 528K ./libboost_date_time.a
648K ./libboost_graph.dylib
828K ./libboost_locale.dylib
```

11.
```sh
 $ find . type -f -exec du -h {} +|sort -rh | head -n 10  # mon10 самых "тяжёлых"
./libboost_log-vc141-mt-gd-x32-1_70.lib
./libboost_log-vc141-mt-gd-x64-1_70.lib
./libboost_log_setup-vc141-mt-gd-x32-1_70.lib
./libboost_log_setup-vc141-mt-gd-x64-1_70.lib
./libboost_regex-vc141-mt-gd-x64-1_70.lib
./libboost_test_exec_monitor-vc141-mt-gd-x32-1_70.lib
./libboost_test_exec_monitor-vc141-mt-gd-x64-1_70.lib
./libboost_unit_test_framework-vc141-mt-gd-x64-1_70.lib
./libboost_wave-vc141-mt-gd-x32-1_70.lib
./libboost_wave-vc141-mt-gd-x64-1_70.lib
```
Copyright (c) 2015-2020 The ISC Authors
```
