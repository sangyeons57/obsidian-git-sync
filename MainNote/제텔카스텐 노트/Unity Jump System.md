#CSharp #unity 

```CSharp

bool isGround

void Update()
{
isGround = Physics2D.OverlapCircle(
	(Vector2)transform.position +
	 new Vector2(0, -0.5f), 0.07f,
	  1 << LayerMask.NameToLayer("Ground"));

if ( isGround &&  (Input.GetKeyDown(KeyCode.W) ||
	 Input.GetKeyDown(KeyCode.UpArrow)
	)) pv.RPC("JumpRPC", RpcTarget.All);
}
```