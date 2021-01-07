# Project3-Reinforcement-Learning

Câu 1:
  Với hàm _init_
    Đầu tiên ta duyệt hết các giá trị của range(iterations), ta xét từng giá trị của từng state, mỗi state ta lại xét từng trạng thái
  nếu trạng thái là đích thì ta sẽ thoái ra và không có phần thưởng, còn nếu đây không phải đích thì ta sẽ tìm tổng phần thưởng mong 
  đợi lớn nhất của các hành động khác nhau 
  
  Với hàm _computeQValueFromValues_
    Ta có một hàm ở đây để có thể tính toán trạng thái chuyển đổi và xác suất là getTransitionStatesAndProbs(state, action). Đối với mỗi
    lần chuyển đổi được tính bằng tổng phần thưởng của việc chuyển đổi và trạng thái chuyển tiếp sau đó. Và chính giá trị này cung cấp cho
    q-value một cặp hành động và trạng thái (action,state) mà từ đó ta có thể tính được giá trị cần tìm
   
  Với hàm _computeActionFromValues_
    Ta đơn giản là chỉ khai báo một bộ đém stateAction để lưu q-value. Với mỗi cặp (Action,state) thì policy hoặc action chính là cho ta 
    biết được tổng phần thưởng mong đợi tốt nhất
    
 Câu 2:
   Với question2 ta chọn hai giá trị answerDiscount = 0.9 và answerNoise = 0 vì với noise = 0 thì mới có thể dễ dàng xác đinh đồng thời agent 
   sẽ luôn kế thúc khi có agent mới 
   
 Câu 3:
   Với Q3a các giá trị là:
        answerDiscount = 1
        answerNoise = 0.2
        answerLivingReward = -1  
   Vì ta muốn agent nhanh chóng di chuyển đến lối ra nhanh nhất có thể ta chọn phần thưởng phải âm để khiến nó thoát ra nhanh nhất
   Với Q3b các giá trị là:
        answerDiscount = 0.3
        answerNoise = 0.3
        answerLivingReward = 0
   Chọn như vậy để agent thoát bằng đường khác nhưng với con đường xa hơn
   Với Q3c các giá trị là:
        answerDiscount = 1
        answerNoise = 0.2
        answerLivingReward = -0.5
   Vì để cho agent có thể sống đủ lâu ở mức +10 bằng cách chấp nhận rủi ro nên phần thưởng cho lớn hơn câu 3a
   Với Q3d các giá trị là:
        answerDiscount = 1
        answerNoise = 0.2
        answerLivingReward = -0.03
   Vì không để agent chấp nhận rủi ro nên ta để phần thưởng có mức âm nhỏ hơn 3c
   Với Q3e các giá trị là:
        answerDiscount = 1
        answerNoise = 0.2
        answerLivingReward = 9999 
   Vì phần thưởng cho việc sống sót lớn hơn nhiều so với việc thoát ra nên nó sẽ không thoát ra nữa
   
Câu 4:
   Để giải quyết bài này với hàm _computeActionFromQValues_
        Ta lấy tât các trạng thái của hành động bằng hàm getLegalActions() với giá trị khởi đầu ta cho giá trị bằng 0 còn với các trạng thái khác thì 
   trả về giá trị tối đa của q-value trạng thái
   Còn hàm _computeActionFromQValues_
        Ý tưởng để tính toán ra được hành động tốt nhất để thực hiện trong một trạng thái như sau 
        
Câu 5:
   Với việc chọn ngẫu nhiên một action epsilon chỉ khi đánh giá được self.epsilon còn không sẽ trả về giá trị hành động của hàm computeActionFromQValues
   
Câu 6:
   Ta chọn các giá trị :
        answerEpsilon = 0.1
        answerLearningRate = 0.8
  Vì không thể tìm được con đường tối ưu đến 99%, 50 tập là quá nhỏ nên cần thêm để tìm kiếm
  
Câu 7:
   
        
   
   
   
   
    
    
