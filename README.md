## 과제2

- SPFLI 테이블에서 CONNID FLTIME DISTANCE 수정
- CONNID : 숫자 0이 앞에 나오도록 수정
- FLTIME  : 시간이 아니라 숫자로 나오도록 수정
- DISTANCE : 소수점이 출력 안되도록 수정
- 힌트: 필드 카탈로그에서 필드 옵션 활용

## 수정 전 모습
![Image](https://github.com/user-attachments/assets/f2f7268d-c7a4-4a7a-a288-3002346a3746)

## 수정 코드 (정확하게는 코드 삽입)

*connid 코드 수정

    fieldcatalog-fieldname   = 'CONNID'.
    fieldcatalog-seltext_m   = 'Flight Connection Numbe'.
    fieldcatalog-col_pos     = 1.
    fieldcatalog-lzero = 'X'. #---> connid의 숫자 0이 앞에 나오도록 수정
    APPEND fieldcatalog TO fieldcatalog.
    CLEAR  fieldcatalog.

lzero : 앞에 0을 붙여줌으로써 자리수 맞추기


*fltime 코드 수정

     fieldcatalog-fieldname   = 'FLTIME'.
     fieldcatalog-seltext_m   = 'Flight time'.
     fieldcatalog-col_pos     = 2.
     fieldcatalog-datatype = 'NUM'. #---> fltime 시간이 아니라 숫자로 나오도록 수정
     APPEND fieldcatalog TO fieldcatalog.
     CLEAR  fieldcatalog.
     
*DISTANCE 코드 수정

       fieldcatalog-fieldname   = 'DISTANCE'.
       fieldcatalog-seltext_m   = 'Distance'.
       fieldcatalog-col_pos     = 5.
       fieldcatalog-decimals_out = 0. #---> distance 소수점이 출력 안되도록 수정
       APPEND fieldcatalog TO fieldcatalog.
       CLEAR  fieldcatalog.

## 수정 후 모습

![Image](https://github.com/user-attachments/assets/f22566e3-d1ae-4a4c-8f36-d1c9efb89e23)
