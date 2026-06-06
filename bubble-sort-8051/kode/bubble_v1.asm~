ORG     0000H
        LJMP    MAIN
        ORG     0030H
MAIN:
        MOV     20H,#08H
        MOV     21H,#07H
        MOV     22H,#05H
        MOV     23H,#03H
        MOV     24H,#01H
        MOV     R1,#04H
OUTER:
        MOV     A,R1
        MOV     R2,A
        MOV     R0,#20H
INNER:
        MOV     A,@R0
        INC     R0
        MOV     B,@R0
        CLR     C
        SUBB    A,B
        JNC     NOSWAP
        DEC     R0
        MOV     A,@R0
        XCH     A,B
        MOV     @R0,A
        INC     R0
        MOV     @R0,B
NOSWAP:
        DJNZ    R2,INNER
        DJNZ    R1,OUTER
DONE:
        SJMP    DONE
        END