
 PhotonNetwork.Instantiate("Bullet", transform.position, Quaternion.identity)
                    .GetComponent<PhotonView>().RPC("DirRPC", RpcTarget.All);
 