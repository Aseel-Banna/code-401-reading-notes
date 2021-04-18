# Spring RequestMapping

How to implement RequestMapping?
1. @RequestMapping — by Path
ex. @RequestMapping(value = "/ex/foos", method = RequestMethod.GET)
2. @RequestMapping — the HTTP Method
The HTTP method parameter has no default. So, if we don't specify a value, it's going to map to any HTTP request.
ex. @RequestMapping(value = "/ex/foos", method = POST)
3. @RequestMapping With the headers Attribute
ex. @RequestMapping(value = "/ex/foos", headers = "key=val", method = GET)
4. @RequestMapping Consumes and Produces
ex. @RequestMapping(
  value = "/ex/foos", 
  method = GET, 
  headers = "Accept=application/json")

RequestMapping With Path Variables:
1. Single @PathVariable
2. Multiple @PathVariable
3. @PathVariable With Regex


RequestMapping With Request Parameters
@RequestMapping can optionally define the parameters


RequestMapping Corner Cases
1. @RequestMapping — Multiple Paths Mapped to the Same Controller Method
2. @RequestMapping — Multiple HTTP Request Methods to the Same Controller Method
3. @RequestMapping — a Fallback for All Requests
4. Ambiguous Mapping Error

#### Spring Framework 4.3 introduced a few new HTTP mapping annotations, all based on @RequestMapping:

* @GetMapping
* @PostMapping
* @PutMapping
* @DeleteMapping
* @PatchMapping

## CrudRepository, JpaRepository, and PagingAndSortingRepository in Spring Data
JpaRepository extends PagingAndSortingRepository and, in turn, the CrudRepository.
JpaRepository contains the full API of CrudRepository and PagingAndSortingRepository.

CRUD functionality:

* save(…) – save an Iterable of entities. Here, we can pass multiple objects to save them in a batch
* findOne(…) – get a single entity based on passed primary key value
* findAll() – get an Iterable of all available entities in database
* count() – return the count of total entities in a table
* delete(…) – delete an entity based on the passed object
* exists(…) – verify if an entity exists based on the passed primary key value


