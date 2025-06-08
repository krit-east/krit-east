; KRIT
; -------------------------------

.data
    name        db      'Krit', 0
    title       db      'Full Stack Developer', 0
    project     db      'East Hub V3', 0

.code
main proc
    ; Initialize Developer Profile
    mov     ax, @data
    mov     ds, ax
    
    ; Display Skills
    call    LoadFrontendSkills         ; React, Next.js, TypeScript, Tailwind, Html, CSS, Vue, Nuxt.js
    call    LoadBackendSkills          ; Node.js, Express, MongoDB, Prisma, ElysiaJS, C#, C++
    call    LoadReverseEngineeringSkills ; IDA Pro, x64dbg, Unity Netcode

    ; Current Status
    push    project
    call    WorkingOn
    add     sp, 2
    
    ; Exit Routine
    mov     ax, 4C00h
    int     21h
main endp

; Contact Subroutines
GitHub      proc
    ; https://github.com/krit-east
    ret
GitHub      endp

; Skill Subroutines
LoadReverseEngineeringSkills proc
    ; Expertise: Ghidra, IDA Pro, x64dbg, reversing Unity Netcode (Entities, Huffman, Quantization)
    ret
LoadReverseEngineeringSkills endp

end main
