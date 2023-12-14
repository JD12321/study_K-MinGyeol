# clone
원격 저장소(GitHub, BitBucket 등)를 로컬 환경(PC)에 복제하는 것

> 💡 공개된 저장소는 소유와 관계없이 누구나 복제 가능  
<br>

### 원격 저장소 복제하기
```
$ git clone <repository> [<directory>]
```
`<repository>`
- 복사할 원격 리포지토리 주소를 지정함

`<directory>`
- 복사한 리포지토리 내용을 담을 폴더나 경로를 지정함
- 이 인자에 아무런 값을 넣지 않을 경우 현재 터미널 경로에 원격 리포지토리의 이름과 동일한 폴더가 생성됨  
<br>

### 원격 저장소 관리
```
$ git remote [-v | --verbose]
```
저장소의 이름을 확인한다.

`--verbose`, `-v`
- 원격 리포지토리의 이름과 URL 등 여러 정보를 상세하게 표시한다  
<br>

```
$ git remote add <name> <URL>
```
`<name>`의 이름으로 `<URL>` 주소에 해당하는 원격 저장소를 추가한다.  
<br>

```
$ git remote show <name>
```
원격 저장소 `<name>`에 대한 정보를 확인한다.  
<br>

```
$ git remote rename <old> <new>
```
원격 저장소 `<old>`의 이름을 `<new>`으(로) 변경한다.  
<br>

```
$ git remote remove <name>
```
원격 저장소 `<name>`을 삭제한다.