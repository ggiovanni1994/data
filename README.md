# Data for [dev3map](https://dev3map.github.io/)

- `cities.json`: location and size of cities
- `claims.json`: boundary, name, shown color of nations
- `transit.json`: railway stations and connections ("edges")

Claim positions coordinates are in `z,x` order, because Leaflet uses the `lat,long` standard.

### Contributing
After adding/editing a claim, run

    ajv -s schemas/claims_schema.json -d claims.json --all-errors

to check if it's valid. You can install `ajv` through `npm` using

    npm install -g ajv-cli
