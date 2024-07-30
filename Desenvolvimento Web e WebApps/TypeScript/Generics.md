
O generic no TypeScript nos permite reutilizar uma determinada implementação de código, de forma tipada. Para representar um generic, nós declaramos ele dessa forma `<T>`(podendo ser utilizado qualquer outra letra, existem as convenções que podemos seguir.

```ts
/*
	* <S> → Representando State
	* <T> → Representando Type
	* <K> → Representando Key
	* <V> → Representando Value
	* <E> → Representando Element
*/

function useState<T>() {
	let state: T

	function get() {
		return state
	}

	function set(newValue: T) {
		state = newValue
	}

	return { get, set }
}

let newState1 = useState();
let newState2 = useState<string>();

newState1.get();
newState1.set("João");
newState1.set(123);

newState2.set(123);
```
