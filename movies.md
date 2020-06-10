**Search Movies**
----
  Returns json data of all movies related to the search

* **URL**

  /movies/ : name

* **Method:**

  `GET`
  
    String : name [ title of movie ]

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `[{ "imagie": "image.jpg","title": "The Matrix",  "link": "https://..." }.{...}]`
 


* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/series/riverdale",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```



**Get Download Link & Info**
----
  Returns download link and movie full info.

* **URL**

  /movies/

* **Method:**

  `POST`
  

* **Body Params**

  { " link " : "https://......" }

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ "imagie": "image.jpg","title": "The Matrix",  "link": "https://..." }`


 

* **Sample Call:**

  ```javascript
  fetch("/movies/",{
    headers: {
      'Accept': 'application/json',
      'Content-Type': 'application/json'
    },
    method: "POST",
    body: JSON.stringify({"link": "https://"})
    })


  ```

***

**Search Tv Series**
----
  Returns json data of all tv series related to the search

* **URL**

  /series/ : name

* **Method:**

  `GET`
  
    String : name [ title of movie ]

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `[{ "imagie": "image.jpg","title": "The Matrix",  "link": "https://..." }.{...}]`
 


* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/series/riverdale",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```



**Get Download Link & Info**
----
  Returns download links and series full info.

* **URL**

  /series/

* **Method:**

  `POST`
  

* **Body Params**

  { " link " : "https://...." }

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ "imagie": "image.jpg","title": "The Matrix",  "link": ["https://...S01.mkv","https://...S02.mkv",...] }`


 

* **Sample Call:**

  ```javascript
  fetch("/series/",{
    headers: {
      'Accept': 'application/json',
      'Content-Type': 'application/json'
    },
    method: "POST",
    body: JSON.stringify({"link": "https:.."})
    })


  ```