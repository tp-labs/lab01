1)$ wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
2)$ tar -xvf boost_1_69_0.tar.gz
3)find . -maxdepth 1 -type f | wc -l
18
4)$ find . -type f|wc -l
68431
5)$ find . -type f -name "*.hpp" -o -name "*.h" | wc -l
15208
 $ find . -type f -name "*.cpp" | wc -l
13774
 find . -not -name "*.h" -not -name "*.hpp" -not -name "*.cpp" | wc -l 
45474
6)find `pwd` -name any.hpp
/home/ubuntu/boost_1_69_0/boost/proto/detail/any.hpp
/home/ubuntu/boost_1_69_0/boost/hana/fwd/any.hpp
/home/ubuntu/boost_1_69_0/boost/hana/any.hpp
/home/ubuntu/boost_1_69_0/boost/xpressive/detail/utility/any.hpp
/home/ubuntu/boost_1_69_0/boost/any.hpp
/home/ubuntu/boost_1_69_0/boost/fusion/include/any.hpp
/home/ubuntu/boost_1_69_0/boost/fusion/algorithm/query/any.hpp
/home/ubuntu/boost_1_69_0/boost/fusion/algorithm/query/detail/any.hpp
/home/ubuntu/boost_1_69_0/boost/type_erasure/any.hpp
7) grep -Ril "boost::asio"
8) sudo apt install g++
./bootstrap.sh --prefix=boost_output
 bootstrap.sh
./b2 install
9) mv lib ~/boost-libs/
10)$ ls -la
11) ls -lSr
4860    ./libboost_wave.a
3992    ./libboost_math_tr1.a
3708    ./libboost_math_tr1l.a
3232    ./libboost_regex.a
3164    ./libboost_math_tr1f.a
2452    ./libboost_test_exec_monitor.a
2428    ./libboost_unit_test_framework.a
1748    ./libboost_program_options.a
