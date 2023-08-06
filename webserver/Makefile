#最省事版本，加入cpp文件也不用改源码
CXX = g++
TARGET = hello 
SRC = $(wildcard *.cpp)  # wildcard *.cpp : 自动收集所有.cpp文件
OBJ = $(patsubst %.cpp, %.o, $(SRC)) # 将所有.cpp文件替换成.o文件

CXXFLAGS = -c -Wall

$(TARGET): $(OBJ)
	$(CXX) -o $@ $^ -pthread

%.o: %.cpp
	$(CXX) $(CXXFLAGS) $< -o $@

.PHONY: clean
clean:
	rm -f *.o $(TARGET)
