
```asm
section .data
    ; Define messages to be printed
    msg1 db 'currently improving Rust and learning Reverse Engineering', 0Ah
    len1 equ $-msg1 ; Calculate length of msg1
    msg2 db 'working with languages like C++, Rust, Intel x86 Assembly and more', 0Ah
    len2 equ $-msg2 ; Calculate length of msg2
    
section .text
    global _start
    
_start:
    ; Print first message (msg1)
    mov eax, 4          ; system call for write
    mov ebx, 1          ; file descriptor 1 (stdout)
    mov ecx, msg1       ; message to print
    mov edx, len1       ; length of message
    int 0x80            ; call kernel
    
    ; Print second message (msg2)
    mov eax, 4          ; system call for write
    mov ebx, 1          ; file descriptor 1 (stdout)
    mov ecx, msg2       ; message to print
    mov edx, len2       ; length of message
    int 0x80            ; call kernel
    
    ; Exit program
    mov eax, 1          ; system call for exit
    xor ebx, ebx        ; exit code 0
    int 0x80            ; call kernel
```

![GitHub stats](https://github-readme-stats.vercel.app/api?username=fresh-milkshake&show_icons=true&hide_border=true)
