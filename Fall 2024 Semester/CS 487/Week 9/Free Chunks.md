

`free(p)`: looks at the chunks just before and after p to see if they are free
- Adjacent free chunks are removed from their respective free lists
- combined with p to make a larger chunk `p'`

Optimization



Removing free



