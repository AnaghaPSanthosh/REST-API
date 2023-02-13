# AnakhasBookStore.BookApi

All URIs are relative to *https://bookstore.swagger.io/api/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addPet**](BookApi.md#addPet) | **POST** /book | Add a new book to the store
[**deletePet**](BookApi.md#deletePet) | **DELETE** /book/{bookId} | Deletes a book
[**findPetsByStatus**](BookApi.md#findPetsByStatus) | **GET** /book/find | Find book
[**getPetById**](BookApi.md#getPetById) | **GET** /book/{bookId} | Find book by ID
[**updatePet**](BookApi.md#updatePet) | **PUT** /book | Update details of existing book

<a name="addPet"></a>
# **addPet**
> Book addPet(body, ID, title, author, publisher, ISBN, pubdate, nopg, genre)

Add a new book to the store

Add a new book to the store

### Example
```javascript
import {AnakhasBookStore} from 'anakhas_book_store';

let apiInstance = new AnakhasBookStore.BookApi();
let body = new AnakhasBookStore.Book(); // Book | Create a new book in the store
let ID = 56; // Number | 
let title = "title_example"; // String | 
let author = "author_example"; // String | 
let publisher = "publisher_example"; // String | 
let ISBN = "ISBN_example"; // String | 
let pubdate = "pubdate_example"; // String | 
let nopg = 56; // Number | 
let genre = "genre_example"; // String | 

apiInstance.addPet(body, ID, title, author, publisher, ISBN, pubdate, nopg, genre, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Book**](Book.md)| Create a new book in the store | 
 **ID** | **Number**|  | 
 **title** | **String**|  | 
 **author** | **String**|  | 
 **publisher** | **String**|  | 
 **ISBN** | **String**|  | 
 **pubdate** | **String**|  | 
 **nopg** | **Number**|  | 
 **genre** | **String**|  | 

### Return type

[**Book**](Book.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

<a name="deletePet"></a>
# **deletePet**
> deletePet(bookId, opts)

Deletes a book

delete a book

### Example
```javascript
import {AnakhasBookStore} from 'anakhas_book_store';

let apiInstance = new AnakhasBookStore.BookApi();
let bookId = 789; // Number | book id to delete
let opts = { 
  'apiKey': "apiKey_example" // String | 
};
apiInstance.deletePet(bookId, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bookId** | **Number**| book id to delete | 
 **apiKey** | **String**|  | [optional] 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

<a name="findPetsByStatus"></a>
# **findPetsByStatus**
> [Book] findPetsByStatus(opts)

Find book

Multiple status values can be provided with comma separated strings

### Example
```javascript
import {AnakhasBookStore} from 'anakhas_book_store';

let apiInstance = new AnakhasBookStore.BookApi();
let opts = { 
  'status': "available" // String | Status values that need to be considered for filter
};
apiInstance.findPetsByStatus(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | **String**| Status values that need to be considered for filter | [optional] [default to available]

### Return type

[**[Book]**](Book.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

<a name="getPetById"></a>
# **getPetById**
> Book getPetById(bookId)

Find book by ID

Returns a single book

### Example
```javascript
import {AnakhasBookStore} from 'anakhas_book_store';

let apiInstance = new AnakhasBookStore.BookApi();
let bookId = 789; // Number | ID of book to return

apiInstance.getPetById(bookId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bookId** | **Number**| ID of book to return | 

### Return type

[**Book**](Book.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

<a name="updatePet"></a>
# **updatePet**
> Book updatePet(body, ID, title, author, publisher, ISBN, pubdate, nopg, genre)

Update details of existing book

Update details of existing book by Id

### Example
```javascript
import {AnakhasBookStore} from 'anakhas_book_store';

let apiInstance = new AnakhasBookStore.BookApi();
let body = new AnakhasBookStore.Book(); // Book | Update an existent book in the store
let ID = 56; // Number | 
let title = "title_example"; // String | 
let author = "author_example"; // String | 
let publisher = "publisher_example"; // String | 
let ISBN = "ISBN_example"; // String | 
let pubdate = "pubdate_example"; // String | 
let nopg = 56; // Number | 
let genre = "genre_example"; // String | 

apiInstance.updatePet(body, ID, title, author, publisher, ISBN, pubdate, nopg, genre, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Book**](Book.md)| Update an existent book in the store | 
 **ID** | **Number**|  | 
 **title** | **String**|  | 
 **author** | **String**|  | 
 **publisher** | **String**|  | 
 **ISBN** | **String**|  | 
 **pubdate** | **String**|  | 
 **nopg** | **Number**|  | 
 **genre** | **String**|  | 

### Return type

[**Book**](Book.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

