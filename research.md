---
layout: default
title:  Projects
order: 2
---

# Current projects

## Context-Guided Splitting
[Context-Guided Splitting](https://github.com/sophie-kaleba/truffleruby){:target="_blank" rel="noopener"} as part of TruffleRuby, a Ruby implementation on top of GraalVM.  
Context-Guided Splitting is a compiler optimisation aiming to improve memory usage and the time spent compiling at run time. This project is still under development, but is yielding
promising results on large Ruby programs.  

It is one of the main focuses of my PhD work.
Apart from a little tinkering of programs written in Ruby, this project is mainly developed in Java.

## Tooling to analyse program behaviour
I built a [Ruby call-site analyser](https://github.com/sophie-kaleba/ruby-cs-analyser){:target="_blank" rel="noopener"} from scratch to provide data about the run-time behaviour of a Ruby program, such as which methods are being executed and when they are cached.
It produces statistics and summary tables that can be used as a starting point to improve existing optimisations or develop new ones.  

I used this tool to guide the implementation of Context-Guided Splitting. It consists in an instrumented version of TruffleRuby, which provides execution traces that are then analysed by a tool developed in R, the statistics programming language.

# Past projects

## Fine-grained VM profiler
Squeak/Pharo, two Smalltalk implementations, use a sampling profiler to identify where most of the execution time is spent. It provides data detailing in which user and VM methods the time is spent.  

I improved this profiler using available debugging information; for the VM part, the improved profiler provides a detailed execution summary to the bytecode-level, instead of method-level. Such a tool
can further help language developers to identify performance bottlenecks in the VM codebase.
