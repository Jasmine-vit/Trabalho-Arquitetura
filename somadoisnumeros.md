# Trabalho-Arquitetura
trabalho sobre soma de dois números
	# Imprimi string 'texto' na tela
	la $a0, texto
	addi $v0, $zero, 4
	syscall

	# Pega inteiro digitado pelo usuário
	addi $v0, $zero, 5
	syscall
	add $s0, $v0, $zero

	# Imprimi string 'texto' na tela
	la $a0, texto
	addi $v0, $zero, 4
	syscall

	# Pega inteiro digitado pelo usuário
	addi $v0, $zero, 5
	syscall
	add $s1, $v0, $zero

	# soma os dois inteiros guardados
	add $s2, $s0, $s1

	# Imprimi string 'soma' na tela
	la $a0, soma
	addi $v0, $zero, 4
	syscall

	# Imprimi o resultado
	add $a0, $s2, $zero
	addi $v0, $zero, 1
	syscall

	jr $ra
