#CSharp #static #readonly

이건 c#코드인데 왜 static으로 표시할수없다는 거지? public static const int PLAYER1 = 1; public static const int PLAYER2 = 2;

---

`const` 키워드는 값을 상수화할 때 사용하며, 정적(static)으로 표시할 수 없습니다. 만약 정적으로 표시하고 싶다면, 다음과 같이 수정하시면 됩니다

`readonly` 키워드는 C# 언어에서 사용되는 접근 제한자입니다. `readonly` 키워드를 사용하면 해당 필드는 객체가 생성된 이후에도 값이 변경되지 않는 것을 보장할 수 있습니다.

예를 들어, 다음 코드처럼 `readonly` 키워드를 사용할 수 있습니다.

---
즉 const대신 사용할수잇다