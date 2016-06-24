
XX=g++

OPENCV = `pkg-config --cflags --libs opencv`
# OPENCV = -I/usr/include/opencv -lopencv_calib3d -lopencv_contrib -lopencv_core -lopencv_features2d -lopencv_flann -lopencv_gpu -lopencv_highgui -lopencv_imgproc -lopencv_legacy -lopencv_ml -lopencv_objdetect -lopencv_ocl -lopencv_photo -lopencv_stitching -lopencv_superres -lopencv_ts -lopencv_video -lopencv_videostab
OPENCV_FLAGS = -lm `pkg-config --cflags opencv`
OPENCV_LIBS = -lm `pkg-config --libs opencv`
CXX_LIBS = -Wall -lm -pedantic $(OPENCV_LIBS)

SRCS = $(wildcard ./*.cpp)
OBJS = ${SRCS:.cpp=.o}
OUTPUT = "$(notdir $(PWD))"

all: $(OBJS)
	$(XX) $(OPENCV_FLAGS) $< $(CXX_LIBS) -o $(OUTPUT)
	@echo 'Done'

#Gerando objetos
.cpp.o:
	$(XX) -Wall -c $(CXX_FLAGS) $<

#Limpando os objetos
clean:
	rm -rf *.o *.elf *.hex *.map *.s *.list
