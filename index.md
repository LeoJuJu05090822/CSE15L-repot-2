First code change
![c05c9e26a740fbd5790eaf13e31c945](https://user-images.githubusercontent.com/103226676/165013734-0cbf69d4-6d65-4efb-9324-ffc5c98c76e3.png)
[failure inducing 1](https://leojuju05090822.github.io/markdown-parser/testError-file.md)
Exception in thread "main" java.lang.OutOfMemoryError: Java heap space
![b63bff0e5f0d1d73b050e18a481a7c5](https://user-images.githubusercontent.com/103226676/165015236-4487eb8d-59af-4315-b6ea-4ed086f0287d.png)
The failure-inducing input has a second line without a bracket or parentheses, so the file will continue the while loop which produce the bug of logic errorit. The infinte loop caused the sympton out of memory.

Second code change
![e7fdcce2c668878f92460d88a7e8ba5](https://user-images.githubusercontent.com/103226676/165019338-d06bbf31-798e-4fab-8290-165797dda35d.png)
[failure inducing2](https://leojuju05090822.github.io/markdown-parser/test3.md)
![5c9544fe24d4003103544a3673fa359](https://user-images.githubusercontent.com/103226676/165019577-13cc51a9-93c6-4168-8d9d-1264bc89436b.png)
The failure-inducing input has a second line without a bracket or parentheses. Although the file will break when it cannot find the brackets, this code, toReturn.add(markdown.substring(openParen + 1, closeParen)); and currentIndex = closeParen + 1; will appear before break, which cause the link will add agian when we run the seond time of while loop before break. It's a logical error, casued the wrong answer sympton.

Third code change 
![344623eac09d7de2c1f3348880ad2d9](https://user-images.githubusercontent.com/103226676/165026358-29efb4ae-d2c7-4b11-967a-4a9e38f7a9a2.png)
[failure inducing3](https://leojuju05090822.github.io/markdown-parser/test4.md)
![a0f9f045fbd7094d918723cdab54cdc](https://user-images.githubusercontent.com/103226676/165026749-92ee850e-3db0-45a6-b22c-0595e66ea22e.png)
when there is something between the close bracket and openPare, it's a invalid link. Howver, there is a logic error in reading the link which neglect the text between the colosreBra and openParen. Thus, it will still print out the invalid link in the array. worng answer Symptom
