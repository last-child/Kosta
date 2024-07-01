<h2>버전 관리</h2>

<br>   

```bash
$ mkdir workspace

$ cd workspace

$ git init
```

<br>   

<p>workspace 폴더에 <b>git 저장소</b>가 생성되었습니다. 이제 해당 폴더에서 git을 통해 버전을 관리할 수 있습니다.</p>

<br>   
<br>   

```bash
$ echo "나의 살던 고향은 꽃피는 산골" > spring.txt

$ git add spring.txt

$ git commit -m "spring song"
```

<br>   

<p>작업 공간에서 특정 파일이 변경되었습니다. <b>git add</b> 명령어를 사용하면 해당 파일이 스테이징 영역에 추가됩니다.</p>
<p><b>스테이징 영역</b>은 다음 스냅샷에 어떤 변경 사항을 반영할지 검토하는 임시 공간입니다.</p>

<br>   

<p><b>git commit</b> 명령어를 사용하면 현재 스테이징 영역에 올라온 파일들이 스냅샷으로 기록됩니다.</p>
<p>이 스냅샷들은 <b>로컬 저장소</b>에 저장되며, 프로젝트의 버전을 관리하는 데 사용됩니다.</p>
