**Trending Music**
----
  Returns json data of all current music.

* **URL**

  /music/

* **Method:**

  `GET`
  
*  **URL Params**

    None

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `[{ img : "***.jpg", link : "https://..." , head :"Lil wayne-Cater V", info:"lorem......" }.{...}]`
 


* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/users/1",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```


**Search Music**
----
  Returns json data for searched music.

* **URL**

  /music/q/:music

* **Method:**

  `GET`
  
  String : music [ musictitle or Artist name ]

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `[ { img : "***.jpg", link : "https://..." , head :"Lil wayne-Cater V", info:"lorem......" } ,{...}]`
 


* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/music/q/nastyc",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```

**Download Music || Music Info**
----
  Returns download link and music infomation about a single music.

* **URL**

  /music/d/

* **Method:**

  `POST`
  

* **Body Params**

  { " link " : " https://...... " }

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ imgae : "***.jpg", link : "https://..." , title :"Lil wayne-Cater V", discripton:"lorem......" }`
 


* **Sample Call:**

  ```javascript
  fetch("/music/d/",{
    headers: {
      'Accept': 'application/json',
      'Content-Type': 'application/json'
    },
    method: "POST",
    body: JSON.stringify({"link": "https://...."})
    })


  ```