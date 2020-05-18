## addTrackToPlaylist
When a playlist has been created, users can then add tracks to it. Note that users can add tracks only to their personal playlists; they cannot add tracks to the default playlist, "Love Tracks." 

### Request Example

```java
MediaAddTrackToPlaylistRequest request = new MediaAddTrackToPlaylistRequest();

request.setProvider("deezer"); 
//Required. ID of this media provider. Supported providers include deezer (premium account) and tidal. Provider ID must be entered in lowercase characters.

request.setPlaylistId("2906653066"); 
//Required. Playlist ID to which tracks are added.

request.setIds("3135553");
//Required. Track IDs to be added.

MediaAddTrackToPlaylistResponse response = MediaService.getInstance().addTrackToPlaylist(request);

```

### Response Example
Code 0 indicates that this operation is a success. 

```java
{
  "code": 0,
  "requestId": "EC66E128-00AB-4E48-A1A0-BF166F5E96AD",
  "timestamp": 1584337003142,
  "domainId": "media"
}
