def rc4(key, data):
    # 初始化
    S = list(range(256))
    j = 0
    key = key.encode('utf-8')  
    key_length = len(key)

    # KSA
    for i in range(256):
        j = (j + S[i] + key[i % key_length]) % 256  
        S[i], S[j] = S[j], S[i]  

    # PRGA
    i = j = 0
    keystream = []
    data_bytes = data if isinstance(data, bytes) else data.encode("utf-8")
    for byte in data_bytes:
        i = (i + 1) % 256
        j = (j + S[i]) % 256
        S[i], S[j] = S[j], S[i]  
        k = S[(S[i] + S[j]) % 256]
        keystream.append(k)

    # XOR
    result = bytes(a ^ b for a, b in zip(data_bytes, keystream))
    return result

key = input("輸入金鑰: ")
plaintext = input("輸入待加密字串: ")

encrypted = rc4(key, plaintext)

print(f"加密後字串: {encrypted.hex()}")
