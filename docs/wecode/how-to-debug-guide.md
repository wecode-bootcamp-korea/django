# 1. iPDB를 설치한다
```pip install ipdp```

# 2. 브레이크 포인트를 걸 시작점을 찾는다

```
ag runserver

# 검색 결과물 중에 가장 그럴싸한 위치를 찾아서 브레이크 포인트를 건다
import ipdb as pdb
pdb.set_trace()
```

# 3. 해당 브레이크 포인트를 실행 시킬수 있는 유닛 테스트를 찾거나 만든다
```
./runtests.py --parallel=1 staticfiles_tests.test_management
```

# 4. 브레이크 포인트가 실행되면 하나 하나 step 혹은 continue 혹은 next (혹은 여러 다양한 다른 pdb 커맨드)를 사용해서 코드의 실행 경로를 기록한다.

# 5. 기록한 경로를 markdown format으로 파일을 작성해서 docs/wecode 디렉토리 아래 커밋 한다.
