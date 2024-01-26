# mongoDBOperators

$and => db.inventory.find( {
    $and: [
        { $or: [ { qty: { $lt : 10 } }, { qty : { $gt: 50 } } ] },
        { $or: [ { sale: true }, { price : { $lt : 5 } } ] }
    ]
} )
The query selects all documents where:
the qty field value is less than 10 or greater than 50, and
the sale field value is equal to true or the price field value is less than 5.

$in: db.inventory.find ( { quantity: { $in: [20, 50] } } )

$all: db.inventory.find( { tags: { $all: [ "appliance", "school", "book" ] } } )



$push is an update operator in MongoDB that adds the value in an array. In contrast, the $set operator is used to update the value of an existing field in the document.

remove removes a document from the collection. This is like an SQL DELETE.
$pull and $unset are update operations that change part of the document. They are similar to SQL UPDATE.
$pull removes an element from an array.
$unset removes the whole array (or any other field).

https://www.mongodb.com/docs/manual/reference/operator/projection/
