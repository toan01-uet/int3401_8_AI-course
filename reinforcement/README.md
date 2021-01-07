## Result 

==================
    Question q1: 6/6
    Question q2: 1/1
    Question q3: 5/5
    Question q4: 5/5
    Question q5: 3/3
    Question q6: 1/1
    Question q7: 1/1
    Question q8: 3/3
------------------
Total: 25/25


## Question 1: Value iteration

Dùng công thức  MDPs

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

## Question 4 vs 5: 
Áp dụng công thức của thuật toán Q-Learning và Q-Learning with Epsilon.
## Question 6:
Kể cả khi epsilon ~1, khả năng đi được tới ô +10 một cách ngẫu nhiên ~0.1%. Nếu chỉ train agent 50 lần, thì khả năng đi qua được cầu của agent là không có.
## Question 8:
Sử dụng Approximate Q-Learning.


