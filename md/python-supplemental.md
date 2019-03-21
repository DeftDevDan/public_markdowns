# API

API is the acronym for Application Programming Interface. An API call, at its most basic form, is a communication method composed of a request for information and the response with that information from a server.

There are thousands of API's available online with access to a wealth of information. Among those are going to be API's such as SalesForce, Google Ads, Mailchimp, etc.

# Jupyter Notebooks

Jupyter Notebook is a dynamic web application that allows the user to both input code AND see the resulting output in the same environment. The output can include visualizations such as narrative text, charts and graphs. It is extremely user-friendly easy to learn and navigate. We will be using Jupyter Notebooks to write in Python

# Python

Python is a general purpose coding language that emphasizes readability. It enables constructs that enable clear programming on both a small and large scale. It is particularly effective when working with vary large data sets.

# Coding Terms

* **Variable**: Variables are references to stored data. In Python, data is stored in specific data types.
    
    * **Strings**: Strings are identified as a set of characters encapsulated by quotation marks. For example:
     
        * string_variable = "This is a string variable"
    
    * **Number**: Numeric values are stored as numbers. For example:

        * number_variable = 20

    * **Array**: An array is used to store a list of data, separated by commas. Array indexing starts at 0. For example:

        * array_variable = ["This", "is", "an", "array", "variable"]

        * array_variable[0] would refer to the string "This".

* **JSON**: JSON stands for JavaScript Object Notation. JSON is used to format the API response. Example of a JSON response:

    ```JSON
    {
        "data": [
            {
            "id": "28623425344",
            "user_id": "150573462",
            "game_id": "488191",
            "community_ids": [
                "848d95be-90b3-44a5-b143-6e373754c382",
                "8deb7b0f-d5a3-4f9d-942d-2331d8f4fe3d",
                "ff1e77af-551d-4993-945c-f8ceaa2a2829"
            ],
            "type": "live",
            "title": "CHILL // PSYCHEDELIA :: ambience \u0026 tones  [ !visuals ]",
            "viewer_count": 9001,
            "started_at": "2018-05-08T18:47:34Z",
            "language": "en",
            "thumbnail_url": "https://static-cdn.jtvnw.net/previews-ttv/live_user_amorelandra-{width}x{height}.jpg"
            }
            ...
        ],
        "pagination": {
            "cursor": "eyJiIjpudWxsLCJhIjp7Ik9mZnNldCI6MX19"
        }
    }
    ```

* **Function**: A function is a block of organized, reusable code that is used to perform a single, related action. Much like how Excel and Tableau have built in functions, such as SUM or AVG Python also has built in functions, such as `print()`

* **Get Request**: A get request is used to retrieve data from the API server. Example of a get request:

    ```python
    # Do not forget to include the dependencies
    import requests
    import json

    # The Client-ID is used to manage who is accessing the API
    headers = {"Client-ID": "<INPUT YOUR CLIENT ID HERE>"}

    # URL endpoint
    twitch_url_gt = "https://api.twitch.tv/helix/games/top"

    # Syntax for the Get Request
    twitch_res_gt = requests.get(twitch_url_gt, headers = headers).json()
    ```

* **Dependencies**: Just like Excel and Tableau have built in functions, like SUM or AVG, Python has functions that are natively built into the code. Libraries, like requests and pandas, can be imported to extend Python's utility, as well as valuable functionality that does not exist in Python out of the box.