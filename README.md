(1) For the following question write the corresponding MongoDB queries
       (a)Find all the information about each products?
        ( Answer) db.users.find()
        (b)Find the product price which are between 400 to 800?
        (Answer) db.users.find({product_price:{$gte:400,$lte:800}})
        (c)Find the product price which are not between 400 to 600?
        (Answer) db.users.find({product_price:{$not:{$gte:400,$lte600}}})
        (d) List the four product which are greater than 500 in price ?
        (Answer) db.users.find({product_price:{$gt:500}}).limit(4)
        (e) Find the product name and product material of each products?
        (Answer) db.users.find({},(-id:0,product_name:1,product_material:1})
        (f) Find the product with a row id of 10?
        (Answer) db.users.find({id:”10”})
        (g) Find only the product name and product material?
        (Answer) db.users.find({id:0,product_name:1,product_material:1})
        (h) Find all products which contain the value of soft in product material 
        (Answer) db.users.find({product_material:”Soft”})
        (i) Find products which contain product color indigo  and product price 492.00?
        (Answer) db.users.find({product_color:”indigo”,product_price:492.00})
        Individually => db.users.find({ product_color: "indigo" }).pretty()
                               db.users.find({ product_price: 492.00 }).pretty()
        (j)Delete the products which product price value are 28?
        (Answer) db.users.deleteMany({product_price:28})

                                                Queries and Answer (_MONGOSH)
          
use Mongodb_task
switched to db Mongodb_task
db.users.find()
{
  _id: ObjectId('6682945770c7df9efc0804d2'),
  id: '1',
  product_name: 'Intelligent Fresh Chips',
  product_price: 655,
  product_material: 'Concrete',
  product_color: 'mint green'
}
{
  _id: ObjectId('6682945770c7df9efc0804d3'),
  id: '2',
  product_name: 'Practical Fresh Sausages',
  product_price: 911,
  product_material: 'Cotton',
  product_color: 'indigo'
}
{
  _id: ObjectId('6682945770c7df9efc0804d4'),
  id: '3',
  product_name: 'Refined Steel Car',
  product_price: 690,
  product_material: 'Rubber',
  product_color: 'gold'
}
{
  _id: ObjectId('6682945770c7df9efc0804d5'),
  id: '4',
  product_name: 'Gorgeous Plastic Pants',
  product_price: 492,
  product_material: 'Soft',
  product_color: 'plum'
}
{
  _id: ObjectId('6682945770c7df9efc0804d6'),
  id: '5',
  product_name: 'Sleek Cotton Chair',
  product_price: 33,
  product_material: 'Fresh',
  product_color: 'black'
}
{
  _id: ObjectId('6682945770c7df9efc0804d7'),
  id: '6',
  product_name: 'Awesome Wooden Towels',
  product_price: 474,
  product_material: 'Plastic',
  product_color: 'orange'
}
{
  _id: ObjectId('6682945770c7df9efc0804d8'),
  id: '7',
  product_name: 'Practical Soft Shoes',
  product_price: 500,
  product_material: 'Rubber',
  product_color: 'pink'
}
{
  _id: ObjectId('6682945770c7df9efc0804d9'),
  id: '8',
  product_name: 'Incredible Steel Hat',
  product_price: 78,
  product_material: 'Rubber',
  product_color: 'violet'
}
{
  _id: ObjectId('6682945770c7df9efc0804da'),
  id: '9',
  product_name: 'Awesome Wooden Ball',
  product_price: 28,
  product_material: 'Soft',
  product_color: 'azure'
}
{
  _id: ObjectId('6682945770c7df9efc0804db'),
  id: '10',
  product_name: 'Generic Wooden Pizza',
  product_price: 84,
  product_material: 'Frozen',
  product_color: 'indigo'
}
{
  _id: ObjectId('6682945770c7df9efc0804dc'),
  id: '11',
  product_name: 'Unbranded Wooden Cheese',
  product_price: 26,
  product_material: 'Soft',
  product_color: 'black'
}
{
  _id: ObjectId('6682945770c7df9efc0804dd'),
  id: '12',
  product_name: 'Unbranded Plastic Salad',
  product_price: 89,
  product_material: 'Wooden',
  product_color: 'pink'
}
{
  _id: ObjectId('6682945770c7df9efc0804de'),
  id: '13',
  product_name: 'Gorgeous Cotton Keyboard',
  product_price: 37,
  product_material: 'Concrete',
  product_color: 'sky blue'
}
{
  _id: ObjectId('6682945770c7df9efc0804df'),
  id: '14',
  product_name: 'Incredible Steel Shirt',
  product_price: 54,
  product_material: 'Metal',
  product_color: 'white'
}
{
  _id: ObjectId('6682945770c7df9efc0804e0'),
  id: '15',
  product_name: 'Ergonomic Cotton Hat',
  product_price: 43,
  product_material: 'Rubber',
  product_color: 'mint green'
}
{
  _id: ObjectId('6682945770c7df9efc0804e1'),
  id: '16',
  product_name: 'Small Soft Chair',
  product_price: 47,
  product_material: 'Cotton',
  product_color: 'teal'
}
{
  _id: ObjectId('6682945770c7df9efc0804e2'),
  id: '17',
  product_name: 'Incredible Metal Car',
  product_price: 36,
  product_material: 'Fresh',
  product_color: 'indigo'
}
{
  _id: ObjectId('6682945770c7df9efc0804e3'),
  id: '18',
  product_name: 'Licensed Plastic Bacon',
  product_price: 88,
  product_material: 'Steel',
  product_color: 'yellow'
}
{
  _id: ObjectId('6682945770c7df9efc0804e4'),
  id: '19',
  product_name: 'Intelligent Cotton Chips',
  product_price: 46,
  product_material: 'Soft',
  product_color: 'azure'
}
{
  _id: ObjectId('6682945770c7df9efc0804e5'),
  id: '20',
  product_name: 'Handcrafted Wooden Bacon',
  product_price: 36,
  product_material: 'Concrete',
  product_color: 'lime'
}
Type "it" for more
db.users.find({product_price:{$gte:400,$lte:800}})
{
  _id: ObjectId('6682945770c7df9efc0804d2'),
  id: '1',
  product_name: 'Intelligent Fresh Chips',
  product_price: 655,
  product_material: 'Concrete',
  product_color: 'mint green'
}
{
  _id: ObjectId('6682945770c7df9efc0804d4'),
  id: '3',
  product_name: 'Refined Steel Car',
  product_price: 690,
  product_material: 'Rubber',
  product_color: 'gold'
}
{
  _id: ObjectId('6682945770c7df9efc0804d5'),
  id: '4',
  product_name: 'Gorgeous Plastic Pants',
  product_price: 492,
  product_material: 'Soft',
  product_color: 'plum'
}
{
  _id: ObjectId('6682945770c7df9efc0804d7'),
  id: '6',
  product_name: 'Awesome Wooden Towels',
  product_price: 474,
  product_material: 'Plastic',
  product_color: 'orange'
}
{
  _id: ObjectId('6682945770c7df9efc0804d8'),
  id: '7',
  product_name: 'Practical Soft Shoes',
  product_price: 500,
  product_material: 'Rubber',
  product_color: 'pink'
}
db.users.find({product_price:{$not:{$gte:400,$lte:600}}})
{
  _id: ObjectId('6682945770c7df9efc0804d2'),
  id: '1',
  product_name: 'Intelligent Fresh Chips',
  product_price: 655,
  product_material: 'Concrete',
  product_color: 'mint green'
}
{
  _id: ObjectId('6682945770c7df9efc0804d3'),
  id: '2',
  product_name: 'Practical Fresh Sausages',
  product_price: 911,
  product_material: 'Cotton',
  product_color: 'indigo'
}
{
  _id: ObjectId('6682945770c7df9efc0804d4'),
  id: '3',
  product_name: 'Refined Steel Car',
  product_price: 690,
  product_material: 'Rubber',
  product_color: 'gold'
}
{
  _id: ObjectId('6682945770c7df9efc0804d6'),
  id: '5',
  product_name: 'Sleek Cotton Chair',
  product_price: 33,
  product_material: 'Fresh',
  product_color: 'black'
}
{
  _id: ObjectId('6682945770c7df9efc0804d9'),
  id: '8',
  product_name: 'Incredible Steel Hat',
  product_price: 78,
  product_material: 'Rubber',
  product_color: 'violet'
}
{
  _id: ObjectId('6682945770c7df9efc0804da'),
  id: '9',
  product_name: 'Awesome Wooden Ball',
  product_price: 28,
  product_material: 'Soft',
  product_color: 'azure'
}
{
  _id: ObjectId('6682945770c7df9efc0804db'),
  id: '10',
  product_name: 'Generic Wooden Pizza',
  product_price: 84,
  product_material: 'Frozen',
  product_color: 'indigo'
}
{
  _id: ObjectId('6682945770c7df9efc0804dc'),
  id: '11',
  product_name: 'Unbranded Wooden Cheese',
  product_price: 26,
  product_material: 'Soft',
  product_color: 'black'
}
{
  _id: ObjectId('6682945770c7df9efc0804dd'),
  id: '12',
  product_name: 'Unbranded Plastic Salad',
  product_price: 89,
  product_material: 'Wooden',
  product_color: 'pink'
}
{
  _id: ObjectId('6682945770c7df9efc0804de'),
  id: '13',
  product_name: 'Gorgeous Cotton Keyboard',
  product_price: 37,
  product_material: 'Concrete',
  product_color: 'sky blue'
}
{
  _id: ObjectId('6682945770c7df9efc0804df'),
  id: '14',
  product_name: 'Incredible Steel Shirt',
  product_price: 54,
  product_material: 'Metal',
  product_color: 'white'
}
{
  _id: ObjectId('6682945770c7df9efc0804e0'),
  id: '15',
  product_name: 'Ergonomic Cotton Hat',
  product_price: 43,
  product_material: 'Rubber',
  product_color: 'mint green'
}
{
  _id: ObjectId('6682945770c7df9efc0804e1'),
  id: '16',
  product_name: 'Small Soft Chair',
  product_price: 47,
  product_material: 'Cotton',
  product_color: 'teal'
}
{
  _id: ObjectId('6682945770c7df9efc0804e2'),
  id: '17',
  product_name: 'Incredible Metal Car',
  product_price: 36,
  product_material: 'Fresh',
  product_color: 'indigo'
}
{
  _id: ObjectId('6682945770c7df9efc0804e3'),
  id: '18',
  product_name: 'Licensed Plastic Bacon',
  product_price: 88,
  product_material: 'Steel',
  product_color: 'yellow'
}
{
  _id: ObjectId('6682945770c7df9efc0804e4'),
  id: '19',
  product_name: 'Intelligent Cotton Chips',
  product_price: 46,
  product_material: 'Soft',
  product_color: 'azure'
}
{
  _id: ObjectId('6682945770c7df9efc0804e5'),
  id: '20',
  product_name: 'Handcrafted Wooden Bacon',
  product_price: 36,
  product_material: 'Concrete',
  product_color: 'lime'
}
{
  _id: ObjectId('6682945770c7df9efc0804e6'),
  id: '21',
  product_name: 'Unbranded Granite Chicken',
  product_price: 90,
  product_material: 'Metal',
  product_color: 'gold'
}
{
  _id: ObjectId('6682945770c7df9efc0804e7'),
  id: '22',
  product_name: 'Ergonomic Soft Hat',
  product_price: 99,
  product_material: 'Rubber',
  product_color: 'black'
}
{
  _id: ObjectId('6682945770c7df9efc0804e8'),
  id: '23',
  product_name: 'Intelligent Steel Pizza',
  product_price: 95,
  product_material: 'Cotton',
  product_color: 'azure'
}
Type "it" for more
db.users.find({product_price:{$gt:500}}).limit(4)
{
  _id: ObjectId('6682945770c7df9efc0804d2'),
  id: '1',
  product_name: 'Intelligent Fresh Chips',
  product_price: 655,
  product_material: 'Concrete',
  product_color: 'mint green'
}
{
  _id: ObjectId('6682945770c7df9efc0804d3'),
  id: '2',
  product_name: 'Practical Fresh Sausages',
  product_price: 911,
  product_material: 'Cotton',
  product_color: 'indigo'
}
{
  _id: ObjectId('6682945770c7df9efc0804d4'),
  id: '3',
  product_name: 'Refined Steel Car',
  product_price: 690,
  product_material: 'Rubber',
  product_color: 'gold'
}
db.users.find({},{_id:0,product_name:1,product_material:1})
{
  product_name: 'Intelligent Fresh Chips',
  product_material: 'Concrete'
}
{
  product_name: 'Practical Fresh Sausages',
  product_material: 'Cotton'
}
{
  product_name: 'Refined Steel Car',
  product_material: 'Rubber'
}
{
  product_name: 'Gorgeous Plastic Pants',
  product_material: 'Soft'
}
{
  product_name: 'Sleek Cotton Chair',
  product_material: 'Fresh'
}
{
  product_name: 'Awesome Wooden Towels',
  product_material: 'Plastic'
}
{
  product_name: 'Practical Soft Shoes',
  product_material: 'Rubber'
}
{
  product_name: 'Incredible Steel Hat',
  product_material: 'Rubber'
}
{
  product_name: 'Awesome Wooden Ball',
  product_material: 'Soft'
}
{
  product_name: 'Generic Wooden Pizza',
  product_material: 'Frozen'
}
{
  product_name: 'Unbranded Wooden Cheese',
  product_material: 'Soft'
}
{
  product_name: 'Unbranded Plastic Salad',
  product_material: 'Wooden'
}
{
  product_name: 'Gorgeous Cotton Keyboard',
  product_material: 'Concrete'
}
{
  product_name: 'Incredible Steel Shirt',
  product_material: 'Metal'
}
{
  product_name: 'Ergonomic Cotton Hat',
  product_material: 'Rubber'
}
{
  product_name: 'Small Soft Chair',
  product_material: 'Cotton'
}
{
  product_name: 'Incredible Metal Car',
  product_material: 'Fresh'
}
{
  product_name: 'Licensed Plastic Bacon',
  product_material: 'Steel'
}
{
  product_name: 'Intelligent Cotton Chips',
  product_material: 'Soft'
}
{
  product_name: 'Handcrafted Wooden Bacon',
  product_material: 'Concrete'
}
Type "it" for more
db.users.find({id:"10"})
{
  _id: ObjectId('6682945770c7df9efc0804db'),
  id: '10',
  product_name: 'Generic Wooden Pizza',
  product_price: 84,
  product_material: 'Frozen',
  product_color: 'indigo'
}
Type "it" for more
db.users.find({}, { _id: 0, product_name: 1, product_material: 1 }).pretty()
{
  product_name: 'Intelligent Fresh Chips',
  product_material: 'Concrete'
}
{
  product_name: 'Practical Fresh Sausages',
  product_material: 'Cotton'
}
{
  product_name: 'Refined Steel Car',
  product_material: 'Rubber'
}
{
  product_name: 'Gorgeous Plastic Pants',
  product_material: 'Soft'
}
{
  product_name: 'Sleek Cotton Chair',
  product_material: 'Fresh'
}
{
  product_name: 'Awesome Wooden Towels',
  product_material: 'Plastic'
}
{
  product_name: 'Practical Soft Shoes',
  product_material: 'Rubber'
}
{
  product_name: 'Incredible Steel Hat',
  product_material: 'Rubber'
}
{
  product_name: 'Awesome Wooden Ball',
  product_material: 'Soft'
}
{
  product_name: 'Generic Wooden Pizza',
  product_material: 'Frozen'
}
{
  product_name: 'Unbranded Wooden Cheese',
  product_material: 'Soft'
}
{
  product_name: 'Unbranded Plastic Salad',
  product_material: 'Wooden'
}
{
  product_name: 'Gorgeous Cotton Keyboard',
  product_material: 'Concrete'
}
{
  product_name: 'Incredible Steel Shirt',
  product_material: 'Metal'
}
{
  product_name: 'Ergonomic Cotton Hat',
  product_material: 'Rubber'
}
{
  product_name: 'Small Soft Chair',
  product_material: 'Cotton'
}
{
  product_name: 'Incredible Metal Car',
  product_material: 'Fresh'
}
{
  product_name: 'Licensed Plastic Bacon',
  product_material: 'Steel'
}
{
  product_name: 'Intelligent Cotton Chips',
  product_material: 'Soft'
}
{
  product_name: 'Handcrafted Wooden Bacon',
  product_material: 'Concrete'
}
Type "it" for more
db.users.find({},{product_material:"Soft"})
{
  _id: ObjectId('6682945770c7df9efc0804d2'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804d3'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804d4'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804d5'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804d6'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804d7'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804d8'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804d9'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804da'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804db'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804dc'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804dd'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804de'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804df'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804e0'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804e1'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804e2'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804e3'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804e4'),
  product_material: 'Soft'
}
{
  _id: ObjectId('6682945770c7df9efc0804e5'),
  product_material: 'Soft'
}
Type "it" for more
db.users.find({ product_color: "indigo" }).pretty()
{
  _id: ObjectId('6682945770c7df9efc0804d3'),
  id: '2',
  product_name: 'Practical Fresh Sausages',
  product_price: 911,
  product_material: 'Cotton',
  product_color: 'indigo'
}
{
  _id: ObjectId('6682945770c7df9efc0804db'),
  id: '10',
  product_name: 'Generic Wooden Pizza',
  product_price: 84,
  product_material: 'Frozen',
  product_color: 'indigo'
}
{
  _id: ObjectId('6682945770c7df9efc0804e2'),
  id: '17',
  product_name: 'Incredible Metal Car',
  product_price: 36,
  product_material: 'Fresh',
  product_color: 'indigo'
}
{
  _id: ObjectId('6682945770c7df9efc0804ea'),
  id: '25',
  product_name: 'Licensed Steel Car',
  product_price: 20,
  product_material: 'Cotton',
  product_color: 'indigo'
}
db.users.find({ product_price: 492.00 }).pretty()
{
  _id: ObjectId('6682945770c7df9efc0804d5'),
  id: '4',
  product_name: 'Gorgeous Plastic Pants',
  product_price: 492,
  product_material: 'Soft',
  product_color: 'plum'
}
db.users.find({
    product_color: "indigo",
    product_price: 492.00
}).pretty()
db.users.find({product_price:28})
{
  _id: ObjectId('6682945770c7df9efc0804da'),
  id: '9',
  product_name: 'Awesome Wooden Ball',
  product_price: 28,
  product_material: 'Soft',
  product_color: 'azure'
}
db.users.deleteMany({product_price:28})
{
  acknowledged: true,
  deletedCount: 1
}
db.users.find({product_price:28})
Mongodb_task



