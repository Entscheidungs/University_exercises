.globl main

.data
	#array : .word 4,-1,5,500,0,10000,-256
	array: 1,2,3,4,5
	N  : .word 5
	Somme : .word 0,0

.text

main:
	lw $t0,N
	li $t5,0 #check
scorri:
	beq $t0,$t1,end

	sll $t3,$t1,2
	lw $t4,array($t3)
	add $t2,$t2,$t4
	addi $t1,$t1,1
	beq $t5,0,pari
	beq $t5,1,dispari
	j scorri
	
	
pari:
	lw $s0,Somme
	add $s0,$s0,$t4
	sw $s0,Somme
	li $t5,1
	j scorri
dispari:
	li $s1,4
	lw $s0,Somme($s1)
	add $s0,$s0,$t4
	sw $s0,Somme($s1)
	li $t5,0
	j scorri	
 
end:
	lw $t0,Somme
	lw $t1,Somme($s1)
	
