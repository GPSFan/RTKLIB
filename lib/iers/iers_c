#-------------------------------------------------
#
# Project created by QtCreator 2016-02-09T08:58:44
#
#-------------------------------------------------

QT       -= core gui

TARGET = iers
TEMPLATE = lib

include(../../RTKLib.pri)

*g++* {
QMAKE_FLAGS += -O3 -ffixed-line-length-132
}

win* {
CONFIG += staticlib
}

CONFIG += staticlib


SOURCES += src_c/cal2jd.c\
	   src_c/dat.c \
	   src_c/dehanttideinel.c \
	   src_c/gmf.c \
	   src_c/gpt.c \
	   src_c/norm8.c \ 
	   src_c/sprod.c \
	   src_c/st1idiu.c \
           src_c/st1isem.c \
	   src_c/st1l1.c \
	   src_c/step2diu.c \
	   src_c/step2lon.c \
	   src_c/vmf1.c \
	   src_c/vmf1_ht.c \
	   src_c/zero_vec8.c

DESTDIR = ..
