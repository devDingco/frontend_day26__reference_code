1. 공통
    - [ ]  완성된 `day26` 폴더를 활용하여 `day27` 을 완성해 주세요.
        - 폴더를 다시 생성할 필요는 없습니다 !
        - 해당 폴더에서 계속 작업해서 과제 제출해 주시면 됩니다.
        
2. 게시글 목록
    - [ ]  게시글 목록 관련 페이지 및 컴포넌트에 이벤트 버블링을 처리해 주세요.
        - 게시글 내용 뿐 아니라, 삭제 버튼을 제외한 게시글 목록 영역을 클릭해도 클릭한 게시글의 상세 페이지로 이동시켜 주세요.
        - 페이지 경로: `src/app/boards/page.tsx`
    
3. 게시글 상세
    - [ ]  게시글 상세 페이지에 사용될 댓글 영역 구현에 필요한 컴포넌트 2개를 추가로 만들어 주세요.
        - 아래 경로의 폴더는 생성해 주세요.
        - 댓글 목록 컴포넌트 경로: `src/components/boards-detail/comment-list`
        - 댓글 등록 컴포넌트 경로: `src/components/boards-detail/comment-write`
    - [ ]  기존에 구현한 게시글 상세 컴포넌트 관련 파일들을 아래 폴더 경로로 이동시켜 주세요.
        - 아래 경로의 폴더는 생성해 주세요.
        - 이동할 폴더 경로: `src/components/boards-detail/detail`
        - 파일 목록:
            - hook.ts
            - index.tsx
            - queries.ts
            - styles.module.css
            - types.ts


4. 게시글 상세[댓글 등록]

![image](https://github.com/user-attachments/assets/8f9d2b76-c226-4ba4-82e7-4024d83d299d)

 - [ ] src/components/boards-detail/comment-write/index.tsx 경로에 위 이미지의 댓글 등록 부분을 완성해 주세요.
     - [ ] 댓글 입력 후, 댓글등록 버튼을 누르면 GRAPHQL-API(createBoardComment)를 사용하여 댓글을 등록해 주세요.
     - [ ] 댓글이 등록된 후, 댓글을 목록에서 조회하기 위해 GRAPHQL-API(fetchBoardComments)를 리페치해 주세요.
     - [ ] 댓글이 등록된 후, 댓글입력창을 모두 초기화 합니다.
     - [ ] 별점, 아바타사진, 수정/삭제 아이콘은 아직 기능을 추가하진 않습니다.(따라서, 별점은 0점으로 등록합니다.)



5. 게시글 상세[댓글 목록 조회]

![image](https://github.com/user-attachments/assets/7bde16a0-7a96-45a1-a422-e93f68575a3e)

 - [ ] src/components/boards-detail/comment-list/index.tsx 경로에 위 이미지의 댓글목록 부분을 완성해 주세요.
     - [ ] GRAPHQL-API(fetchBoardComments)를 사용하여 댓글목록을 완성합니다.
     - [ ] 별점, 아바타사진, 수정/삭제 아이콘은 아직 기능을 추가하진 않습니다.(따라서, 별점은 0점으로 보여줍니다.)

6. 게시글상세[최종조립]
 - [ ] 게시글상세페이지 src/app/boards/[boardId]/page.tsx 경로의 파일을 수정합니다.
     - [ ] 해당 페이지에 위에서 만든 3개의 컴포넌트(게시글상세, 댓글등록, 댓글목록)를 불러와서 조립합니다.

7. 컴포넌트[리팩토링]
    - [ ] 게시글상세, 댓글등록, 댓글목록조회 컴포넌트의 파일을 보완해 주세요.
        - [ ] 타입에러가 감지되어 빨간 밑줄이 그어지는 부분에 타입스크립트를 적용하여 문제를 해결해 주세요.
        - [ ] 유지보수가 쉽도록 파일을 hook.ts, index.tsx, queries.ts, styles.ts, types.ts 로 분리해 주세요.
