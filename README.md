PROJECT {_id : 1, address : 1, borough : 1, cuisine : 1, grades: 1, name : 1, restaurant_id : 1}
PROJECT {restaurant_id:1, name:1, borough:1, cuisine:1}
PROJECT {_id:0,restaurant_id:1, name:1, borough:1, cuisine:1}
PROJECT {restaurant_id:1, name:1, borough:1, "address.zipcode":1, _id : 0}
FILTER {borough : "Bronx"}
FILTER {borough : "Bronx"} LIMIT 5
FILTER {borough : "Bronx"} SKIP 5 LIMIT 5
FILTER {"grades.score":{$gt : 90}}
FILTER {"grades.score":{$gt : 80, $lt : 100}}
FILTER {"address.coord":{$lt : -95.754168}}
FILTER {'grades.score': {$gt: 70},'address.coord': {$lt: -65.754168},cuisine: {$in: [ 'Pizza/Italian', 'Italian', 'Bakery', 'Latin (Cuban, Dominican, Puerto Rican, South & Central American)', 'Café/Coffee/Tea', 'Chinese', 'Pizza', 'Caribbean', 'Mediterranean', 'Spanish', 'Polish', 'Russian', 'Jewish/Kosher', 'Tex-Mex', 'Pancakes/Waffles', 'Vegetarian', 'Seafood', 'Delicatessen', 'Continental', 'Japanese', 'Hamburgers', 'Chicken', 'Vietnamese/Cambodian/Malaysia', 'Irish', 'French', 'Mexican', 'Ethiopian']}}
FILTER {'grades.score': {$gt: 70},'address.coord': {$lt: -65.754168},cuisine: {$in: [ 'Pizza/Italian', 'Italian', 'Bakery', 'Latin (Cuban, Dominican, Puerto Rican, South & Central American)', 'Café/Coffee/Tea', 'Chinese', 'Pizza', 'Caribbean', 'Mediterranean', 'Spanish', 'Polish', 'Russian', 'Jewish/Kosher', 'Tex-Mex', 'Pancakes/Waffles', 'Vegetarian', 'Seafood', 'Delicatessen', 'Continental', 'Japanese', 'Hamburgers', 'Chicken', 'Vietnamese/Cambodian/Malaysia', 'Irish', 'French', 'Mexican', 'Ethiopian']}}
FILTER {cuisine: {$in: [ 'Italian', 'Pizza', 'Latin (Cuban, Dominican, Puerto Rican, South & Central American)', 'Bakery', 'Café/Coffee/Tea', 'Pizza/Italian', 'Chinese', 'Hamburgers', 'Japanese', 'Irish', 'Sandwiches', 'Donuts', 'Delicatessen', 'Seafood', 'Vegetarian', 'Sandwiches/Salads/Mixed Buffet', 'Mexican', 'Mediterranean', 'Jewish/Kosher', 'Asian', 'Spanish', 'Greek', 'Continental', 'Caribbean', 'Chicken', 'German']},'grades.grade': 'A',borough: {$in: [ 'Manhattan', 'Queens', 'Bronx', 'Staten Island']}} SORT {name:-1}
FILTER { name: /^Wil/ } PROJECT {restaurant_id:1, name:1, borough:1, cuisine:1}
FILTER { name: /ces$/ } PROJECT {restaurant_id:1, name:1, borough:1, cuisine:1}
FILTER { name: /Reg/ } PROJECT {restaurant_id:1, name:1, borough:1, cuisine:1}
FILTER {borough: 'Bronx',cuisine: {$in: [ 'American ', 'Chinese']}}
FILTER {borough: {$in: [ 'Brooklyn', 'Queens', 'Bronx', 'Staten Island']}} PROJECT {restaurant_id:1, name:1, borough:1, cuisine:1}
PROJECT {restaurant_id:1, name:1, borough:1, cuisine:1}
