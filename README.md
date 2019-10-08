# MemoScope.Net [![Build](https://ci.appveyor.com/api/projects/status/rri98ga4qy0v4384?svg=true)](https://ci.appveyor.com/project/fremag/memoscope-net) [![Code Climate](https://codeclimate.com/github/fremag/MemoScope.Net/badges/gpa.svg)](https://codeclimate.com/github/fremag/MemoScope.Net) [![Issue Count](https://codeclimate.com/github/fremag/MemoScope.Net/badges/issue_count.svg)](https://codeclimate.com/github/fremag/MemoScope.Net)

![Memoscope.Net Logo](https://raw.githubusercontent.com/fremag/MemoScope.Net/master/MemoScope/Icons/Logos/memoscope_logo.png) | Dump and analyze .Net applications memory
---------------------|-------------------------------------------

# Wiki
Please, read the [wiki](https://github.com/fremag/MemoScope.Net/wiki) to know everything about MemoScope.
Lot of pictures, animated gifs and some text for every major features.

# TLDR
## What it MemoScope.Net ?
It's a tool to analyze .Net process memory: it can dump an application's memory in a file and read it later.
The dump file contains all data (objects) and threads (state, stack, call stack)

MemoScope.Net will analyze the data and help you to find **memory leaks** and **deadlocks**

Thanks to [Lee Culver](https://github.com/leculver) for his [ClrMd](https://github.com/Microsoft/clrmd) library, without it, MemoScope.Net would not exist.

## Install
Get binaries from AppVeyor: [x86](https://ci.appveyor.com/api/projects/fremag/memoscope-net/artifacts/MemoScope_x86_Release.zip?job=Configuration%3A%20Release%3B%20Platform%3A%20x86) [x64](https://ci.appveyor.com/api/projects/fremag/memoscope-net/artifacts/MemoScope_x64_Release.zip?job=Configuration%3A%20Release%3B%20Platform%3A%20x64)

# Use cases
## Out of Memory
I know, with 64 bits apps it should not be an issue but computers only have a few a few Go so it may still happen if your application :
- is using too much memory (peak)
- runs for days and has a "slow" memory leak

## Dead lock
If your application is locked and you want to know where and why: dump the memory, display the threads status and blocking objects to see what thread is holding one that is waited by another thread.

## Hard to reproduce bug
Sometimes, users can do weird things with your application and you can't make it happen on your computer so ask the user to dump its application's memory to analyze it on your machine.

# Features
 
## Heap statistics
![](Screenshots/memoscope_typestats.png "")

## Query instances
![](Screenshots/memoscope_instances_filter.png "")

## Instances content and references
![](Screenshots/memoscope_instance_details.png "")

## Compare dumps
![](Screenshots/memoscope_dumpdiff.png "")

## Threads, Stacks
![](Screenshots/memoscope_threads.png "")

## Deadlocks
![](Screenshots/memoscope_deadlocks.png "")

## Delegates
![](Screenshots/memoscope_delegates.png "")

## Dump process memory
![Dump Process Memory](Screenshots/memoscope_process_dump.png "Dump your process when conditions are satisified")

 
