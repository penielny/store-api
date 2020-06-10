**Trending News**
----
  Returns json data of all current and trending tech news.

* **URL**

  /technews/news/

* **Method:**

  `GET`
  
*  **URL Params**

    None

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `[{"id":1, image : "***.jpg", href : "facebook/..." , title :"Facebok ...", content:"lorem......" }.{...}]`
 


* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/technews/news/",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```


**Search TechNews**
----
  Returns json data for searched tech news.

* **URL**

  technews/q/:topic

* **Method:**

  `GET`
  
  String : topic [ subject or company ]


* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `[{"id":1, image : "***.jpg", href : "facebook/..." , title :"Facebok ...", content:"lorem......" }.{...}]`
 
 


* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/technews/q/facebook",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```

**Get Full Article**
----
  Returns full article on a single news.

* **URL**

  /technews/r/

* **Method:**

  `POST`
  

* **Body Params**

  { " link " : "facebokk/...... " }

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ "image": "image.jpg","title": "facebook ...",  "content": "lorem ..." }`


 

* **Sample Call:**

  ```javascript
  fetch("/technews/r/",{
    headers: {
      'Accept': 'application/json',
      'Content-Type': 'application/json'
    },
    method: "POST",
    body: JSON.stringify({"link": "0219/facebook/...."})
    })


  ```