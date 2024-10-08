1. 공통
    - 완성된 day26 폴더를 활용하여 day27을 완성해 주세요.
2. 게시글목록
    - src/app/boards/page.tsx 경로의 게시글목록과 관련된 페이지 및 컴포넌트에 이벤트 버블링을 처리해 보세요.
    => 게시글내용 뿐만 아니라, 삭제버튼을 제외한 게시글 목록 영역을 클릭하더라도 클릭한 게시글의 상세페이지로 이동시켜 주세요.
3. 게시글상세
    - 게시글 상세 컴포넌트가 게시글상세, 댓글등록, 댓글목록 3개의 컴포넌트로 분리될 예정입니다.
    따라서, 게시글 상세 컴포넌트 하위에 3개의 컴포넌트를 추가로 만들어 주세요.
        - 댓글목록: src/components/boards-detail/comment-list
        - 댓글등록: src/components/boards-detail/comment-write
        - 게시글상세: src/components/boards-detail/detail
    - 기존에 존재하였던 게시글상세컴포넌트의 파일들(hook, index, queries, styles, types)을
    src/components/boards-detail/detail 경로로 이동시켜 주세요.
        - src/components/boards-detail/hook.ts => src/components/boards-detail/detail/hook.ts
        - src/components/boards-detail/index.tsx => src/components/boards-detail/detail/index.tsx
        - src/components/boards-detail/queries.ts => src/components/boards-detail/detail/queries.ts
        - src/components/boards-detail/styles.module.css => src/components/boards-detail/detail/styles.module.css
        - src/components/boards-detail/types.ts => src/components/boards-detail/detail/types.ts
4. 게시글상세[댓글등록]
   
    ![image](https://github.com/user-attachments/assets/8f9d2b76-c226-4ba4-82e7-4024d83d299d)
    - src/components/boards-detail/comment-write/index.tsx 경로에 위 이미지의 댓글 등록 부분을 완성해 주세요.
    => 댓글 입력 후, 댓글등록 버튼을 누르면 GRAPHQL-API(createBoardComment)를 사용하여 댓글을 등록해 주세요.
    => 댓글이 등록된 후, 댓글을 목록에서 조회하기 위해 GRAPHQL-API(fetchBoardComments)를 리페치해 주세요.
    => 댓글이 등록된 후, 댓글입력창을 모두 초기화 합니다.
    => 별점, 아바타사진, 수정/삭제 아이콘은 아직 기능을 추가하진 않습니다.(따라서, 별점은 0점으로 등록합니다.)
6. 게시글상세[댓글목록조회]
    ![image](https://github.com/user-attachments/assets/7bde16a0-7a96-45a1-a422-e93f68575a3e)
    - src/components/boards-detail/comment-list/index.tsx 경로에 위 이미지의 댓글목록 부분을 완성해 주세요.
    => GRAPHQL-API(fetchBoardComments)를 사용하여 댓글목록을 완성합니다.
    => 별점, 아바타사진, 수정/삭제 아이콘은 아직 기능을 추가하진 않습니다.(따라서, 별점은 0점으로 보여줍니다.)
7. 게시글상세[최종조립]
    - 게시글상세페이지 src/app/boards/[boardId]/page.tsx 경로의 파일을 수정합니다.
    => 해당 페이지에 위에서 만든 3개의 컴포넌트(게시글상세, 댓글등록, 댓글목록)를 불러와서 조립합니다.
8. 컴포넌트[리팩토링]
    - 게시글상세, 댓글등록, 댓글목록조회 컴포넌트의 파일을 보완해 주세요.
    => 타입에러가 감지되어 빨간 밑줄이 그어지는 부분에 타입스크립트를 적용하여 문제를 해결해 주세요.
    => 유지보수가 쉽도록 파일을 hook.ts, index.tsx, queries.ts, styles.ts, types.ts 로 분리해 주세요.
