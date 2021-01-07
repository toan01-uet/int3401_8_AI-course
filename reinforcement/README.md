# 2021l_INT3401_8_Reinforcement_Learning
Solutions for Pacman Project 2021l_INT3401_8 courses of UET-VNU

## Question 1: Value iteration

  **Hàm tính value**: với mỗi action trong mỗi state tính ra tổng điểm rồi lấy giá trị lớn nhất tương ứng với action.
  
  **Hàm computeQValueFromValues**: tương tự hàm trên nhưng chỉ tính value của từng cặp state, action, không lấy max

  **Hàm computeActionFromValues**: trả về hành động có điểm số tốt nhất
  

## Question 2 : Bridge Crossing Analysis
Thay tham số noise từ 0.2 về 0

## Question 3: Policies

    def question3a():
        answerDiscount = 0.9
        answerNoise = 0.1
        answerLivingReward = -5.0
        return answerDiscount, answerNoise, answerLivingReward
        # If not possible, return 'NOT POSSIBLE'


    def question3b():
        answerDiscount = 0.3
        answerNoise = 0.3
        answerLivingReward = 0
        return answerDiscount, answerNoise, answerLivingReward
        # If not possible, return 'NOT POSSIBLE'


    def question3c():
        answerDiscount = 0.9
        answerNoise = 0
        answerLivingReward = 0
        return answerDiscount, answerNoise, answerLivingReward
        # If not possible, return 'NOT POSSIBLE'


    def question3d():
        answerDiscount = 0.9
        answerNoise = 0.2
        answerLivingReward = 0
        return answerDiscount, answerNoise, answerLivingReward
        # If not possible, return 'NOT POSSIBLE'


    def question3e():
        answerDiscount = 0.9
        answerNoise = 0.2
        answerLivingReward = 11
        return answerDiscount, answerNoise, answerLivingReward

## Question 4: Q-learning
Tương tự câu 1 ngoại trừ hàm update.


