1)wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
2)tar -xvf boost_1_69_0.tar.gz
3)  find . -maxdepth 1 -type f | wc -l
18
4) $ find . -type f|wc -l
68431
5) $ find . -type f -name "*.hpp" -o -name "*.h" | wc -l
15208
 $ find . -type f -name "*.cpp" | wc -l
13774
 find . -not -name "*.h" -not -name "*.hpp" -not -name "*.cpp" | wc -l
45474
6) find `pwd` -name any.hpp
/home/user1/boost_1_69_0/boost/fusion/include/any.hpp
/home/user1/boost_1_69_0/boost/fusion/algorithm/query/detail/any.hpp
/home/user1/boost_1_69_0/boost/fusion/algorithm/query/any.hpp
/home/user1/boost_1_69_0/boost/proto/detail/any.hpp
/home/user1/boost_1_69_0/boost/spirit/home/support/algorithm/any.hpp
/home/user1/boost_1_69_0/boost/type_erasure/any.hpp
/home/user1/boost_1_69_0/boost/xpressive/detail/utility/any.hpp
/home/user1/boost_1_69_0/boost/any.hpp
/home/user1/boost_1_69_0/boost/hana/fwd/any.hpp
/home/user1/boost_1_69_0/boost/hana/any.hpp
7) grep -Ril "boost::asio"
8)sudo apt install libicu-dev
sudo apt install g++
cd boost_1_69_0/tools/build
sh bootstrap.sh
./b2 install --prefix=q
9)mv q boost-libs
10) cd
cd boost_1_69_0/tools/build/boost-libs


find . -type f -exec du -h {} +


11) find . -type f -exec du {} +|sort -rh | head -n 10
288     ./bin/bjam
288     ./bin/b2
80      ./share/boost-build/src/tools/msvc.jam
64      ./share/boost-build/src/build/targets.jam
60      ./share/boost-build/src/tools/msvc.py
60      ./share/boost-build/src/build/targets.py
56      ./share/boost-build/src/build/project.py
52      ./share/boost-build/src/tools/gcc.jam
48      ./share/boost-build/src/build/project.jam
48      ./share/boost-build/src/build/generators.py


