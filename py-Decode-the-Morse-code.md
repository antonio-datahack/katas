```py
def decode_morse(morse_code):
    arr = morse_code.replace("   ","  ").strip().split(" ")
    return "".join([" " if i == "" else MORSE_CODE[i] for i in arr])


def decode_morse(morse_code):
    return "".join([" " if i == "" else MORSE_CODE[i] for i in morse_code.replace("   ","  ").strip().split(" ")])

```
