# Getting Started

[![CircleCI](https://circleci.com/gh/ahmednafies/covid.svg?style=shield)](https://circleci.com/gh/ahmednafies/covid) [![codecov](https://codecov.io/gh/ahmednafies/covid/branch/master/graph/badge.svg)](https://codecov.io/gh/ahmednafies/covid)

Python SDK to get information regarding the novel corona virus provided
by Johns Hopkins university and worldometers.info

![corona.jpeg](img/corona.jpeg)

Full code on [github](https://github.com/ahmednafies/covid)

## Requirements

    python >= 3.6

## How to install

    pip install covid

## Dependencies

    pydantic
    requests

## How to use

    from covid import Covid

    covid = Covid()
    covid.get_data()
