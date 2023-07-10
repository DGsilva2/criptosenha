# criptosenha
#armazenar
from hashlib import sha256

senha = input('senha: ')
senha_armazenar = sha256(senha.encode()).hexdigest()
print(senha_armazenar)

# login

senha_login = input('senha login:')
hash_senha_login = sha256(senha_login.encode()).hexdigest()
if hash_senha_login == senha_armazenar:
    print('senha correta')
else:
    print('senha incorreta')
