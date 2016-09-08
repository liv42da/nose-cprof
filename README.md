# nose-cprof

A plugin to use cProfile to profile
[nosetests](https://nose.readthedocs.io/en/latest/), rather than the built-in
Hotshot profiler.

Profiling tests can help track down sources of performance issues in code,
especially if a synthetic test can be created to focus on the area of concern.

The output generated by this plugin can easily be browsed using
[pstats\_viewer](https://github.com/msherry/pstats_viewer), or any other
pstats-compatible viewer.

## Getting started

### Prerequisites

This is a plugin for [nose](https://nose.readthedocs.io/en/latest/), so it's
useless without that installed.

### Installation

`pip install nose-cprof`

### Usage

This plugin adds some new options to `nosetests`:

```
--with-cprofile       Enable plugin cProfiler:  Use this plugin to run tests
                      using the cProfile profiler.  [NOSE_WITH_CPROFILE]
--cprofile-stats-file=FILE
                      Output file name; default "stats.dat"
--cprofile-stats-erase
                      Erase previously-collected profiling statistics before
                      run
```