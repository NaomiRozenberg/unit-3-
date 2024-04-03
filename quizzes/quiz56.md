```py
def secret_handshake(number):

    handshake_actions = []
    binary_digits = format(number, '05b')
    if binary_digits[-1] == '1':
        handshake_actions.append("wink")
    if binary_digits[-2] == '1':
        handshake_actions.append("double blink")
    if binary_digits[-3] == '1':
        handshake_actions.append("close your eyes")
    if binary_digits[-4] == '1':
        handshake_actions.append("jump")
    if binary_digits[-5] == '1':
        handshake_actions.reverse()

    return handshake_actions

actions = secret_handshake(30)
print( actions)
```
