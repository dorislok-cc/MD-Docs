## deleteTrackFromPlaylist


### Request Example

```java
MediaDeleteTrackFromPlaylistRequest request = new MediaDeleteTrackFromPlaylistRequest();

request.setProvider("deezer"); 
//Required. ID of this media provider. Supported providers include deezer (premium account) 
//and tidal. Provider ID must be entered in lowercase characters.

request.setPlaylistId("2906653066"); 
//Required. Playlist ID that holds the tracks.

request.setIds("3135553");
//Required. Array of track IDs to be deleted.


MediaDeleteTrackFromPlaylistResponse response = MediaService.getInstance().deleteTrackFromPlaylist(request);

```
### Request Example
Code 0 indicates that this operation is a success.

```java
{
  "code": 0,
  "requestId": "EC66E128-00AB-4E48-A1A0-BF166F5E96AD",
  "timestamp": 1584337003142,
  "domainId": "media"
}

```
