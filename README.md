# Covid

[![CircleCI](https://circleci.com/gh/ahmednafies/covid.svg?style=shield)](https://circleci.com/gh/ahmednafies/covid) [![codecov](https://codecov.io/gh/ahmednafies/covid/branch/master/graph/badge.svg)](https://codecov.io/gh/ahmednafies/covid)

## Description

Python SDK to get information regarding the novel corona virus provided by Johns Hopkins university

Full Documentation can be found [here](https://ahmednafies.github.io/covid/)

## Requirements

    python >= 3.6

## How to install

    pip install covid

## Dependencies

    pydantic
    requests

## How to use

### Get All Data

    from covid import Covid

    covid = Covid()
    covid.get_data()

#### Result

    [
        {
            'country': 'Mainland China',
            'confirmed': 80756,
            'deaths': 3136,
            'recovered': 60096,
            'latitude': 30.5928,
            'longitude': 114.3055,
            'last_update': 1582264984000
        },
        {
            'country': 'Italy',
            'confirmed': 9172,
            'deaths': 463,
            'recovered': 724,
            'latitude': 43.0,
            'longitude': 12.0,
            'last_update': 1583777591000
        },
        ...

### List Countries

This comes in handy when you need to know the available names of countries
when using `get_status_by_country`, eg. "The Republic of Moldova" or just "Moldova"
So use this when you need to know the country exact name that you can use.

    countries = covid.list_countries()

#### Result

    [
        {'id': '40', 'country': 'China'},
        {'id': '93', 'country': 'Italy'}
        ...
    ]

### Get Status By Country ID

    italy_cases = covid.get_status_by_country_id(93)

#### Result

    {
        'country': 'Italy',
        'confirmed': 10000,
        'deaths': 0,
        'recovered': 1,
        'latitude': 63.0,
        'longitude': 16.0,
        'last_update': 1583893094000
    }

### Get Status By Country Name

    italy_cases = covid.get_status_by_country_name("italy")

#### Result

    {
        'country': 'Italy',
        'confirmed': 10000,
        'deaths': 0,
        'recovered': 1,
        'latitude': 63.0,
        'longitude': 16.0,
        'last_update': 1583893094000
    }

### Get Total Confirmed cases

    confirmed = covid.get_total_confirmed_cases()

### Get Total Recovered cases

    recovered = covid.get_total_recovered()

### Get Total Deaths

    deaths = covid.get_total_deaths()
