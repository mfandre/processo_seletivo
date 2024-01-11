# Teste Dev Senior

Enunciado:

```python
###
### Implementar uma função que receba um texto e uma palavra de entrada e encontre a palavra mais próxima nesse texto.
### Essa função deve retornar a linha e a coluna onde se encontra a palavra.
### Unit test são obrigatórios!
###

from typing import Tuple

my_main_text = '''Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam convallis sit amet lacus id suscipit. 
Nunc cursus vehicula pharetra. Curabitur eget accumsan nisl, in scelerisque quam. 
Quisque eu sagittis augue, vitae luctus felis. Praesent ultricies sapien vel leo tincidunt pulvinar. 
Curabitur mollis sapien nec massa semper pellentesque. Duis laoreet urna ac nisi ultricies, sed iaculis diam ultrices. 
Vivamus in euismod est, eu consectetur tortor. Quisque molestie felis quis mauris hendrerit rutrum. 
Duis porttitor ligula mollis, eleifend magna at, fringilla nisl. Pellentesque venenatis laoreet tincidunt.
'''

def find_closest_word(text: str, word: str) -> Tuple:
    # TODO
    pass

closest = find_closest_word(my_main_text, "Lorem")
print("Lorem =>", closest)
## (0, 0) => line 0 and column 0

closest = find_closest_word(my_main_text, "ipsum")
print("ipsum =>", closest)
## (0, 6) => line 0 and column 6

closest = find_closest_word(my_main_text, "pysum")
print("pysum =>", closest)
## (0, 6)

closest = find_closest_word(my_main_text, "psum")
print("psum =>", closest)
## (0, 6)

closest = find_closest_word(my_main_text, "Nunc")
print("Nunc =>",closest)
## (1, 0)

closest = find_closest_word(my_main_text, "qusque")
print("qusque =>", closest)
## (2, 0)
```

Solução:
