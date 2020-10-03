# int3401_8_AI-course
##Dạng bài tìm kiếm trong đồ thị:
	- Có input: là các node trong đồ thị, mỗi node thì có thông tin của (vị trí, hướng đi, và chi phí ) ví dụ như ([10, 10], ['South', 'North', 'West', 'West', ...],3).
	- output : là các hướng đi đến được đích (goalState).
	- chiến thuật của thuật toán (dfs,bfs,ucs,a*).
##Giải thuật cho bài toán :
	1.khởi tạo điểm bắt đầu (sử dụng state ở problem)
	2.danh sách các điểm đã đi qua (tránh bị lặp)
	3.vòng lặp đến khi đi đến được đích
		nếu node hiện tại đang chứa điểm đích thì đưa ra hướng đi tương ứng của node
		nếu node chưa đi qua:
			mở rộng nó theo chiến thuật của thuật toán
			thêm node mở rộng vào danh sách các điểm đi qua
###1. DFS
- Chiến thuật: đi đến xa nhất theo từng nhánh, khi nhánh duyệt hết thì lùi về để tìm là duyệt những nhánh tiếp theo. Do đó dùng cấu trúc stack để lưu trữ các node đã duyệt (fringe).
- Khởi tạo các giá trị: 
	+ node khởi đầu startNode = (problem.getStartState(),[],0)
	+ fringe = stack()
	push startNode vào fringe
	+ danh sách các node đã qua 
-Vòng lặp, lặp đến khi fringe rỗng:
	+ lấy node vừa được push vào fringe: node = fringe.pop()
	+ kiểm tra state của node này (node[0]) có phải đích hay không, nếu phải thì trả về hướng đi (node[1])
	+ mở rộng các node xung quanh vị trí (node[0]) đang sét, node này chưa được đi qua: push các node mở rộng vào fringe với hướng đi của node là (hướng node[1] + hướng của  nút mở rộng).
###2. BFS
- Chiến thuật: từ đỉnh hoặc node ban đầu,xác định và duyệt các đỉnh kề phần xét. Do đó dùng cấu trúc Queue để lưu trữ các node đã duyệt (fringe).
- Phần còn lại tương tự DFS
###3. UCS
- Chiến thuật: mở rộng đến node có chi phí (cost) nhỏ nhất do đó fringe lưu dưới dạng Piority Queue với piority = cost (min).
- Các phần còn lại tương tự : chỉ riêng phần mở rộng: phải cập nhập giá mới (giá của node mới pop + giá của node mở rộng)
###4. A*
- Chiến thuật: tương tự UCS nhưng cách tính cost ở đây là f = g + h với
	+ g là cost của node hiện tại đến node khác
	+ h là heuristic value, giá trị xấp xỉ đến node đích.
- Tương tự UCS, riêng phần cost giá trị ưu tiên thì phải là f

###5. Finding All the Corners
- hàm getStartState trả về trạng thái bắt bầu là 1 tuple gồm có:
	+ Ví trí điểm bắt đầu 
	+ Toạ độ 4 góc
- hàm kiểm tra đích isGoalState: nếu danh sách 4 toạ độ là rỗng thì trả về True
- getSuccessor : successor (state,action,cost)
	kiểm tra va chạm tường
	nếu không va chạm:
		kiểm tra vị trí tiếp theo có phải là vịt trí của 4 góc hay không, nếu phải thì xoá góc đó trong danh sách góc.
		và cập nhật successor
	
