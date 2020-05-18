## reorderPlaylist
Users can re-order their playlist based on track IDs provided. Suppose the original order is 1, 2, 3, 4. If track IDs 4 and 2 are provided, only these 2 track IDs are sorted. The updated order is 1, 4, 3, 2.

### Request Example

```java
MediaReorderPlaylistRequest request = new MediaReorderPlaylistRequest();

request.setProvider("deezer"); 
//Required. ID of this media provider. Supported providers include deezer (premium account) 
//and tidal. Provider ID must be entered in lowercase characters.

request.setPlaylistId("2906653066"); 
//Required. Playlist ID containing the tracks.

request.setIds("3135553");
//Required. Array of track IDs to be re-ordered.

MediaReorderPlaylistResponse response = MediaService.getInstance().reorderPLaylist(request);

```

### Response Example
Code 0 indicates that the operation is a success.

```java
{
  "code": 0,
  "requestId": "9FD1CC96-3362-40BF-9A0F-96CE3EA94599",
  "timestamp": 1584005779251,
  "domainId": "media"
}

```
