# WRITE UP TTV - KCSC
## The Doki Club
> ĐỀ BÀI: Một trò chơi vui vẻ để tuyển thành viên, nhưng hình như nó đang bị ai đó chiếm quyền điều khiển...? Hãy cứu lấy nhân vật chính nào

  Vì file có đuôi .zip nên sau khi tải về, ta sẽ thử giải nén ra 
  
<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212960785-754bc0be-1d1c-48e7-9c05-5f6349b12e07.png">

Tác giả gợi ý là nên trải nghiệm game nên em sẽ chơi thử :V

Sau khi qua phần giới thiệu ta sẽ được yêu cầu giải câu hỏi trong file question.txt vừa xuất hiện và câu trả lời sẽ được đặt trong answer.txt,
trong file question.txt là một đoạn mã tính toán bằng ngôn ngữ Asembbly

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212962186-0192bda4-4ead-4dfa-916b-eb9f5fc9e2f5.png">

Ở đây thì em sẽ sữ dụng tool emu8086 để tính ra được giá trị của eax, tuy nhiên thì emu8086 chỉ chạy code 16bit nên em sẽ bỏ hết 'E' của Cx,Bx và Cx

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212964771-6214562e-42de-42e4-9b1d-ffb533440c38.png">

Hàng register bên trái là giá trị của Ax, Bx, Cx khi chưa tính toán

sau khi tiến hành tính toán ta thu được Ax =30

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212965137-f5443c09-38f6-41be-96e2-76a3b88ce621.png">

Nhập kết quả vào answer.txt và chạy lại game ta sẽ thu được file Memory mở bằng notepad ta sẽ có được đoạn flag dưới đây

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212965751-b09f81c5-4e4f-4710-a9c7-60f9f407deee.png">

Vì đoạn flag này chưa hoàn chỉnh và cũng có thể là cú lừa :V, nên em vào lại game lần nữa và đoạn hội thoại đã thay đổi, và tự bay ra ngoài menu game

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212967193-912bee0e-2157-44f4-b07d-d5725ee7046d.png">

Và sau khi nghiên cứu thì em nghĩ đoạn hội thoại phía sau sẽ có thêm thông tin về flag, do có kinh nghiệm dịch game Visual Novel ( chủ yếu là game... à mà thôi =)) ) nên em dùng tool UnRen (Dùng để giải nén file .rpa và tách .rpyc ra .rpy để lấy file text) 

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212969014-5e1bfbe9-7a2d-4906-bd4b-36a59514f725.png">

để Unren vào file game chung với file .exe

![image](https://user-images.githubusercontent.com/105163556/212969195-e6700b65-508c-4dcb-b169-502720acc2e8.png)

Gõ lệnh 1 dùng để giải nén file .rpa

![image](https://user-images.githubusercontent.com/105163556/212969343-7e8481ac-c1ca-4bc8-9e12-b6a52b3396e9.png)



Gõ lệnh 2 dùng để tách file .rpyc ra .rpy

![image](https://user-images.githubusercontent.com/105163556/212970078-e17c1b61-f86c-4226-ab87-3288a9517e33.png)

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212970315-4e2569cc-6a5e-408e-b028-5e701aa93ff7.png">

Mở file script để xem hết hội thoại của game, và em tìm được gợi ý của tác giả

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212970784-e7859ae2-0b89-427d-b7e3-a53f81ab0244.png">

Vâng ''thuật toán Chinese algorithm'' nhưng thật ra chỉ cần đổi từ hexadecimal sang byte là sẽ thu được flag, à nhớ bỏ '0x' :3 

>flag KCSC{W3llC0m3_T0_Our_D0k1_d0ki_Club!!!}



## Find me
> ĐỀ BÀI: Find mee in C Diskk 

đề bài có từ khóa 'find' nên em nghĩ flag sẽ nằm trong source, nên em dùng Detect it easy để xác định file trước

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212975016-8f299232-3123-4d21-8b2f-c49ce02dcfc2.png">

Và file được viết bằng python và đã được Packet nên ta sẽ tiến hành giải nén, ở đây em sữ dụng PyInstaller Extractor

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212976028-cfcd38f8-f099-4807-a1e7-a216395578ad.png">

ta thu được file source đã extracted


<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212976875-50a2e47c-977b-44b6-a41a-8682cad34c69.png">

                                                                                                                                        
mở file kéo xuống thì em thấy souce nên em cat thẳng vào nó và thu được đoạn flag :V

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212977065-51bb34e0-950c-4578-9c2d-3aa4d44c0985.png">


<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212976498-8eebbf31-2f74-49ce-ae97-922c4bceef1b.png">

>flag KCSC{T3t_n4y_4nh_kh0ng_th3m_d0t_ph4o_V1_ti3ng_cu0i_3m_r0n_r4_l0ng_4nh_r0i!}



## Antidebug

> ĐỀ BÀI: Can you help me get output of ENC(0xAB12DF34, 0x7B, 0x2D, 0x43) và file .asm

đề bài là câu lệnh gọi hàm và kèo theo file .asm, khi mở file lên là một hàm nên e nghĩ kia là các parameter và nhiệm vụ là từ parameter đó thực thi xem input là gì

```
void __cdecl ENC(int a1, int a2, int a3, int a4)

push    ebp
mov     ebp, esp
mov     eax, [ebp+0Ch]
add     eax, [ebp+10h]
add     eax, [ebp+8]
mov     ecx, [ebp+14h]
add     ecx, 0Ah
xor     ecx, [ebp+8]
add     eax, ecx
xor     eax, [ebp+8]
push    eax             ; char
push    offset Format   ; "0x%x"
call    printf
add     esp, 8
pop     ebp
retn
```

chú ý vị trí của các parameter:
ebp+8 = a1; ebp+0Ch = a2; ebp+10h = a3; ebp+14h = a4 với a1, a2, a3, a4 lần lược là 0xAB12DF34, 0x7B, 0x2D, 0x43

mov     eax, [ebp+0Ch] ; có nghĩa là dịch giá trị của a2(ebp+0Ch) vào eax
...
add     eax, [ebp+10h] ; cộng eax với a3(ebp+10h) và sau đó lưu vào eax
...
xor     ecx, [ebp+8] ; xor giá trị ecx với a1(ebp+8) và lưu vào ecx
như vậy đoạn code có thể dịch lại sang c như sau

```
int result,shadow;
result = a1 + a2 + a3;
shadow = (a4 + 0xA) ^ a1; 
result = result + shadow;
result = result ^ a1; 
printf("0x%x", result);
```
Chú ý rằng:
add eax, ecx ; Cộng eax + ecx = 0xab12dfdc + 0xab12df79
eax = 0x15625bf55 -> đồng thời eax chỉ mang 4 byte nên sẽ có giá trị thực là eax = 0x5625bf55

như vậy flag là KCSC{0xfd376061}



## Merger XOR
Trước tiên, đề bài cho ta 2 file

<img width="533" alt="image" src="https://user-images.githubusercontent.com/105163556/218100821-4b68ae09-d33c-46b4-841b-a6b9ea7df923.png">

Một file code C và một file text

<img width="533" alt="image" src="https://user-images.githubusercontent.com/105163556/218101028-99fda76e-c0d4-4a3f-b79a-f433303d06a0.png">


<img width="533" alt="image" src="https://user-images.githubusercontent.com/105163556/218101059-a5bb9ca3-0e90-4be7-8e3f-26bfe02722f5.png">

<img width="533" alt="image" src="https://user-images.githubusercontent.com/105163556/218101133-7306448b-623e-4831-a5d3-7b52b6e3e891.png">

Sau khi làm lại và đọc sơ các write up của bài này thì em hiểu là:
1. Trước tiên hàm được mã hóa bằng hàm flat nó sẽ chia đôi mỗi ký tự trong chuỗi Cipher, và với mỗi 4 bit cuối  của ký tự vừa chia xong ta sẽ Merger với 4 bit đầu của ký tự tiếp theo để tạo thành chuỗi mới rồi XOR với ký tự ban đầu:

<img width="533" alt="image" src="https://user-images.githubusercontent.com/105163556/218104698-3265df06-d413-4b72-a591-69c1448a43e1.png">

Và nó sẽ được chạy 5 lần để in ra kết quả giống trong Stdout.txt:

<img width="533" alt="image" src="https://user-images.githubusercontent.com/105163556/218105415-11b59725-6fc4-4ce2-8c5b-1053cf05e93f.png">

2. Cách giải: 
+ Với bài này ta sẽ tìm 2 byte input, nằm trong khoảng từ 0 - 255 encrypt sau đó so sánh với byte đầu trong Cipher nếu đúng thì quay lui hết các byte còn lại cho đến khi hết chuỗi, còn sai thì chọn lại cho đến khi đúng. 
+ Do ta đã biết mẫu của flag sẽ chứa chuỗi "KCSC" cho nên em sẽ viết code để kiếm chuỗi flag còn lại:

<img width="662" alt="image" src="https://user-images.githubusercontent.com/105163556/218120467-1ff2c3b7-c971-4a97-b8a8-61f76d7ad99e.png">


<img width="662" alt="image" src="https://user-images.githubusercontent.com/105163556/218120323-cec8903d-73fb-473a-8f4d-f1b6f928371d.png">

Và kết quả : <img width="662" alt="image" src="https://user-images.githubusercontent.com/105163556/218120525-8a8e3302-55a5-4d67-bc3b-e562a9f04258.png">

## Find Me làm lại:

Đầu tiên em dùng  dùng Detect it easy để xác định file trước

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212975016-8f299232-3123-4d21-8b2f-c49ce02dcfc2.png">

Và file được viết bằng python và đã được Packet nên ta sẽ tiến hành giải nén, ở đây em sữ dụng PyInstaller Extractor

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212976028-cfcd38f8-f099-4807-a1e7-a216395578ad.png">

ta thu được file source đã extracted


<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212976875-50a2e47c-977b-44b6-a41a-8682cad34c69.png">

Tiếp theo ta cần decomplyce file souce.pyc sang souce.py để có thể đọc được file
























