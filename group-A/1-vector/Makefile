## -----------------------------------------------------------------------------
## Created: Sun 26 Aug 2018 23:09:53 IST
## Last-Updated: Sun 26 Aug 2018 23:11:45 IST
##
## Makefile is part of be-comp-sem1
## URL: https://github.com/justinekizhak/be-comp-sem1
## Description: Makefile
##
## Copyright (c) 2018, Justine Kizhakkinedath
## All rights reserved
##
## Licensed under the terms of MIT License
## See LICENSE file in the project root for full information.
## -----------------------------------------------------------------------------

# project name (generate executable with this name)
TARGET   = 1-vector

CC       = clang++
# compiling flags here
CFLAGS=-I$(IDIR) -Wall -g -O3

LINKER   = clang++
# linking flags here
LFLAGS   = -Wall -I. -lm

# change these to proper directories where each file should be
SRCDIR   = src
OBJDIR   = obj
BINDIR   = bin
INCDIR   = inc
LIBDIR   = lib

SOURCES  := $(wildcard $(SRCDIR)/*.cpp)
INCLUDES := $(wildcard $(INCDIR)/*.h)
OBJECTS  := $(SOURCES:$(SRCDIR)/%.cpp=$(OBJDIR)/%.o)
rm       	= rm -f
MKDIR_P 	= mkdir -p

$(TARGET): $(OBJECTS)
		@$(LINKER) $(OBJECTS) $(LFLAGS) -o $(BINDIR)/$@
		@echo "Linking complete!"

$(OBJECTS): $(OBJDIR)/%.o : $(SRCDIR)/%.cpp directories
		@$(CC) $(CFLAGS) -c $< -o $@
		@echo "Compiled "$<" successfully!"

directories:
		@echo "Creating directories"
		@$(MKDIR_P) $(SRCDIR)
		@$(MKDIR_P) $(OBJDIR)
		@$(MKDIR_P) $(BINDIR)
		@$(MKDIR_P) $(INCDIR)
		@$(MKDIR_P) $(LIBDIR)

.PHONY: clean

clean:
	rm -f $(OBJDIR)/*.o
	rm -f $(BINDIR)/*
	@echo "Cleanup complete!"
