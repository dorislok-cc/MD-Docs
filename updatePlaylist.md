## updatePlaylist
Users can update playlists that they create. Except the provider and playlist ID, they can make changes to other parameters. 


### Request Example

```java
MediaUpdatePlaylistRequest request = new MediaUpdatePlaylistRequest();

request.setProvider("deezer"); 
//Required. ID of this media provider. Supported providers include deezer (premium account) 
//and tidal. Provider ID must be entered in lowercase characters.

request.setPlaylistId("2906653066"); 
//Required. Playlist ID being updated.

request.setName("My Playlist");
//Optional. The name of this playlist being updated.

request.setPublic(false);
//Optional. True indicates that this is a public playlist; false indicates otherwise.

request.setDescription("Added ABC track”);
//Optional. A brief summary/notation about this playlist.

MediaUpdatePlaylistResponse response = MediaService.getInstance().updatePLaylist(request);

```

### Response Example
All items in the data object are guaranteed. This example shows that playlist ID, "7368781344" is updated with the name “this side up” and a description.

```java
{
  "code": 0,
  "requestId": "855378DB-22EB-4AA4-A77A-7B1A0269A6F0",
  "timestamp": 1584337977628,
  "domainId": "media",
  "data": [
    {
    "id": "7368781344",
    "type": "playlist",
    "provider": "deezer",
    "name": "this side up",
    "description": "Play once more",
    "imageUrl": "https://e-cdns-images.dzcdn.net/images/cover/9eb6bea4df2af219453ec4aad616ec58/250x250-000000-80-0-0.jpg",
    "isPublic": true,
    "userCreated": true,
    "isLovedTracks": false,
    "numberOfTracks": 2
    }
  ]
}

```
