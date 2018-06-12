# Pexels API
A simple wrapper to use the [Pexels API](https://www.pexels.com/api/). Please refer to the API docs to undestand the inputs and expected results.

### Installation

Install the package

```sh
$ cd /path/to/app
$ npm install --save pexels-api-wrapper
```

### Usage

```js
//In NodeJS App

//Require Wrapper Library
const PexelsAPI = require('pexels-api-wrapper');

//Create Client instance by passing in API key
var pexelsClient = new PexelsAPI("<API_KEY>");

//Search API
pexelsClient.search("food", 10, 1)
    .then(function(result){
        console.log(result);
    }).
    catch(function(e){
        console.err(e);
    });

//Get Popular Photos
pexelsClient.getPopularPhotos(10, 1)
    .then(function(result){
        console.log(result);
    }).
    catch(function(e){
        console.err(e);
    });

//Get Curated Photos
pexelsClient.getCuratedPhotos(10, 1)
    .then(function(result){
        console.log(result);
    }).
    catch(function(e){
        console.err(e);
    });

//Get Photo by ID
pexelsClient.getPhoto(123456)
    .then(function(result){
        console.log(result);
    }).
    catch(function(e){
        console.err(e);
    });

//Search Video API
pexelsClient.searchVideos("food", 10, 1)
    .then(function(result){
        console.log(result);
    }).
    catch(function(e){
        console.err(e);
    });

//Get Popular Videos
pexelsClient.getPopularVideos(10, 1)
    .then(function(result){
        console.log(result);
    }).
    catch(function(e){
        console.err(e);
    });
```


### API

#### Search
Promise factory to interact with Pexels Search API

| Param | Type | Description |
| ----- | ---- | ----------- |
| **query** | *string* | The search term to query the API with
| **per_page** | *number* | The number of results to return per page (Defaults to 10)
| **page** | *number* | The page number to return (Defaults to 1)

```js
PexelsAPI.search(query, per_page, page);
```

#### Popular
Promise factory to interact with Pexels Popular Photos API

| Param | Type | Description |
| ----- | ---- | ----------- |
| **per_page** | *number* | The number of results to return per page (Defaults to 10)
| **page** | *number* | The page number to return (Defaults to 1)

```js
PexelsAPI.getPopularPhotos(per_page, page);
```

#### Curated
Promise factory to interact with Pexels Curated Photos API

| Param | Type | Description |
| ----- | ---- | ----------- |
| **per_page** | *number* | The number of results to return per page (Defaults to 10)
| **page** | *number* | The page number to return (Defaults to 1)

```js
PexelsAPI.getCuratedPhotos(per_page, page);
```

#### Photo
Promise factory to fetch a single photo from Pexels Photos API

| Param | Type | Description |
| ----- | ---- | ----------- |
| **id** | *number* | The ID of the photo

```js
PexelsAPI.getPhoto(id);
```

#### Search Videos
Promise factory to interact with Pexels Videos API

| Param | Type | Description |
| ----- | ---- | ----------- |
| **query** | *string* | The search term to query the API with
| **per_page** | *number* | The number of results to return per page (Defaults to 10)
| **page** | *number* | The page number to return (Defaults to 1)

```js
PexelsAPI.searchVideos(query, per_page, page);
```

#### Popular Videos
Promise factory to interact with Pexels Popular Videos API

| Param | Type | Description |
| ----- | ---- | ----------- |
| **per_page** | *number* | The number of results to return per page (Defaults to 10)
| **page** | *number* | The page number to return (Defaults to 1)

```js
PexelsAPI.getPopularVideos(per_page, page);
```

### Acknowledgements
Thanks, [Pexels](http://pexels.com) for creating a great platform for great images. Always rooting for you.


Made with :heart: at [Shopalyst](http://shopalyst.com)

