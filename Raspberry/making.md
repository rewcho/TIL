pip install sounddevice

python -m sounddevice

디폴트 출력 장치는 `<`나 `>`로 표시된다.

소비자 코드는 메인스레드에서 저장(record_customlen.py에서)

tell 매서드는 파일의 읽기쓰기를 하는 현재위치를 나타낸다.

seek 매서드는 위치를 이동시키는 것이다. seek(0)이면 파일 맨 앞으로 이동이다.
truncate 매서드는 현재위치에서부터 내용을 다 지운다.

소리 결정할 3요소
 1. samplerate
 2. depth(format)      1샘플 당 몇 bit(보통 16bit = 2 Bytes)   -> 소리크기에 최대값과 최소값을 설정한다.
 3. 

research 디렉토리에서 protoc object_detection/protos/*.proto --python_out=.
를 실행해주세요.





.access_token.txt를 만들 때 앞에 .을 붙인다.(히든파일)



별표는 신뢰할 수 있는 장비, 열쇠는 핑이 설정된 장비



블루투스 클라이언트에서 작동을 안 하면 sock.close()가 아닌 s.close()로 해보자.



블루투스 클라이언트에서 라인변경이 되어서 수신하는 이유는 리시브의 속도가 나무 빨라 수신 문자열이 끊김이 발생하기 때문이다. 이를 방지하기 위해서 딜레이를 줘야 한다.





라즈베리파이 웹 연결 stream port = 8081

etc/motion/motion.config에 들어가서

target_dir / var/lib/motion

export PATH=.:$PATH:/home/pi/.local/bin

리눅스는 현제 디렉토리를 찾기 않아서 ./command로 타이핑을 해야 했지만, 위의 명령어를 이용해서  command로 쳐도 된다.


ifconfig