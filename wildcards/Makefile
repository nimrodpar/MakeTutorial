# https://makefiletutorial.com/#-wildcard

wrong := *.o # Don't do this! '*' will not get expanded
right := $(wildcard *.o)

all: one two three four

# Fails, because $(thing_wrong) is the string "*.o"
one: $(wrong)
        echo "in one, dep is '$?'"

# Stays as *.o if there are no files that match this pattern :(
two: *.o
        echo "in two, dep is '$?'"

# Works as you would expect! In this case, it does nothing.
three: $(right)
        echo "in three, dep is '$?'"

# Same as rule three
four: $(wildcard *.o)
