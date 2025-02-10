

[[TypeScript]]



enum type provides a way to define a set of named constants.

Makes it easier to work with sets of related values and improve readability of code.



``` TypeScript
enum Direction {
	Up,
	Down,
	Left,
	Right
}

let move: Direction = Direction.Up;

let move = Direction.Down; // type inference? will it infer that it's of type direction?
```