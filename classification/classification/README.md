## bai 1: cài perceptron trong file perceptron.py
- Trong mỗi lần duyệt thì update weight dựa theo các classfication errors
- CT:wy=wy+f ,wy′=wy′−f trong đó y là mylable,y' là trọng số của lable, f là featurebetter

## bai 2: display 100 pixel vowi trong so lon nhat
- hoàn thiện hàm findhighWeifeatures trả về 100 features của weight cao nhất -sd câu lệnh: 
- py -2  dataClassifier.py -c perceptron -w 
- trong câu hỏi để hiển thị 100 pixel với weight lớn nhất 
- so sánh ta đc a là kết quả và trả lời trong answer.py
## bai 3 cai bo phan lop mira 

## bai 4: cai feature moi : thiết kế và cải thiện features hiện có các feature đặc biệt:
- được thêm vào là số khoảng trắng trên dữ liệu đầu vào. Viết thêm hàm DFS() để đánh dấu các khoảng trắng. Số khoảng trắng với các kí tự số sẽ là 1, 2 và 3 tương ứng với 3 features được thêm vào.

## bai 5 : perceptron ai
- Pacman Behavioral Cloning Tương tự như bài 1,tuy nhiên vì sử dụng chung vector trọng số cho tất cả các nhãn( các hành động tương ứng với 1 trạng thái của pacman) nên khi cập nhật sẽ đồng thời cộng và trừ vào vector trọng số đó. công thức cập nhật là:
    w=w+f(s,a) # Correct action
    w=w−f(s,a′)  # Guessed action
## bai 6: thiết kế feature của riêng mình 
các feature chúng ta có thể sử dụng: win, lose, score,...
## KET QUA:

Finished at 8:44:08
==================
Question q1: 4/4
Question q2: 1/1
Question q3: 6/6
Question q4: 6/6
Question q5: 4/4
Question q6: 4/4
------------------
Total: 25/25