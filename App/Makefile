CC = gcc
CFLAGS = -O1 -Wall -Wno-missing-braces
LINKFLAGS = -lraylib -lopengl32 -lgdi32 -lwinmm

CFILES = src/main.c
LINKPATH = src/libraries/link

OUTPUTDIR = windows_build
APPLICATIONNAME = app.exe

all: $(CFILES)
	mkdir $(OUTPUTDIR)
	$(CC) $(CFILES) -o $(OUTPUTDIR)/$(APPLICATIONNAME) $(CFLAGS) -L $(LINKPATH) $(LINKFLAGS)
	@echo created executable file in $(OUTPUTDIR)/$(APPLICATIONNAME)
	@echo launching app
	.\$(OUTPUTDIR)\$(APPLICATIONNAME)

clean:
	del $(OUTPUTDIR)\$(APPLICATIONNAME) 
	rmdir $(OUTPUTDIR)

build: $(CFILES)
	@mkdir $(OUTPUTDIR)
	$(CC) $(CFILES) -o $(OUTPUTDIR)/$(APPLICATIONNAME) $(CFLAGS) -L $(LINKPATH) $(LINKFLAGS)
	@echo created executable file in $(OUTPUTDIR)/$(APPLICATIONNAME)
