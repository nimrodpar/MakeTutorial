# coveres up to https://makefiletutorial.com/#targets (including)

all: gah blah fs  # make always runs the firs rule it finds. this allows us to control what gets run

gah:
        echo "Gah"

blah: blah.c
        cc blah.c -o blah

files := f1.o f2.o  # variable

fs: ${files}
        echo "fs $?"  # $? is the dependency, so it will be 'f1.o' and then 'f2.o'


f1.o f2.o:
        echo "f1.o f2.o $@" # $? is the target

# the 'f1.o f2.o' rule is equivalent to:
#
# f1.o:
#        echo f1.o
# f2.o:
#        echo f2.o
