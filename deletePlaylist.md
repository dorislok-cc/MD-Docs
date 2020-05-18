## deletePlaylist
Users can delete playlists that they create. Users cannot delete the default playlist (Loved tracks).

### Request Example

```java
MediaDeletePlaylistRequest request = new MediaDeletePlaylistRequest();

request.setProvider("deezer"); 
//Required. ID of this media provider. Supported providers include deezer (premium account) 
//and tidal. Provider ID must be entered in lowercase characters.

request.setPlaylistId("2906653066"); 
//Required. Playlist ID to be deleted.

MediaDeletePlaylistResponse response = MediaService.getInstance().deletePlaylist(request);

```
### Response Example
Code 0 indicates that this operation is a success.

```java
{
  "code": 0,
  "requestId": "13995295-D130-4E56-A419-11FC8F583190",
  "timestamp": 1584337003142,
  "domainId": "media"
}

```
