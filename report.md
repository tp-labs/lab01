1) Устанавливаем библиоткеку с помощью wget
 wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
2)Разархивируем скачанный файл
 tar -xvf boost_1_69_0.tar.gz
3)считаем количество файлов в директории не включая вложенные директории
find . -maxdepth 1 -type f | wc -l
18
4) Считаем количество файлов в директории, включая вложенные директории
 find . -type f|wc -l
68431
5) Посчитаем количество заголовочных файлов, файлов с расширением .cpp, сколько остальных
файлов (не заголовочных и не .cpp)
 find . -type f -name "*.hpp" -o -name "*.h" | wc -l
15208
 find . -type f -name "*.cpp" | wc -l
13774
find . -not -name "*.h" -not -name "*.hpp" -not -name "*.cpp" | wc -l
45474
 Найдем полный пусть до файла
find `pwd` -name any.hpp
/home/dmitrii/boost_1_69_0/boost/proto/detail/any.hpp
/home/dmitrii/boost_1_69_0/boost/hana/fwd/any.hpp
/home/dmitrii/boost_1_69_0/boost/hana/any.hpp
/home/dmitrii/boost_1_69_0/boost/xpressive/detail/utility/any.hpp
/home/dmitrii/boost_1_69_0/boost/fusion/algorithm/query/detail/any.hpp
/home/dmitrii/boost_1_69_0/boost/fusion/algorithm/query/any.hpp
/home/dmitrii/boost_1_69_0/boost/fusion/include/any.hpp
/home/dmitrii/boost_1_69_0/boost/any.hpp
/home/dmitrii/boost_1_69_0/boost/type_erasure/any.hpp
/home/dmitrii/boost_1_69_0/boost/spirit/home/support/algorithm/any.hpp
7) Отображаем в консоли все файлы, где упоминается последовательность boost::asio
grep -Ril "boost::asio"
8) Скомпилируем boost
sudo apt install libicu-dev
sudo apt install g++
cd boost_1_69_0/tools/build
sh bootstrap.sh
./b2 install —prefix=out
9) Переносим файлы с помощью mv
mv out boost-libs
10) Идем в библиотеку
cd
cd boost_1_69_0/tools/build/boost-libs
2 Вариант
Затем, смотрим вес файлов
find . -type f -exec du -h {} +

11) Находим 10 самых тяжелых файлов
find . -type f -exec du {} +|sort -rh | head -n 10
288 ./bin/bjam

288 ./bin/b2
84 ./share/boost-build/src/tools/msvc.jam
68 ./share/boost-build/src/build/targets.jam
64 ./share/boost-build/src/tools/msvc.py
64 ./share/boost-build/src/build/targets.py
60 ./share/boost-build/src/build/project.py
56 ./share/boost-build/src/tools/gcc.jam
48 ./share/boost-build/src/build/project.jam
48 ./share/boost-build/src/build/generators.py
