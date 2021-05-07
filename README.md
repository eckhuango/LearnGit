# **Software Engineering HW#2**

20182593 김영빈  
Github repository URL : https://github.com/eckhuango/LearnGit

<hr/>
<br>

**1일차 :**  

과제를 부여받음. 현재 과제 폴더에는 과제를 작성할 markdown파일 1개(first.md)가 들어있으며, 문서에는 아무런 내용도 적혀있지 않다고 하자.  
과제의 수행을 위해서 버전관리 프로그램인 git을 이용하기로 한다. 먼저 git bash에서 cd명령어를 이용하여 프로젝트 폴더까지 이동한다.  

**` $ cd C:/Users/home/desktop/markdown `**

이 프로젝트 폴더에서 git을 사용하기 위하여 git bash창에 다음과 같은 명령을 입력한다.

# $ git init

 이 명령어를 사용하여 프로젝트 폴더에 git폴더를 생성하여 git을 사용할 수 있게 한다. 이 명령어는 git을 사용할 수 있게 하는 명령어이다. 이 명령어를 사용하면 프로젝트 폴더 내에 .git이라는 숨겨진 폴더가 생성되게 된다. 이후 이 폴더를 기반으로 하여 git이 동작하게 된다.

![image_git](https://user-images.githubusercontent.com/81168401/117405084-06b48f00-af46-11eb-929c-d73474ed15f7.png)



# $ git config

또한, git 사용을 위해서는 git 사용자의 정보를 입력해 주어야 한다.

**` $ git config --global user.name "kimyoungbin" `**  
**` $ git config --global user.email "bsh51515@naver.com" `**

위와 같이 config 명령어는 git의 사용 환경을 변경/설정하는 역할을 한다. --global옵션으로 설정하게 되면 그 설정은 딱 한번만 하면 된다. 만약 프로젝트마다 다른 이름/email을 사용하고 싶다면, --global 옵션을 빼주면 된다. 또한, 설정이 잘 되었는지 확인하려면 ` $ git config --list ` 를 입력해서 확인할 수 있다.

git 환경을 구축했으니 다음으로는 원격 저장소 github도 사용해보자. 웹호스팅 서비스를 지원하는 github는 협업 프로젝트를 진행하는 것을 돕는다. 현재 프로젝트 폴더는 아무런 원격 저장소와 연결되어 있지 않은데, 원격 저장소를 연결하면 소스의 공유와 협업을 보다 수월하게 할 수 있다.
<br><br><br>


# $ git remote
먼저, 원격 저장소를 컨트롤하기 위한 명령어를 입력해보자.

![git_remote](https://user-images.githubusercontent.com/81168401/117405107-0a481600-af46-11eb-8753-551832b56da4.png)

 git remote 명령어는 현재 프로젝트 파일과 연결된 원격 저장소의 정보를 보여준다. 현재 프로젝트 파일은 아무런 원격 저장소와의 연결도 되어있지 않으므로 아무것도 나오지 않는 것을 확인할 수 있다.  

 이제 원격 저장소와의 연결을 위해 다음과 같이 git remote add명령어를 입력해보자.

**` $ git remote add origin https://github.com/eckhuango/LearnGit.git `**  
**` $ git branch -M main`**  
**` $ git push -u origin main `**  

이렇게 입력하면 프로젝트 폴더의 원격 저장소가 해당 github.com 주소로 설정된다.  
(branch와 push에 대해서는 나중에 설명하도록 하겠다.)

![git_remote_origin](https://user-images.githubusercontent.com/81168401/117405109-0a481600-af46-11eb-94e9-2739d66b70ae.png)
 
 설정이 끝나고 remote 명령어 재입력시 origin이라는 원격 저장소의 정보가 나오는 것을 확인할 수 있다.  

이제 github와의 연동이 끝났으니 본격적으로 파일을 작업하자. 일단 글의 느낌정도만 잡기 위해서 제목과 첫 단락정도만 작성한 후 컴퓨터에 저장했다. 이때 이 작업으로 인해 변화한 내용을 git에서 확인해볼 수 있다.
<br><br><br>

# $ git status

![git_status](https://user-images.githubusercontent.com/81168401/117405115-0b794300-af46-11eb-9072-8d5ecb257f12.png)

 status 명령어를 이용하면 현재 git의 상태를 알 수 있다. first.md파일이 not staged되었으며, commit해야 한다고 나와있다.  
 이 말인 즉슨, 프로젝트 폴더에 있는 first.md파일은 수정되어 저장되었지만, 아직 변경사항이 git에는 반영되지 않았다는 뜻이다. 이제 파일의 변경사항을 git에 반영해보자.
<br><br><br>

# $ git add 

add 명령어는 파일의 추적을 지시한다. git에게 버전 관리를 맡기기 위해서는 파일의 상태를 넘겨주어야 하는데, git add <파일명> 과 같이 쓰게 되면 git은 그 파일을 추적하여 변경사항을 담는다. 이때, `$ git add -A`와 같이 사용하면 프로젝트 폴더 내의 모든 파일들을 추적한다. 변경점을 알고 싶다면, 앞서 배운대로 git status를 다시 사용해보자.

![git_status_2](https://user-images.githubusercontent.com/81168401/117405117-0c11d980-af46-11eb-8b30-ea67c249fcdf.png)

 ‘Changes not staged for commit'의 항목이 사라지고 'Changes to be committed' 항목만이 남았다. 쉽게 말하자면, 이제 git이 변경사항을 모두 알아냈다는 것을 의미한다. 
<br><br><br>

# $ git commit

이제 git이 인식한 변경사항들을 commit하게 하면 된다. commit은 파일 및 폴더의 추가/변경을 저장소에 기록하는 것을 의미한다. 앞서 add를 통해서 git은 변경사항을 인식했지만 그것을 아직 저장하지는 않았다. commit을 통해 git은 변경사항을 ’그 당시의 폴더의 모습‘의 형태로 저장한다. 

![git_commit](https://user-images.githubusercontent.com/81168401/117405092-07e5bc00-af46-11eb-82f8-3243266f144b.png)

일반적으로 ’git commit‘ 이라고 입력하면, git은 commit 내용에 관한 설명을 추가할 것을 요구하면서 vi에디터라는 리눅스 편집기로 화면이 넘어가게 된다. 이 과정을 생략하려면, `-m` 옵션을 추가하면 뒤에 설명을 바로 추가해 줄 수 있다. 이제 commit이 잘 되었는지 확인해 보자.
<br><br><br>

# $ git log 

log 명령어를 이용하면 git에 저장한 commit들을 확인할 수 있다.  

![git_log](https://user-images.githubusercontent.com/81168401/117405093-087e5280-af46-11eb-8026-4e79854f624c.png)

git log의 정렬은 시간순으로 위-아래로 배치된다. 위의 사진에서 새롭게 commit된 파일이 log의 맨 위에 나타나 있는 것을 볼 수 있다. 또한 commit들은 각각 고유한 해쉬 값을 가지는데, 이것은 git의 분산 버전 관리 시스템이라는 특성과 연결된다. commit은 말 그대로 버전의 역할을 하는데, 고유 해쉬값을 할당하면 온/오프라인 상관없이 버전 전환이 가능하다. 
<br><br>
이제 마지막으로 저장된 버전을 원격 저장소에 저장해보자. 개발을 위해서는 여러 개발자들이 협업해야 하는 경우가 많고, 개발 중 테스트와 같은 활동을 위해서는 여러명이 main폴더를 공유해야 하는 필요성이 있는데, 클라우드나 메일을 이용해서 소스 공유와 개발을 하는 과정은 매우 번거롭다. 이때 git과 원격 저장소를 이용하면 ’버전 관리된 소스‘를 쉽게 공유할 수 있다. 
<br><br><br>

# $ git push origin main

push <저장소명> <branch명> 을 이용하면 지금까지 수정/add/commit한 프로젝트 폴더의 정보가 원격 저장소에 저장된다. 처음 remote 명령어를 이용하여 원격저장소를 추가할 때 origin이라는 원격 github 저장소가 등록되었고, git의 기본 branch는 main 브랜치이므로, 이렇게 추가하면 지금까지 수정/add/commit한 프로젝트들이 원격 저장소에 올라가게 된다.

![git_push](https://user-images.githubusercontent.com/81168401/117405102-0916e900-af46-11eb-9627-297e372ceaf2.png) 
push에 성공한 모습.

![github_afterpush](https://user-images.githubusercontent.com/81168401/117405120-0caa7000-af46-11eb-968e-a7bdd8f76641.png)

이렇게 원격 저장소에서도 “Day1_fin”이라고 commit하여 저장한 파일의 모습을 확인할 수 있다.
<br><br><br>


# $ git pull origin main
**2일차 :**  

오늘도 어제 작업한 내용을 이어서 작업할 것이다. 그런데, 내가 어제 프로젝트 파일의 작업을 마치고 원격 저장소에 올려놓은 시점과는 달리, 지금은 원격 저장소에 어제와는 다르게 어떤 변화가 발생했을지 알 수 없다. 따라서 원격 저장소의 작업 내역이 나의 로컬 작업내용과 다를 수 있다. 이 상태로 나의 로컬 작업을 끝내고 push하게 되면, 원격 저장소의 내용과 충돌이 발생할 수 있다. 그것을 방지하기 위하여, pull이라는 명령어를 사용해야 한다.

pull <저장소명> <branch명>을 입력하면, 원격 저장소의 내용을 해당 브랜치로 가져올 수 있다. git의 기본 branch는 main이고, 앞서 말했듯이 원격 github 저장소의 이름이 origin이므로 위와 같이 입력하면 나의 git이 원격 저장소에 맞게 최신화될 것이다.


![git_pull](https://user-images.githubusercontent.com/81168401/117405098-0916e900-af46-11eb-85a1-74c6f9880719.png)

Already up to date‘라는 말을 보아 밤 사이에 아무도 내 과제를 건드리지 않았다는 것을 알 수 있다. 이것은 원격 저장소에 추가적인 push가 없었음을 의미한다. 하지만 (반드시 그러리라는 보장이 없으니) 로컬 저장소의 내용을 수정하기 전에는 반드시 pull해서 최신화해주는 습관을 들이도록 하자.

**- 앞서 말한 pull-add-commit-push라는 4단계 과정이 git+github 이용의 기본적인 cycle이다.**
<br><br><br>

# $ git reset


이번에는 문서를 잘못 수정한 경우에 복구하는 방법을 알아보자.  

소프트웨어공학 과제 파일에 실수로 공학수학 방정식 내용을 덮어넣은 채로 commit해 버렸다고 가정하자. 이때는 git의 reset 명령어를 사용할 수 있다. ` git reset <옵션> <커밋 해쉬값> ` 은 컴퓨터의 시간 백업과 비슷하게 돌아가려는 버전의 커밋으로 되돌려 놓을 수 있다. reset에는 3가지 옵션(hard, soft, mixed)가 있는데 hard는 돌아가려는 이력 이후의 내용을 모두 지우는것, 나머지 2개는 일부 남아있는 것을 의미한다. 나는 공학수학의 내용은 모두 지우기 위해 --hard 옵션을 사용했다.  

![git_reset_hard](https://user-images.githubusercontent.com/81168401/117405110-0ae0ac80-af46-11eb-96bf-78c942bac1bc.png)  
1일차에 완료한 Day1_fin 뒤에 Hermitian transpose라는 정체모를 커밋이 추가되어 있다.
![git_reset_hard2](https://user-images.githubusercontent.com/81168401/117405112-0ae0ac80-af46-11eb-94dc-0f8bc7e59e27.png)   
reset을 하자 제어가 Day1_fin으로 넘어왔다는 안내가 나온다.  
![git_reset_hard3](https://user-images.githubusercontent.com/81168401/117405113-0b794300-af46-11eb-8904-dc30cc7bfca8.png)  
log를 확인해보면 정상적으로 파일이 해당 커밋의 상태로 되돌아갔음을 알 수 있다.
<br><br><br>


# $ git branch/checkout <branch명>


**3일차 :**    

나는 4장까지 first.md 파일로 저장하고 5장부터는 second.md 파일에 나누어 저장할 계획이었다. 그래서 오늘은 지난 내역에 이어 4장까지 작업을 마친 후, 다음 작업을 위해 second.md 파일을 생성하고 원격 저장소에 push했다.  
그런데 갑자기 친구가 내 과제를 하고 싶다고 한다. 그렇다고 해서 내 과제의 원본을 맡기기는 꺼림칙하니 일단 결과물을 보고 반영하기로 했다. 먼저 branch 명령어를 이용해서 친구에게 맡길 new_idea라는 branch를 만들고, checkout 명령어로 그 branch로 이동했다.
그 후에는 친구에게 그 branch에서 파일을 수정하고 add, commit, push하게 하면 된다.

![git_branch_checkout](https://user-images.githubusercontent.com/81168401/117405080-03b99e80-af46-11eb-9221-bdf2bba45413.png) 

![git_branch_checkout2](https://user-images.githubusercontent.com/81168401/117405086-06b48f00-af46-11eb-99d4-cdc779e97964.png)

 -> 중간에 main을 push했을때 나오는 문구로 보아 main에는 변화가 없음을 알 수 있다.

앞서 얘기했듯이, 개발자들은 협업을 할때 동일한 소스코드를 함께 공유하고 관리하게 된다. 그런데 여러 사람이 동일한 소스코드를 기반으로 서로 다른 작업을 할 때에는 각각 서로 다른 버전의 코드가 만들어지게 된다. 이럴 때 사용되는 기능이 branch이다. 앞서 얘기했듯 git의 기본 branch는 main이지만, [ git branch <branch명>] 명령어를 사용하면 새로운 branch를 추가할 수 있다. 또한, 특정 branch를 사용하여 작업을 수행하기 위해서, [ git checkout <branch명>] 과 같이 checkout 명령어를 사용할 수 있다. 그렇게 하면 명시한 branch로 제어가 이동하게 된다. 또한, `branch -d`옵션을 주면 branch를 삭제할 수 있고, `checkout -b` 옵션을 주면 branch후 바로 checkout이 되게 만들수도 있다.
<br><br>

# $ git merge <branch명>

생각보다 친구가 작업한 내용이 아주 만족스러워서 친구가 작성한 내용을 그대로 사용하기로 했다. 그런데 문제는 지금 친구가 작성한 내용은 new_idea 브랜치에 있는데, main 브랜치로 작업을 합친 후 이어나가고 싶다는 것이다. 이 때 필요한 것이 merge 명령어이다.

![git_merge](https://user-images.githubusercontent.com/81168401/117405095-087e5280-af46-11eb-8a49-ed6d70f016ba.png)

main branch에 new_idea branch를 병합하고 싶은 것이니, 먼저 checkout을 통해서 main으로 제어를 이동시킨 뒤 merge명령을 실행하였다. 즉, merge는 명시해준 branch를 현재 제어가 위치한 branch로 병합하라는 것을 의미한다. 이후 main branch에서 second.md파일을 확인해보면 정상적으로 병합된 것을 확인할 수 있다.

이제 필요없게된 new_idea branch는 `branch -d` 명령어로 삭제해주자.
<br><br>


# $ git clone 

**4일차 :**  
오늘은 일이 생겨서 원래 작업하던 데스크톱이 아니라 노트북을 이용하여 과제를 이어서 해야 한다고 하자. 그런데 노트북에는 과제 자료가 따로 담겨있지 않다. 이때 clone 명령어를 사용하면 과제를 원격 저장소에서 받아와서 이용할 수 있다.

![git_clone](https://user-images.githubusercontent.com/81168401/117405089-074d2580-af46-11eb-922c-8a4fa0689630.png)   
![git_clone2](https://user-images.githubusercontent.com/81168401/117405090-07e5bc00-af46-11eb-9fe0-9ad12ce05c97.png) 

노트북의 프로젝트 폴더에, Github에 push해놓은 자료들이 github library명으로 저장되어 있다. 내부를 확인해보면 first, second 파일 뿐만 아니라 log까지도 완벽하게 복사되었음을 알 수 있다. (git log명령어를 입력해보자.)  
또한 노트북에서 과제 작성 이후 add-commit-push 해주면 다음에 데스크탑에서 다시 pull하면 노트북의 내용을 이어서 작성할 수 있다.
<br><br>

# $ git rebase 

**5일차 :**    
rebase는 merge 명령어와 유사하게 사용할 수 있다. 예를 들어 앞서 얘기했던, 새로운 내용 혹은 기능을 테스트해보는 경우나, main branch와 side branch에서 둘다 작업을 하다가 병합하는 경우 모두 가능하다. 하지만 rebase와 merge의 가장 큰 차이는 작업 과정의 수정이다. 앞서 봤듯이, merge는 두 갈래의 branch를 합친다. 하지만 rebase는 한 branch를 다른 branch의 끝에 이어준다. (commit의 base를 다시 잡아준다!)

예를 들어, 이번에는 과제의 9. Images 에 대한 설명을 쓰고 나서, 나는 마땅한 이미지 파일이 컴퓨터에 없다는 것을 알았다. 그런데 동료가 적당한 사진을 추가한 파일을 image branch에 올려 주었다고 하자. 이 상태에서 merge를 해도 사진만 존재하는 파일과 설명만 존재하는 파일이 합쳐지긴 하지만, 설명을 먼저 쓰고 사진을 추가한 것처럼 보이기 위해서는 rebase를 쓰면 된다.   
![git_rebase](https://user-images.githubusercontent.com/81168401/117405104-09af7f80-af46-11eb-8d8f-8aec6f2f6dc2.png)  

![git_rebase2](https://user-images.githubusercontent.com/81168401/117405106-09af7f80-af46-11eb-829b-6eb6069f203a.png)  
`git merge <branch명>` 과 같이 사용하면, 제어가 위치한 (image)브랜치가 <branch명> 브랜치를 가리키게 된다. 여기서는 checkout image, git base main 과 같이 사용하면 된다.
<br><br>


# $ git tag  

**6일차 :**   
과제를 마지막까지 작성한 후, 과제에서 추가/검토하면서 수정된 커밋을 생성하게 될텐데, 몇번째 버전인지를 확인하는데 태그가 도움이 된다. 태그는 특정 커밋을 태깅한다.  
태그에는 크게 lightweight태그와 annotated 태그가 있는데, lightweight 태그는 git tag v1.0 와 같이 버전명만 간단하게 남기며, annotated 태그는 태그 제작자의 이름, 이메일, 태깅 날짜, 메세지, GPG서명까지 들어간다. 학생 입장에서는 lightweight 태그를 많이 사용할 것이다. 

![git_tag](https://user-images.githubusercontent.com/81168401/117405118-0c11d980-af46-11eb-854e-617aa25d7700.png)


<br><br><hr/><br>



| Git 명령어      | 사용 여부 |  Link  |
| ----------- | ----------- | ------- |
| add      | O       | [add](#-git-add)  |
| branch      | O       | [branch](#-git-branch/checkout-branch명)
| checkout      | O       |[checkout](#-git-branch/checkout-branch명)
| clone      | O       |[clone](#-git-clone)
| commit      | O       |[commit](#-git-commit)
| config      | O       |[config](#-git-config)
| init      | O       |[init](#-git-init)
| log      | O       |[log](#-git-log)
| merge      | O       |[merge](#-git-merge-branch명)
| pull      | O       |[pull](#-git-pull-origin-main)
| push      | O       |[push](#-git-push-origin-main)
| rebase      | O       |[rebase](#-git-rebase)
| remote      | O       |[remote](#-git-remote)
| reset      | O       |[reset](#-git-reset)
| status      | O       |[status](#-git-status)
| tag      | O       |[tag](#-git-tag)
