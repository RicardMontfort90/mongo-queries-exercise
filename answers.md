# Solutions sheet

Submit your final query after each iteration:

## Iteration 1:  Write a query that finds all the users in the collection but returns only their names.

db.users.find({}, {name: 1})

## Iteration 2:  Write a query that finds all the users that currently have insurance.

db.users.find({hasInsurance: {$eq:true}})

## Iteration 3: Write a query that return all users that are 18 years old or older.

db.users.find({age: {$gte: 18}})

## Iteration 4:  Write a query that returns the first user living in Italy. Return only their name and email.



## Iteration 5: Write a query that returns users living in the USA. Limit the data to 5 users. Return only their names.

db.users.find({ country: {eq:"USA"}}, {name: 1, _id:0}).limit(5).sort({})

## Iteration 6: Write a query that returns those users of whom we have the phone number.

db.users.find({ phone: {exist:true}})

## Iteration 7: Write a query that updates the information of Marissa Geller: her new mail account is "marissa@hotmail.com".



## Iteration 8: Write a query that updates the information of everyone living in the UK. Add to their documents a new field called currency and pass 'pounds' as a value.



## Iteration 9: Write a query that returns all the users living in the UK. Return only their names and currency.



## Iteration 10: Write a query that deletes all users that are older that are 45 or older.

