---
layout: page
title: "Projects"
permalink: /projects/
comments: false
---

### 실습 - 둘레와 넓이를 계산하기

이 프로젝트는 사용자가 사각형과 원 중 하나를 선택하면, 각 도형에 맞는 수를 입력받아 둘레와 넓이를 함수로 계산해 주는 프로그램입니다.

```python
# 사각형 계산 함수
def calc_rectangle(w, h):
    perimeter = 2 * (w + h)
    area = w * h
    return perimeter, area

# 원 계산 함수
def calc_circle(r):
    pi = 3.14
    perimeter = 2 * pi * r
    area = pi * (r ** 2)
    return perimeter, area

def main():
    while True:
        choice = input("1:사각형, 2:원 , 3:종료>>")
        
        if choice == '1':
            num1 = float(input("첫번째 수를 입력하세요: "))
            num2 = float(input("두번째 수를 입력하세요: "))
            p, a = calc_rectangle(num1, num2)
            print(f"사각형의 둘레는{p:.2f}, 넓이는{a:.2f} 입니다")
            
        elif choice == '2':
            radius = float(input("반지름을 입력하세요: "))
            p, a = calc_circle(radius)
            print(f"원의 둘레는{p:.2f}, 넓이는{a:.2f} 입니다")
            
        elif choice == '3':
            break
            
        else:
            print("잘못 입력하였습니다.")

if __name__ == "__main__":
    main()
