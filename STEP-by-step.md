1단계. 개발 환경 준비 — 전원
1. Python 설치 (Windows에서는 Add Python to PATH 체크)
2. VS Code 설치
3. Git 설치
4. VS Code에서 Python 확장 프로그램 설치
5. GitHub 로그인 및 저장소 초대 수락
6. VS Code에서 터미널 열기
7. 프로젝트 다운로드
git clone https://github.com/kimhohyeong2/md-to-word.git
cd md-to-word


8. 가상환경 생성
python -m venv .venv


9. 가상환경 활성화

Windows:
.\.venv\Scripts\Activate.ps1


macOS:
source .venv/bin/activate


10. 라이브러리 설치
python -m pip install -r requirements.txt


11. 각자 작업할 브랜치 생성
담당자	명령어
배정민	git switch -c feature/converter-gui
신재민	git switch -c feature/file-manager
김형호	git switch -c feature/integration

2단계. 개별 기능 개발
배정민 — A. 변환 기능 (converter.py)
- [ ] converter.py 파일 생성
- [ ] Markdown 파일 읽기
- [ ] Mistune을 이용한 Markdown 문법 분석
- [ ] python-docx를 이용한 Word 문서 생성
- [ ] 제목 적용 (#, ##, ###)
- [ ] 일반 본문 적용
- [ ] 굵게 및 기울임 적용
- [ ] 순서 있는 목록 적용
- [ ] 순서 없는 목록 적용
- [ ] 표 변환
- [ ] 이미지 삽입
- [ ] 글꼴 설정
- [ ] 글자 크기 설정
- [ ] 줄 간격 설정
- [ ] 문서 여백 설정
- [ ] .docx 파일 저장
- [ ] 개별 기능 테스트
- [ ] 변환 기능 완성
배정민 — B. GUI (gui.py)
- [ ] gui.py 파일 생성
- [ ] PyQt5를 이용한 기본 프로그램 창 생성
- [ ] 파일 선택 버튼 구현
- [ ] 폴더 선택 버튼 구현
- [ ] 선택된 파일 목록 표시
- [ ] 저장 경로 표시 및 변경 기능
- [ ] 글꼴 선택 기능
- [ ] 글자 크기 설정 기능
- [ ] 줄 간격 설정 기능
- [ ] 여백 설정 기능
- [ ] 변환 버튼 구현
- [ ] 변환 진행 상태 표시
- [ ] 변환 완료 메시지 표시
- [ ] 오류 메시지 표시
- [ ] 결과 폴더 열기 버튼 구현
- [ ] GUI 실행 테스트
신재민 — C. 파일 관리 (file_manager.py)
- [ ] file_manager.py 파일 생성
- [ ] 파일 경로 받아오기
- [ ] 파일 존재 여부 확인
- [ ] .md 확장자 확인
- [ ] 폴더 내 Markdown 파일 탐색
- [ ] 여러 파일 목록 반환
- [ ] 기본 저장 경로 설정
- [ ] 결과 저장 폴더 자동 생성
- [ ] 일괄 변환 시 날짜·시간별 폴더 생성
- [ ] 원본 파일명을 기반으로 결과 파일명 생성
- [ ] 동일한 이름의 파일이 존재할 경우 덮어쓰기 방지
- [ ] 잘못된 파일 경로 예외 처리
- [ ] 저장 권한 오류 처리
- [ ] 개별 기능 테스트
- [ ] 파일 관리 기능 완성
3단계. GitHub 업로드 — 전원
각자 맡은 기능을 완성한 후 진행합니다.

1. 변경 사항 확인
git status


2. 작업한 파일 추가

배정민:
git add converter.py gui.py


신재민:
git add file_manager.py


3. 변경 사항 저장
git commit -m "담당 기능 구현"


4. GitHub에 업로드
git push -u origin HEAD


5. GitHub 저장소 접속
6. Compare & pull request 클릭
7. 구현한 기능 설명 작성
8. Create pull request 클릭
9. 팀장에게 검토 요청
팀원들은 직접 main 브랜치에 병합하지 않습니다.
4단계. 코드 병합 및 통합 — 김형호
- [ ] 팀원들의 Pull Request 확인
- [ ] 코드 검토
- [ ] 함수 이름 및 매개변수 확인
- [ ] 중복 기능 확인
- [ ] 라이브러리 누락 확인
- [ ] 수정 사항 요청
- [ ] Pull Request 승인
- [ ] main 브랜치에 병합
- [ ] 최신 코드 다운로드
- [ ] main.py 작성
- [ ] GUI와 파일 관리 기능 연결
- [ ] 파일 관리와 변환 기능 연결
- [ ] GUI 서식 설정과 변환 기능 연결
- [ ] 전체 프로그램 실행
프로그램 구조는 다음과 같이 구성하는 것을 권장합니다.
#chatgpt-mermaid-_r_pg_{font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";font-size:16px;fill:rgb(13, 13, 13);}@keyframes edge-animation-frame{from{stroke-dashoffset:0;}}@keyframes dash{to{stroke-dashoffset:0;}}#chatgpt-mermaid-_r_pg_ .edge-animation-slow{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 50s linear infinite;stroke-linecap:round;}#chatgpt-mermaid-_r_pg_ .edge-animation-fast{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 20s linear infinite;stroke-linecap:round;}#chatgpt-mermaid-_r_pg_ .error-icon{fill:rgb(243, 243, 243);}#chatgpt-mermaid-_r_pg_ .error-text{fill:rgb(13, 13, 13);stroke:rgb(13, 13, 13);}#chatgpt-mermaid-_r_pg_ .edge-thickness-normal{stroke-width:1px;}#chatgpt-mermaid-_r_pg_ .edge-thickness-thick{stroke-width:3.5px;}#chatgpt-mermaid-_r_pg_ .edge-pattern-solid{stroke-dasharray:0;}#chatgpt-mermaid-_r_pg_ .edge-thickness-invisible{stroke-width:0;fill:none;}#chatgpt-mermaid-_r_pg_ .edge-pattern-dashed{stroke-dasharray:3;}#chatgpt-mermaid-_r_pg_ .edge-pattern-dotted{stroke-dasharray:2;}#chatgpt-mermaid-_r_pg_ .marker{fill:rgb(143, 143, 143);stroke:rgb(143, 143, 143);}#chatgpt-mermaid-_r_pg_ .marker.cross{stroke:rgb(143, 143, 143);}#chatgpt-mermaid-_r_pg_ svg{font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";font-size:16px;}#chatgpt-mermaid-_r_pg_ p{margin:0;}#chatgpt-mermaid-_r_pg_ .label{font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";color:rgb(13, 13, 13);}#chatgpt-mermaid-_r_pg_ .cluster-label text{fill:rgb(13, 13, 13);}#chatgpt-mermaid-_r_pg_ .cluster-label span{color:rgb(13, 13, 13);}#chatgpt-mermaid-_r_pg_ .cluster-label span p{background-color:transparent;}#chatgpt-mermaid-_r_pg_ .label text,#chatgpt-mermaid-_r_pg_ span{fill:rgb(13, 13, 13);color:rgb(13, 13, 13);}#chatgpt-mermaid-_r_pg_ .node rect,#chatgpt-mermaid-_r_pg_ .node circle,#chatgpt-mermaid-_r_pg_ .node ellipse,#chatgpt-mermaid-_r_pg_ .node polygon,#chatgpt-mermaid-_r_pg_ .node path{fill:rgb(222, 234, 251);stroke:rgb(83, 154, 248);stroke-width:1px;}#chatgpt-mermaid-_r_pg_ .rough-node .label text,#chatgpt-mermaid-_r_pg_ .node .label text,#chatgpt-mermaid-_r_pg_ .image-shape .label,#chatgpt-mermaid-_r_pg_ .icon-shape .label{text-anchor:middle;}#chatgpt-mermaid-_r_pg_ .node .katex path{fill:#000;stroke:#000;stroke-width:1px;}#chatgpt-mermaid-_r_pg_ .rough-node .label,#chatgpt-mermaid-_r_pg_ .node .label,#chatgpt-mermaid-_r_pg_ .image-shape .label,#chatgpt-mermaid-_r_pg_ .icon-shape .label{text-align:center;}#chatgpt-mermaid-_r_pg_ .node.clickable{cursor:pointer;}#chatgpt-mermaid-_r_pg_ .root .anchor path{fill:rgb(143, 143, 143)!important;stroke-width:0;stroke:rgb(143, 143, 143);}#chatgpt-mermaid-_r_pg_ .arrowheadPath{fill:rgb(143, 143, 143);}#chatgpt-mermaid-_r_pg_ .edgePath .path{stroke:rgb(143, 143, 143);stroke-width:1px;}#chatgpt-mermaid-_r_pg_ .flowchart-link{stroke:rgb(143, 143, 143);fill:none;}#chatgpt-mermaid-_r_pg_ .edgeLabel{background-color:rgb(252, 252, 252);text-align:center;}#chatgpt-mermaid-_r_pg_ .edgeLabel p{background-color:rgb(252, 252, 252);}#chatgpt-mermaid-_r_pg_ .edgeLabel rect{opacity:0.5;background-color:rgb(252, 252, 252);fill:rgb(252, 252, 252);}#chatgpt-mermaid-_r_pg_ .labelBkg{background-color:rgba(252, 252, 252, 0.5);}#chatgpt-mermaid-_r_pg_ .cluster rect{fill:rgb(243, 243, 243);stroke:rgba(0, 0, 0, 0.1);stroke-width:1px;}#chatgpt-mermaid-_r_pg_ .cluster text{fill:rgb(13, 13, 13);}#chatgpt-mermaid-_r_pg_ .cluster span{color:rgb(13, 13, 13);}#chatgpt-mermaid-_r_pg_ div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";font-size:12px;background:rgb(243, 243, 243);border:1px solid rgba(0, 0, 0, 0.1);border-radius:2px;pointer-events:none;z-index:100;}#chatgpt-mermaid-_r_pg_ .flowchartTitleText{text-anchor:middle;font-size:18px;fill:rgb(13, 13, 13);}#chatgpt-mermaid-_r_pg_ rect.text{fill:none;stroke-width:0;}#chatgpt-mermaid-_r_pg_ .icon-shape,#chatgpt-mermaid-_r_pg_ .image-shape{background-color:rgb(252, 252, 252);text-align:center;}#chatgpt-mermaid-_r_pg_ .icon-shape p,#chatgpt-mermaid-_r_pg_ .image-shape p{background-color:rgb(252, 252, 252);padding:2px;}#chatgpt-mermaid-_r_pg_ .icon-shape .label rect,#chatgpt-mermaid-_r_pg_ .image-shape .label rect{opacity:0.5;background-color:rgb(252, 252, 252);fill:rgb(252, 252, 252);}#chatgpt-mermaid-_r_pg_ .label-icon{display:inline-block;height:1em;overflow:visible;vertical-align:-0.125em;}#chatgpt-mermaid-_r_pg_ .node .label-icon path{fill:currentColor;stroke:revert;stroke-width:revert;}#chatgpt-mermaid-_r_pg_ .node .neo-node{stroke:rgb(83, 154, 248);}#chatgpt-mermaid-_r_pg_ [data-look="neo"].node rect,#chatgpt-mermaid-_r_pg_ [data-look="neo"].cluster rect,#chatgpt-mermaid-_r_pg_ [data-look="neo"].node polygon{stroke:url(#chatgpt-mermaid-_r_pg_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-_r_pg_ [data-look="neo"].swimlane.cluster rect{filter:none;}#chatgpt-mermaid-_r_pg_ [data-look="neo"].node path{stroke:url(#chatgpt-mermaid-_r_pg_-gradient);stroke-width:1px;}#chatgpt-mermaid-_r_pg_ [data-look="neo"].node .outer-path{filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-_r_pg_ [data-look="neo"].node .neo-line path{stroke:rgb(83, 154, 248);filter:none;}#chatgpt-mermaid-_r_pg_ [data-look="neo"].node circle{stroke:url(#chatgpt-mermaid-_r_pg_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-_r_pg_ [data-look="neo"].node circle .state-start{fill:#000000;}#chatgpt-mermaid-_r_pg_ [data-look="neo"].icon-shape .icon{fill:url(#chatgpt-mermaid-_r_pg_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-_r_pg_ [data-look="neo"].icon-shape .icon-neo path{stroke:url(#chatgpt-mermaid-_r_pg_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-_r_pg_ .node text{font-size:14px;font-weight:600;letter-spacing:normal;fill:rgb(0, 79, 153);}#chatgpt-mermaid-_r_pg_ .edgeLabels text{font-size:13px;font-weight:600;letter-spacing:-0.08px;fill:rgb(0, 79, 153);}#chatgpt-mermaid-_r_pg_ .node tspan[font-weight="normal"],#chatgpt-mermaid-_r_pg_ .edgeLabels tspan[font-weight="normal"]{font-weight:600;}#chatgpt-mermaid-_r_pg_ .edgeLabel .label rect{opacity:1;rx:13px;ry:13px;fill:rgb(245, 250, 255);stroke:rgb(206, 219, 229);stroke-width:1px;}#chatgpt-mermaid-_r_pg_ .node rect,#chatgpt-mermaid-_r_pg_ .node circle,#chatgpt-mermaid-_r_pg_ .node ellipse,#chatgpt-mermaid-_r_pg_ .node polygon,#chatgpt-mermaid-_r_pg_ .node path{fill:rgb(229, 243, 255);stroke:rgba(0, 0, 0, 0.1);stroke-width:1px;}#chatgpt-mermaid-_r_pg_ .node rect{rx:16px;ry:16px;}#chatgpt-mermaid-_r_pg_ .mermaid-decision .label-container{fill:rgb(245, 250, 255);stroke:rgb(206, 219, 229);stroke-dasharray:2,2;}#chatgpt-mermaid-_r_pg_ .edgePaths .flowchart-link{stroke:rgb(143, 143, 143);stroke-width:1px;stroke-linecap:round;stroke-linejoin:round;}#chatgpt-mermaid-_r_pg_ .marker{fill:rgb(143, 143, 143);stroke:rgb(143, 143, 143);}#chatgpt-mermaid-_r_pg_ :root{--mermaid-font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";}main.py프로그램 실행 및 통합gui.py사용자 인터페이스file_manager.py파일 탐색 및 경로 관리converter.pyMarkdown → Word 변환Word 파일 저장GUI 결과 표시





5단계. 전체 프로그램 테스트 — 김형호
- [ ] 단일 Markdown 파일 변환
- [ ] 여러 Markdown 파일 일괄 변환
- [ ] 제목 및 본문 변환
- [ ] 표 및 이미지 변환
- [ ] 글꼴 및 크기 설정 적용
- [ ] 줄 간격 및 여백 설정 적용
- [ ] 한글·영어·일본어 파일 변환
- [ ] 빈 파일 처리
- [ ] 잘못된 확장자 처리
- [ ] 존재하지 않는 파일 처리
- [ ] 중복 파일명 처리
- [ ] 저장 권한 오류 처리
- [ ] Windows 실행 테스트
- [ ] macOS 실행 테스트
- [ ] 오류 수정
6단계. 배포 — 김형호
- [ ] PyInstaller 설치 확인
- [ ] EXE 실행 파일 제작
python -m PyInstaller --onefile --windowed --name MD-to-Word main.py


- [ ] EXE 실행 테스트
- [ ] Inno Setup 설치
- [ ] 설치 프로그램 제작
- [ ] Windows 우클릭 메뉴 연동
- [ ] 프로그램 제거 시 우클릭 메뉴 제거
- [ ] Python이 설치되지 않은 Windows PC에서 테스트
- [ ] 최종 설치 파일 제작
- [ ] GitHub Releases에 배포
- [ ] README.md 사용 설명서 작성
- [ ] 최종 보고서 작성
- [ ] 발표 자료 제작
Windows용 EXE는 Windows 환경에서 제작해야 합니다.

개발 전에 반드시 합의할 사항
각자 코드를 작성하기 전에 함수 이름, 매개변수, 반환값을 통일해야 합니다. 그렇지 않으면 각자 기능을 완성하더라도 서로 연결되지 않을 수 있습니다.

예를 들어 다음과 같이 정할 수 있습니다.
파일	함수	역할
converter.py	convert_file()	Markdown 변환
file_manager.py	get_md_files()	Markdown 파일 탐색
file_manager.py	get_output_path()	저장 경로 생성
file_manager.py	create_output_folder()	결과 폴더 생성
gui.py	MainWindow	프로그램 화면
main.py	main()	프로그램 실행

이 함수 이름과 세부 구현 순서는 내가 제안한 것이며, 현재 GitHub 소스 코드를 직접 검토한 결과는 아닙니다. 압축 및 문서 암호화 기능도 최종 구현 여부가 확정되지 않아 필수 작업에서 제외했습니다.

지금 당장 해야 할 일은 개발 환경 준비와 함수 인터페이스 합의입니다. 이후 각자 독립적으로 개발하면 됩니다.
