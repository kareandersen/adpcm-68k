TARGET = ADPCMCodec
OBJS = codec.o main.o

CXX = clang++
CXXFLAGS = -std=c++17 -Wall -Wextra
RELEASE_FLAGS = -O3 -DNDEBUG
DEBUG_FLAGS = -g -D_DEBUG

all: $(TARGET)

$(TARGET): $(OBJS)
	$(CXX) $(CXXFLAGS) $(RELEASE_FLAGS) -o $@ $(OBJS)

debug: $(OBJS)
	$(CXX) $(CXXFLAGS) $(DEBUG_FLAGS) -o $(TARGET)_debug $(OBJS)

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $< -o $@

clean:
	@rm -f $(TARGET) $(TARGET)_debug $(OBJS)

.PHONY: all debug clean

