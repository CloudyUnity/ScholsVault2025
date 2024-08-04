A cipher is an algorithm to disguise a message 
Cryptography is the art of designing ciphers

Affine Cipher:
	$E(x) = y \equiv (ax + b)$ (mod n)
	$D(y) = x \equiv v(y - b)$ (mod n)
		$v$ is the inverse of $a$ (mod n)
	For an alphabetical cipher n = 26
	Easy to decode when you find a small piece of info

Exponential Cipher:
	$p$ is a prime number
	$k \in \mathbb{Z}_{p - 1}$ and co-prime with $p-1$
	$k'$ is the inverse of $k$ (mod $p$ - 1)
	$E_k(x) \equiv x^k$ (mod $p$)
	$D_k(y) \equiv y^{k'}$ (mod $p$)
	For an alphabetical cipher $p$ = 29

#bonus 
RSA Cipher:
	Choose two large primes $p$ and $q$
	$n = pq$
	$n$ is a public key but $p,q$ are private keys
	$k \in \mathbb{Z}_{(p-1)(q-1)}$ and co-prime with $(p-1)(q-1)$
	$k'$ is the inverse of $k$ (mod $(p-1)(q-1)$)
	$E_k(x) \equiv x^k$ (mod $n$)
	$D_k(y) \equiv y^{k'}$ (mod $n$)