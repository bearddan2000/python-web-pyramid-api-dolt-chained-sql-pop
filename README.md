# python-web-pyramid-api-dolt-chained-sql-pop

## Description
Simple web app that serves an api
for a pyramid project.

Uses sqlalchemy chained functions to query a table `pop`.

Remotely tested with *testify*.

## Tech stack
- python
  - pyramid
  - sqlalchemy
  - testify
  - requests
- dolt

## Docker stack
- python:latest
- dolthub/dolt-sql-serverdb

## To run
`sudo ./install.sh -u`
- Get all pops: http://localhost/pop
  - Schema id, name, and color
- CRUD opperations
  - Create: curl -i -X PUT localhost/pop/<id>
  - Read: http://localhost/pop/<id>
  - Update: curl -i -X POST localhost/pop/<id>/<name>/<color>
  - Delete: curl -i -X DELETE localhost/pop/<id>

## To stop (optional)
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`

## Credit
- [Pyramid setup](https://docs.pylonsproject.org/projects/pyramid/en/latest/index.html)
- [Sqlalchemy setup](https://docs.pylonsproject.org/projects/pyramid-cookbook/en/latest/database/sqlalchemy.html)
- [Json setup](https://docs.pylonsproject.org/projects/pyramid/en/latest/narr/renderers.html)