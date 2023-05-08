# Code Peer Review Templete

- 코더 : 박동원님 / 정선종님
- 리뷰어 : 김영원

---

# PRT(PeerReviewTemplate)

각 항목을 스스로 확인하고 체크하고 확인하여 작성한 코드에 적용하세요.

- [x] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
- [o] 주석을 보고 작성자의 코드가 이해되었나요?
- [o] 코드가 에러를 유발할 가능성이 있나요?
- [x] 코드 작성자가 코드를 제대로 이해하고 작성했나요? (직접 인터뷰해보기)
- [ ] 코드가 간결한가요?

---

# 예시

1. 코드의 작동 방식을 주석으로 기록합니다.

2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.

3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.
   
'''
import pprint

maze = [                #maze 리스트 생성
    [0, 1, 0, 0, 0],
    [0, 0, 0, 1, 0],
    [0, 1, 1, 0, 0],
    [0, 0, 1, 1, 0],
    [0, 0, 0, 0, 0]
]

turtles()
setup(250, 250)
clear()
goto(x, y)      #터틀

def solve_maze(x, y):               #0인지 1인지 판단하여 미로를 찾는 코드 1이라면 다음으로 넘어감 0이면 2로 바꿈
  solved_maze = maze
  while True:
    if 0 <= y < 4 and solved_maze[x][y+1] == 0:
      solved_maze[x][y] = 2
      y += 1
      forward(20)
    elif 0 <= x < 4 and solved_maze[x+1][y] == 0:
      solved_maze[x][y] = 2
      x += 1
      right(90)
      forward(20)
      left(90)
    elif 0 < x < 4 and solved_maze[x-1][y] == 0:
      solved_maze[x][y] = 2
      x -= 1
      left(90)
      forward(20)
      right(90)
    elif 0 < y < 4 and solved_maze[x][y-1] == 0:
      solved_maze[x][y] = 2
      y -= 1
      left(180)
      forward(20)
      right(180)
    else:
      print("미로를 찾을 수 없습니다")
    # pprint.pprint(solve_maze)
    # print(x, y)

    if x == 4 and y == 4:
      solved_maze[x][y] = 2
      print("미로를 찾았습니다")
      pprint.pprint(solved_maze)
      break
'''
---

# 참고 링크 및 코드 개선 여부...

```python
#
#많이 배우고 갑니다..
#선종님 화이팅
#
```