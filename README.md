# Databases

## Overview

Our topic for this week is databases. We will practice the basic database
concepts discussed in lecture by writing a series of queries over a small
database.

If you did not bring a laptop today, please partner up with someone else. Make
sure both you and your partner's names are listed in the README.md.

**Please download** the [starter kit] for this activity. This will download a
file called `disc-week-10-datases-master.zip`. Unzip this directory somewhere in
your virtual machine. **Do NOT add the archive or its files to your
repository.**

[starter kit]: https://github.com/umass-cs-220/disc-week-10-databases/archive/master.zip

## Setup

**NOTE:** There is no programming for this assignment. Copy each query you write
into a file called `queries.txt`. This will be your deliverable for the
assignment, along with your README.

You will be using a small database of cars for the assignment. We've provided
the database as part of the starter kit linked above, so you can jump straight
to writing queries. The database contains two tables:

- CARS: Records the make, model and year of each car with a unique ID
- COLORS: Records the color options for each car, linked to the car's ID

1. Download and unzip the starter kit. You can do this directly inside the VM:

    ```
    wget https://github.com/umass-cs-220/disc-week-10-databases/archive/master.zip
    unzip master.zip
    ```
    This will create a directory called disc-week-10-databases-master.

1. Inside the unzipped directory, run the h2 script (`sh h2`) to start the
   database. You can connect to the database through your web browser at
   `localhost:4001`. You will have to create a second connection to your VM
   (e.g. creating another PuTTY instance or running vagrant ssh from another
   terminal) in order to interact with your VM.

1. In your repository, create a folder called **dis10**.

1. Create a **README.md** file that contains the following:

    CMPSCI 220 Programming Methodology  
    Discussion Week 10  
    Your Name  
    Your Spire ID  
    Your Partner's Name (if applicable)  
    Your Partner's Spire ID (if applicable)  
  
1. Create a file called `queries.txt`. Record the queries you create for Task 2
   in this file.

## Task

Write the following queries, test them in the web console, and record the query
(and ONLY the query) in queries.txt.

1. List every record in the CARS table

1. List only the make, model and year of every Toyota

1. List all cars that were released during or after 2010.

1. List all Hondas that have 'black' as a color option

1. List all of the distinct color options for Fords

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
