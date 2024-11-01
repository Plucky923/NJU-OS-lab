# 指定编译器
CC = gcc

# 指定编译选项
CFLAGS = -Wall -g

# 指定源文件和目标文件
SRC = pstree.c
OBJ = $(SRC:.c=.o)

# 目标可执行文件
TARGET = pstree

# 默认目标
all: $(TARGET)

# 生成目标可执行文件
$(TARGET): $(OBJ)
	$(CC) -o $@ $^

# 生成中间目标文件
%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

format:
	clang-format -i *.c

# 清理生成的文件
clean:
	rm -f $(OBJ) $(TARGET)

.PHONY: all clean
