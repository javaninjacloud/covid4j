# covid4j - Java API for pulling Covid-19 Stats

## Spring Boot REST Api for fetching Covid-19 Stats for country/state/city

Include the following maven dependency
```maven
<dependency>
    <groupId>io.javaninja.ajeet</groupId>
    <artifactId>covid4j</artifactId>
    <version>1.0.0</version>
</dependency>
```

### API's exposed:-
Get data by country
@GetMapping("/getCovidDataByCountry/{country}")

Get data by state or city
@GetMapping("/getCovidDataByCityOrState/{cityOrState}")

Params 'country' and 'cityOrState' are not case-sensitive.

### Sample response for country 'India'
```json
{
    "confirmed": "309K",
    "recovered": "154K",
    "deaths": "8,884",
    "confirmedNewCases": "+11,458",
    "confirmedNewDeaths": "+386",
    "lastUpdated": "Updated less than 1 hour ago"
}
```
