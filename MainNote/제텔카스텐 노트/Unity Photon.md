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
public ovv

```
