## getUserPlaylist
The returned data includes the default playlist (LovedTracks) and user-created playlists.

### Request Example

```java
MediaGetUserPlaylistRequest request = new MediaGetUserPlaylistRequest();

request.setLimit(2);
//Optional. Sets the maximum number of items to be returned in the response. 
//Default is 20.

request.setOffset(2);
//Optional. Sets the index of the first returned item.
//Default is 0.

MediaGetUserPlaylistRequestResponse response = MediaService.getInstance().getUserPLaylist(request);

```
### Request Example
All items in the data object are guaranteed. The returned data includes the default playlist (LovedTracks) and a user-created playlist (7374971144), which contains two tracks. 

```java
{
  "code": 0,
  "requestId": "58E804B8-89E7-4B75-97CF-A636A9CF5F92",
  "timestamp": 1584326665008,
  "domainId": "media",
  "data": [
    {
      "id": "2906653066",
      "type": "playlist",
      "provider": "deezer",
      "name": "Loved tracks",
      "description": "",
      "imageUrl": "https://e-cdns-images.dzcdn.net/images/cover/f0604f1104723a8cb0bd1439bc6f6a30/250x250-000000-80-0-0.jpg",
      "isPublic": false,
      "userCreated": true,
      "isLovedTracks": true,
      "numberOfTracks": 1
    },
    {
      "id": "7374971144",
      "type": "playlist",
      "provider": "deezer",
      "name": "demo 0312",
      "description": "",
      "imageUrl": "https://e-cdns-images.dzcdn.net/images/cover/9eb6bea4df2af219453ec4aad616ec58/250x250-000000-80-0-0.jpg",
      "isPublic": true,
      "userCreated": true,
      "isLovedTracks": false,
      "numberOfTracks": 2
    }
  ]
}

```



