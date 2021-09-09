Write a function that fills memory with a constant byte.

Prototype: char *_memset(char *s, char b, unsigned int n); The _memset() function fills the first n bytes of the memory area pointed to by s with the constant byte b Returns a pointer to the memory area s FYI: The standard library provides a similar function: memset. Run man memset to learn more.

julien@ubuntu:~/0x06$ cat 0-main.c #include "holberton.h" #include <stdio.h>

/**

simple_print_buffer - prints buffer in hexa

@buffer: the address of memory to print

@size: the size of the memory to print

Return: Nothing. */ void simple_print_buffer(char *buffer, unsigned int size) { unsigned int i;

 i = 0;
 while (i < size)
 {
         if (i % 10)
         {
                 printf(" ");
         }
         if (!(i % 10) && i)
         {
                 printf("\n");
         }
         printf("0x%02x", buffer[i]);
         i++;
 }
 printf("\n");
 }