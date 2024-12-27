MODNAME=mod_openai_asr.so
CFLAGS=-fPIC -O2 $(shell pkg-config --cflags freeswitch) $(shell pkg-config --cflags libcurl)
LDFLAGS=$(shell pkg-config --libs freeswitch) $(shell pkg-config --libs libcurl)

$(MODNAME): ../sources/mod_openai_asr.c ../sources/utils.c ../sources/curl.c
  gcc $(CFLAGS) -shared -o $(MODNAME) $^ $(LDFLAGS)
