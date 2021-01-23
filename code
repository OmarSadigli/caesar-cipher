alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']

def caesar(text,shift,direction):
  if direction == "encode":
    encrypt(text, shift)
  elif direction == "decode":
    decrypt(text, shift)
  

def encrypt(text, shift):
  cipher_text = ""
  for char in text:
    if char in alphabet:
      shifted_char_index = alphabet.index(char) + shift
      if shifted_char_index > len(alphabet) - 1:
        shifted_char_index = shifted_char_index - len(alphabet)
      new_char = alphabet[shifted_char_index]
      cipher_text += new_char
    else:
      cipher_text += char  
  print(f"The encoded text is {cipher_text}")

def decrypt(text, shift):
  plain_text = ""
  for char in text:
    if char in alphabet:
      shifted_char_index = alphabet.index(char) - shift
      new_char = alphabet[shifted_char_index]
      plain_text += new_char
    else:
      plain_text += char
  print(f"The decoded text is {plain_text}")


should_continue = True
while should_continue:
  direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n")
  text = input("Type your message:\n").lower()
  shift = int(input("Type the shift number:\n"))
  shift = shift % 26

  caesar(text, shift, direction)

  result = input("Type 'yes' if you want to go again. Otherwise type 'no'.\n")
  if result == 'yes':
    should_continue
  else:
    print("Goodbye")
    should_continue = False
