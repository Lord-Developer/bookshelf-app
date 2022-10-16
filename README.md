# bookshelf-app

Sign Up
POST https://go-bookshelf-app.herokuapp.com/signup

{
    "name": "Nodir",
    "key": "Lord",
    "secret": "King"
}



!!! Headerda key va signni berish shart aks holda ma'lumot qaytarmaydi chunki user authenticate qiladi berilgan ma'lumot orqali!

My Self
GET https://go-bookshelf-app.herokuapp.com/myself/{id}
Header:
    key: Lord,
    sign: King
    
    
    
Create Book
POST https://go-bookshelf-app.herokuapp.com/books
Header:
    key: Lord,
    sign: King

{
     "isbn": "787777123656",
     "title": "Windy Days",
     "author": "Lee Chan",
     "published": 2022,
     "pages": 120,
     "status": 3
}



Get Books List
GET http://localhost:8080/books
Header:
    key: Lord,
    sign: King
   
    
    
Update Boook Status OR Edit Book Properties 
PATCH https://go-bookshelf-app.herokuapp.com/books/{id}
Header:
    key: Lord,
    sign: King
{
    ... boshqa property larni kam kiritsa bo'ladi.
    "status": 1
} 



Get Book By ISBN
GET https://go-bookshelf-app.herokuapp.com/books/{isbn}
Header:
    key: Lord,
    sign: King



Get Book By ID
GET https://go-bookshelf-app.herokuapp.com/book_by_id/{id}
Header:
    key: Lord,
    sign: King


Delete Book By ID
DELETE https://go-bookshelf-app.herokuapp.com/books/{id}
Header:
    key: Lord,
    sign: King
    
    
