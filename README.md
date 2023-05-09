
```asm
section .data
    msg1 db 'currently improving Rust and learning Reverse Engineering', 0Ah
    len1 equ $-msg1
    msg2 db 'working with languages like C++, Rust, Intel x86/64 Assembly and more', 0Ah
    len2 equ $-msg2
    
section .text
    global _start
    
_start:
    mov eax, 4
    mov ebx, 1        
    mov ecx, msg1     
    mov edx, len1    
    int 0x80         
    
    mov eax, 4 
    mov ebx, 1        
    mov ecx, msg2     
    mov edx, len2      
    int 0x80       
    
    mov eax, 1        
    xor ebx, ebx    
    int 0x80          
```

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=fresh-milkshake&layout=compact)
