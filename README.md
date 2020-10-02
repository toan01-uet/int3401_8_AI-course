# int3401_8_AI-course
1. DFS
lấy trạng thái bắt đầu -> cho vào stack -> duyệt đến khi stack
trống thì thôi -> kiểm tra nút được pop ra xem có phải GOALSTATE
hay ko nếu có thì đưa ra nút này, nếu không thì kiểm tra node này
đã đi qua (visited) chưa? có rồi thì bỏ qua, còn chưa có trong visited
thì thêm vào fringe với action + [act], [act] để cho thành list.
3.UCS
duyệt theo piority queue, piority = cost (min).
4. cornersProblem
	init: khoi tao gia tri bat dau
	bat dau man thi la tuple gom co (vi tri pacman, goc)
	ket thuc neu cac goc trong tuple 0 con goc nao
	lay toa do, kiem tra va cham tuong:
		neu khong va cham tuong:
			kt vi tri tiep theo co phai GOC hay ko:
				xoa GOC do trong tuple
			neu ko thi them vao successor
