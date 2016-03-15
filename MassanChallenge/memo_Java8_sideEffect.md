
### したいこと
Java8っぽく簡潔に書きたい

### forEarchバージョン

* 副作用あり

```

private List<Integer> customerTypeList;

private List<Customer> createCustomerType(Long customerId) {

 List<Customer> customerList = new ArrayList<>();
 customerTypeList.forEarch( type -> {
   Customer customer = new  Customer();
   customer.setCustomerId(customerId);
   customer.setCustomerType(type);
   customerList.add(customer)
 });
 return customerList;
}

```

### stream使いバージョン

* 副作用なし

```

private List<Integer> customerTypeList;

private List<Customer> createCustomerType(Long customerId) {

 return  customerTypeList.stream.map( type -> {
   Customer customer = new  Customer();
   customer.setCustomerId(customerId);
   customer.setCustomerType(type);
   return customer;
 }).collect(Collectors.toList());
}

```
