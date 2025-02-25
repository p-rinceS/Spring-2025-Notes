

Idea : Split one lock into multiple 

- Requires careful thought
We have to reason about all operations at once
[[linearizable]] helps a lot. 

Split object into logical parts where each part has it's own lock and the methods that work on separate parts can work concurrently



How do we split the list locks?  