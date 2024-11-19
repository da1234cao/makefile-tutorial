SRC_FILES := $(wildcard *.c)

TARGET := target-example

$(TARGET): $(SRC_FILES)
	gcc -o $@ $^

.PHONY: all
all: $(TARGET)

.PHONY: clean
clean:
	rm -f $(TARGET)