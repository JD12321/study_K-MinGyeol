# push
로컬 리포지토리(PC)에서 원격 리포지토리로 변경 사항을 올리는 것  
> ⚠️ push를 하기 위해선 원격 리포지토리에서 쓰기 권한을 갖고 있어야 한다.  
<br>

```
$ git push [<repository>] [<branch>]
```

`<repository>`
- push 할 리포지토리명을 지정한다

`<branch>`
- push 할 브랜치명을 지정한다  
  
```
💡 최초에 한 번만 저장소명과 브랜치명을 입력하고, 그 이후부터는 모든 인자를 생략 가능함
```
<br>

# pull
원격 리포지토리의 변경 사항을 로컬 리포지토리(PC)에 반영시키는 것  
<br>

### fetch
```
$ git fetch [<repository>]
```
원격 저장소의 정보를 로컬 저장소로 가져오는 역할을 수행한다.  

`<repository>`
- 변경사항을 가져올 리포지토리를 지정한다  
<br>

### merge
```
$ git merge [<commit>...]
```
변경된 정보를 로컬 저장소의 내용과 병합하는 역할을 수행한다.

`<commit>...`
- 합병할 브랜치를 지정한다
- `origin/main` 등과 같이 추가할 수 있음  
<br>

### fetch와 pull의 차이점
두 기능 모두 원격 저장소에서 로컬 리포지토리에 변경 사항을 가져온다는 점은 동일하다. 그러나, fetch의 경우 변경 사항을 가져만 올 뿐 병합을 진행하진 않고(=변경 사항을 적용시키진 않고), 사용자가 직접 merge를 하여 병합을 완료해야 한다.

반면, pull의 경우 변경 사항을 가져올 뿐만 아니라 자동으로 병합을 진행한다. 즉, pull은 fetch와 merge가 한꺼번에, 자동으로 진행된 것과 동일하다.  
<br>

### pull 사용하기
```
$ git pull [<repository>] [<branch>]
```

`<repository>`
- pull 할 리포지토리명을 지정한다

`<branch>`
- pull 할 브랜치명을 지정한다  