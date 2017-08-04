kissfft_src = kiss_fft.c
kissfft_obj = $(kissfft_src:.c=.o)

libkissfft.a: $(kissfft_obj)
	@$(AR) -cr libkissfft.a $^

%.o : %.c 
	$(CC) $(CFLAGS) -c -o $@ $<

.PHONY: clean
clean:
	$(RM) -f $(kissfft_obj) libkissfft.a
