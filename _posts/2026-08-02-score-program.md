---
layout: post
title: "이름과 점수 파일 저장 프로그램"
date: 2026-08-01
---

파이썬을 이용하여 사용자로부터 이름과 점수를 입력받고 파일에 저장하는 실습 코드입니다.

```python
def save_scores():
    filename = "scores.txt"
    with open(filename, "a", encoding="utf-8") as file:
        while True:
            print("********************")
            name = input("이름을 입력하세요: ")
            score = input("점수을 입력하세요: ")
            file.write(f"{name}:{score}\n")
            cont = input("계속하시겠습니까?(y/n): ")
            if cont.lower() == 'n':
                break
    print("-- 파일내용 --")
    with open(filename, "r", encoding="utf-8") as file:
        print(file.read().strip())
if __name__ == "__main__":
    save_scores()
