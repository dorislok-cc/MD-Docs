## addFavorites
Favorites are provider specific, not all media types can be added as favorites. The following table lists media types for favorites that are supported by different providers. 

| Provider  |  Album |  Artist |   Track| Radio  |  Playlist |  Genre |  Podcast | Station  | Episode  |  Host |
|---|---|---|---|---|---|---|---|---|---|---|
|  deezer (premium) |  ✔ | ✔  |  ✔ |  ✔ |  ✔ | ✔  |  ✔ |   |  ✔ |   |
| deezer (fremium)  |   |  ✔ |   |   ✔|   |   |   |   |   |   |
|  spotify* |  ✔ |  ✔ |  ✔ |   | ✔  |   |  ✔ |   |   |   |
|  tunein |   |   |   |   |   |   |  ✔ | ✔  |  ✔ |   |
| kuwo  |   |   |  ✔ |   |   |   |   |   |   |   |
|  ximalya |   |   |   |   |   |   |   |   |   |   ✔|

*Applies to both premium and fremium accounts.


### Request Example

```java
MediaAddFavoritesRequest request = new MediaAddFavoritesRequest();

request.setId("678371"); 
//Required. Media ID. The format varies among providers. For example, s30370 (tunein), 678371 (deezer), A2HB8BMTCDQSQ4 (amazon), and so forth.

request.setType("track"); 
//Required. Media type such as album, artist, radio, playlist, genre, podcast, and host.

request.setProvider("deezer"); 
//Required. Provider ID. Enter the value in lowercase characters. 

request.setName("True Blue");
//Required. Name of "setType." If “setType” is track, “setName” is the name of the track.

request.setDescription("My favorite track");
//Optional. A  brief summary describing “setType.”

request.setImageUrl("https://m.media-amazon.com/images/I/81ITzP4YjoL._SX325_SY325_.jpg");
//Optional. The URL associated with the image of this favorite.

request.setDuration(268);
//Optional. Integer The duration of the track is expressed in number of seconds. 
0 indicates that duration is unknown.

request.setAdvertisement(false);
//Optional. True indicates that this track is an advertisment; false indicates otherwise. 

request.setArtists();
//Optional. A list of ID and name of the artist.

request.setAlbum();
//Optional. A list of ID and name of the album.

MediaAddFavoritesResponse response = MediaService.getInstance().AddFavorites(request);
```
### Response Example
Status of the operation is returned.

```java
{
  "code": 0,
  "requestId": "629729aa-3c74-256c-4602-af373dcafaa1",
  "timestamp": 1543359888133,
  "domainId": "media",
  "success": "favorite added",
  "cccontext": {
    "requestId": "629729aa-3c74-256c-4602-af373dcafaa1",
    "sessionId": "08612232-e5af-e720-d5f7-1c730bf1c4d7"
  }
}
```
<button type="button" onclick="('POST %20media%20favorites!')">< Previous</button>
<button type="button" onclick="('getStreamingUrls.md!')">> Next</button>
