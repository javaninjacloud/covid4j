# covid4j - Java API for pulling Covid-19 Stats

## Spring Boot REST Api for fetching Covid-19 Stats for country/state/city

Data is sourced from WHO and is regularly updated. More details available here:-
https://javaninja.io/spring-boot-rest-api-for-pulling-covid-19-stats/

Include the following maven dependency:-
```
<dependency>
    <groupId>io.javaninja.ajeet</groupId>
    <artifactId>covid4j</artifactId>
    <version>1.0.3</version>
</dependency>
```

### API's exposed:-
Get data by country:-
```java
@GetMapping("/getCovidDataByCountry/{country}")
    public CovidStats getCovidDataByCountry(@PathVariable String country) throws IOException {

        return CovidApi.getAllCovidStatsForCountry(country);
    }
```


Get data by state or city:-
```java
@GetMapping("/getCovidDataByCityOrState/{cityOrState}")
    public CovidStats getCovidDataByCityOrState(@PathVariable String cityOrState) throws IOException {

        return CovidApi.getAllCovidStatsForCityOrState(cityOrState);
    }
```

Params 'country' and 'cityOrState' are not case-sensitive.

### Sample response for country 'India'
```json
{
    "name": "india",
    "type": "country",
    "confirmed": "321K",
    "recovered": "162K",
    "deaths": "9,195",
    "confirmedNewCases": "+11,929",
    "confirmedNewDeaths": "+311",
    "lastUpdated": "Updated less than 20 mins ago"
}
```
