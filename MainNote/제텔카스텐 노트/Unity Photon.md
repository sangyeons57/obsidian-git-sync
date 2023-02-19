#unity #CSharp #Photon2

[튜토리얼 한국어 영상](https://www.youtube.com/playlist?list=PL3KKSXoBRRW3YE4UMnRH762vOhSHLdnpK)

[포톤서버](https://dashboard.photonengine.com/)
에서 CREATE A NEW APP 을하고 App Id를 복사한다

unity 에서 Photon Asset 을 import하고 

App Id를 생성해준다

---
MonoBehaviourPunCallbacks
#MonoBehavour대신에 쓰는고 다양함 함수를 override해서 쓰기위해 사용한다.

```CSharp
PhotonNetwork.NetworkClientState.ToString();
//내트워크 연결 상태를 준다
PhotonNetwork.LocalPlayer.NickName =
//이걸로 클라이언트 닉네임을 설정한다.
//OnConnectedToMaster에서 상용한다.


PhotonNetwork.ConnectUsingSettings();
//connect연결
public override void OnConnectedToMaster() {}
//connect되면실핼하는함수


PhotonNetwork.Disconnect();
//열결끊기
public override void OnDisconnected() {}
//연결끊길때 실행


PhotonNetwork.JoinLobby();
//로비접속
public override void OnJoinedLobby() {}
//로비 접속했을대 실행

```
방을 만들거나 참가할때는 connect되어있던가 Lobby에 있어야한다.

```CSharp
PhotonNetwork.CreateRoom(roomName, new RoomOptions{Maxlayers = 2});


```
RoomOption 들
[MaxPlayers](https://doc-api.photonengine.com/en/pun/v2/class_photon_1_1_realtime_1_1_room_options.html#afe8e03921d811f4fe536cfd9a71dd9bb)
[PlayerTtl](https://doc-api.photonengine.com/en/pun/v2/class_photon_1_1_realtime_1_1_room_options.html#a209447cfcc1477298f53bd59d7771e88)
[EmptyRoomTtl](https://doc-api.photonengine.com/en/pun/v2/class_photon_1_1_realtime_1_1_room_options.html#a01b2d365fd7a9fea82a9dc1e055801c9)
[CustomRoomProperties](https://doc-api.photonengine.com/en/pun/v2/class_photon_1_1_realtime_1_1_room_options.html#acf4d20de1d1a094f4b5253acdf5d9ce0)
[CustomRoomPropertiesForLobby](https://doc-api.photonengine.com/en/pun/v2/class_photon_1_1_realtime_1_1_room_options.html#a9664878066f389ecb8979c636ac78d32)
[Plugins](https://doc-api.photonengine.com/en/pun/v2/class_photon_1_1_realtime_1_1_room_options.html#aab3dbb987830f0c38b167d8b5de6a08f)