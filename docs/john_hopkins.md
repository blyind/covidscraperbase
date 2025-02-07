by default `Covid` uses John Hopkins univeristy API as default
so you can use:

    covid = Covid(source="john_hopkins")

or

    covid = Covid()

### Get All Data

    from covid import Covid

    covid = Covid()
    covid.get_data()

result

    [
        {
            'id': '53',
            'country': 'China',
            'confirmed': 81020,
            'active': 9960,
            'deaths': 3217,
            'recovered': 67843,
            'latitude': 30.5928,
            'longitude': 114.3055,
            'last_update': 1584097775000
        },
        {
            'id': '115',
            'country': 'Italy',
            'confirmed': 24747,
            'active': 20603,
            'deaths': 1809,
            'recovered': 2335,
            'latitude': 41.8719,
            'longitude': 12.5674,
            'last_update': 1584318130000
        },
        ...

### List Countries

This comes in handy when you need to know the available names of countries
when using `get_status_by_country_name`, eg. "The Republic of Moldova" or just "Moldova"
So use this when you need to know the country exact name that you can use.

    countries = covid.list_countries()

result

    [
        {'id': '53', 'country': 'China'},
        {'id': '115', 'country': 'Italy'}
        ...
    ]

### Get Status By Country ID

    italy_cases = covid.get_status_by_country_id(115)

result

    {
        'id': '115',
        'country': 'Italy',
        'confirmed': 24747,
        'active': 20603,
        'deaths': 1809,
        'recovered': 2335,
        'latitude': 41.8719,
        'longitude': 12.5674,
        'last_update': 1584318130000
    }

### Get Status By Country Name

    italy_cases = covid.get_status_by_country_name("italy")

result

    {
        'id': '115',
        'country': 'Italy',
        'confirmed': 24747,
        'active': 20603,
        'deaths': 1809,
        'recovered': 2335,
        'latitude': 41.8719,
        'longitude': 12.5674,
        'last_update': 1584318130000
    }

### Get Total Active cases

    active = covid.get_total_active_cases()

### Get Total Confirmed cases

    confirmed = covid.get_total_confirmed_cases()

### Get Total Recovered cases

    recovered = covid.get_total_recovered()

### Get Total Deaths

    deaths = covid.get_total_deaths()
