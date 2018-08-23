[ Complicate URL mapping example](https://www.baeldung.com/spring-requestmapping)

```
@RequestMapping(value = "/ex/foos", method = RequestMethod.GET)
@RequestMapping(value = "/ex/foos", headers = "key=val", method = GET)
@RequestMapping(value = "/ex/foos", headers = { "key1=val1", "key2=val2" }, method = GET)
@RequestMapping(value = "/ex/foos", method = GET, headers = "Accept=application/json")
@RequestMapping( value = "/ex/foos", method = RequestMethod.GET, produces = "application/json")
@RequestMapping(value = "/ex/foos", method = GET,produces = { "application/json", "application/xml" })


   https://www.baeldung.com/spring-requestmapping
@RequestMapping(value = "/ex/foos/{id}", method = GET)
@ResponseBody
public String getFoosBySimplePathWithPathVariable(
  @PathVariable("id") long id) {
    return "Get a specific Foo with id=" + id;
}


@RequestMapping(value = "/ex/foos/{fooid}/bar/{barid}", method = GET)
@ResponseBody
public String getFoosBySimplePathWithPathVariables
  (@PathVariable long fooid, @PathVariable long barid) {
    return "Get a specific Bar with id=" + barid + 
      " from a Foo with id=" + fooid;
}

@RequestMapping(value = "/ex/bars/{numericId:[\\d]+}", method = GET)
@ResponseBody
public String getBarsBySimplePathWithPathVariable(
  @PathVariable long numericId) {
    return "Get a specific Bar with id=" + numericId;
}

```
