## createPlaylist
For Deezer Premium accounts, users can create their personal playlists.  

### Request Example

```java
MediaCreatePlaylistRequest request = new MediaCreatePlaylistRequest();

request.setProvider("deezer"); 
//Required. ID of this media provider. Supported providers include deezer (premium account)
//and tidal. Provider ID must be entered in lowercase characters.

request.setName("My Playlist");
//Required. The name of this playlist being created.

MediaCreatePlaylistResponse response = MediaService.getInstance().createPLaylist(request);

```

### Response Example
All items in the data object are guaranteed. This example shows that playlist ID, “7389366844” with the name “My Playlist” has been created. The new playlist is created by a user and not a default playlist, and is publicly accessible. Note that a newly created playlist has no tracks until they are added to it. 

```java
{
  "code": 0,
  "requestId": "257F1180-FB43-4E6E-8EB0-45AEE2333D09",
  "timestamp": 1584339031494,
  "domainId": "media",
  "data": [
    {
    "id": "7389366844",
    "type": "playlist",
    "provider": "deezer",
    "name": "My Playlist",
    "description": "",
    "imageUrl": "https://e-cdns-images.dzcdn.net/images/cover//250x250-000000-80-0-0.jpg",
    "isPublic": true,
    "userCreated": true,
    "isLovedTracks": false,
    "numberOfTracks": 0
    }
  ]
}

```
