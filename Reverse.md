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


## AntiDebug


> ĐỀ BÀI:Can you help me get output of

> ENC(0xAB12DF34, 0x7B, 0x2D, 0x43)

> Flag form: KCSC, for example : KCSC{0xdeadbeef}

Ta sẽ mở file bằng SASM và thu được đoạn code bằng asm

<img width="700" alt="image" src="https://user-images.githubusercontent.com/105163556/212977553-20bfec2f-2ca7-431c-aa57-8acbe4c339bb.png">

Và em sẽ dịch đoạn code này sang C cho dễ hiểu











