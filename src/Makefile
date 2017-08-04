btrack_src = BTrack.cpp OnsetDetectionFunction.cpp
btrack_obj = $(btrack_src:.cpp=.o)

KISSFFT ?= -DUSE_KISS_FFT -I../libs/kiss_fft130

libbtrack.a: $(btrack_obj)
	@$(AR) -cr libbtrack.a $^

%.o:%.cpp 
	$(CXX) $(CFLAGS) $(KISSFFT) -c -o $@ $<

.PHONY: clean
clean:
	$(RM) $(btrack_obj) libbtrack.a
