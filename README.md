# Databases

## Overview

Our topic for this week is databases. We will practice the basic database
concepts discussed in lecture by writing a series of queries over a small
database.

If you did not bring a laptop today, please partner up with someone else. Make
sure both you and your partner's names are listed in the README.md:


Do not include any additional formatting.

**Please download** the [starter kit] for this activity. This will download a
file called `disc-week-10-datases-master.zip`. Unzip this directory somewhere in
your virtual machine. **Do NOT add the archive or its files to your
repository.**

[starter kit]: https://github.com/umass-cs-220/disc-week-10-databases/archive/master.zip

## Task

**NOTE:** There is no programming for this assignment. Copy each query you write
into a file called `queries.txt`. This will be your deliverable for the
assignment, along with your README.

You will be using a small database of cars for the assignment. We've provided
the database as part of the starter kit linked above, so you can jump straight
to writing queries.

Make | Model | Year | Color
--- | --- | --- | ---
Toyota | Corolla | 2008 | Black
Toyota | Camry | 2012 | Silver
Toyota | Camry | 2008 | Red
Honda | Civic | 2013 | White
Honda | Civic | 2010 | Black
Honda | Accord | 2012 | Silver
Ford | Focus | 2008 | White
Ford | Focus | 2010 | Red
Ford | Mustang | 2013 | Red

**You should be committing between steps in order to save your progress.**

1. In your repository, create a folder called **dis10**.

1. Create a **README.md** file that contains the lines:

    CMPSCI 220 Programming Methodology
    Discussion Week 10
    Your Name
    Your Spire ID
    Your Partner's Name (if applicable)
    Your Partner's Spire ID (if applicable)

1. Create a file called `queries.txt`.

1. Write the following queries:

    println("Finding all Toyotas:")
    prettyPrint(carFinder.find("Toyota"))

    println("Finding all Black Hondas:")
    prettyPrint(carFinder.find("Black", "Honda"))

    println("Removing all Hondas")
    carFinder.remove("Honda")

    println("Finding all cars from 2010:")
    prettyPrint(carFinder.find("2010"))

    println("Removing all Ford Focuses")
    carFinder.remove("Ford", "Focus")

    println("Finding all Fords:")
    prettyPrint(carFinder.find("Ford"))

## Deliverables

When you are finished, you should have the following in your dis10/ directory:

```
- README.md
- queries.txt
```

**The files in the starter kit must NOT be in your repository.**

## Submitting

You will not be submitting this assignment to Moodle. Instead, we will be using
*tagging*, just like the previous discussion section.

**You will be submitting this assignment at the end of the discussion section.
Do not worry if you do not have everything finished.**

1. Make sure everything is added, committed and pushed.

2. Create a tag: `git tag -a dis10 -m "dis10"`

3. Push the tag to the gitblit repository: `git push origin dis10`

We will use this tag when grading. Make sure that you create the tag right before your final push.

## Expected Output from Queries

```
Finding all Toyotas:
1. Toyota Camry 2008 Red
2. Toyota Camry 2012 Silver
3. Toyota Corolla 2008 Black

Finding all Black Hondas:
1. Honda Civic 2010 Black

Removing all Hondas

Finding all cars from 2010
1. Ford Focus 2010 Red

Removing all Ford Focuses

Finding all Fords:
1. Ford Mustang 2013 Red

End state:
1. Ford Mustang 2013 Red
2. Toyota Camry 2008 Red
3. Toyota Camry 2012 Silver
4. Toyota Corolla 2008 Black
```
