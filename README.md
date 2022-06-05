# grf-py
A Python framework for making NewGRFs for OpenTTD.

Goal is to combine the convenience and power of Python with control and performance of nfo.

Low-level API provides full coverage of the GRF format features, meaning it's possible to make any (modern) GRF with grf-py.

At this point it's mostly just a proof of concept, API, syntax and goals can be changed at any moment.

See https://github.com/citymania-org/cmclient/tree/master/grf/alpine/alpine.py for an example of grf made with this framework.

Out of GRF features it currently only supports objects. But most of actions are supported.

## grf.py

Idea is to provide two levels of api:

1) Low level (Action*) - directly mimic the grf capabilites with python syntax.
[Some documentation of the low-level API classes](docs/low_level.md).
2) High level - Something convenient to use but still interoperable with low-level api.

## grftopy 

GRF decompiler into a low-level grf.py api.

A tool to inspect the grf files. It's main goal is to provite a readable representation, not to be a fully functional decompiler. I.e. don't expect the generated py files to work and generate the grf back, even though it's not that hard to achieve it's not a priority atm.

Installation on linux with a clean virtualenv:
```
python3 -m venv grfenv
source grfenv/bin/activate
pip install --upgrade pip
pip install --upgrade setuptools
python setup.py install
```
