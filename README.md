# TodoList React Practice

- 使用javascript, tailwindcss

- 以 `npm run dev` 執行，跑在locolhost


## 功能介紹：
- 導覽列（Navigation Bar）
  - Home：首頁
  - Todo List：待辦清單主頁
 
- Todo List 主頁功能
  - 新增 Todo 項目
    - 可輸入：名稱（Name）、截止日期（Due Date）、負責人（Assignee）
  - Todo 詳細頁面
    - 點擊任一 Todo 項目可跳轉至該項目的詳細頁面
    - 詳細頁面包含以下資訊：
      - 任務名稱（Task Name）
      - 截止日期（Due Date）
      - 當前狀態（Current Status）
      - 建立時間（Create Time）
      - 最後更新時間（Last Updated）
      - 剩餘天數（Days Left）
  - 階段切換功能
    - 每個 Todo 可依照進度切換四個階段：
      - Not Started
      - Progress
      - Done（完成後文字會有透明效果並加上刪除線）
      - Archived
    - 點擊階段按鈕即可切換至下一階段
  - 階段篩選功能
    - 可依照階段分類檢視 Todo 項目：
      - 顯示全部（All）
      - 僅顯示：Not Started、Progress、Done、Archived
  - 編輯與刪除功能
    - 每個 Todo 項目右側提供
      - 階段切換按鈕
      - 編輯按鈕：可修改名稱、日期、負責人
      - 刪除按鈕：移除該項目

## 介面：

Home
<img width="1044" height="329" alt="image" src="https://github.com/user-attachments/assets/9ec16668-f271-4747-8778-a39a13ab6917" />


Todo List
<img width="1016" height="925" alt="image" src="https://github.com/user-attachments/assets/e63d6397-68d7-46e8-a6ad-fd87a1b5c53d" />

Todo Detail
<img width="1055" height="479" alt="image" src="https://github.com/user-attachments/assets/c9add7ff-eade-469a-831d-3aadd9acfe09" />


## Tech Highlights：
- 架構設計
  - Component 模組化
    - 將功能拆分為獨立元件（如 AddTodo, TodoItem, DeleteButton 等），提升可維護性與重用性。
  - Pages 分頁管理
    - 使用 pages 資料夾管理多個頁面（ HomePage, TodosPage, DetailPage），搭配 Router 實現清晰的導覽流程。
  - Router 路由設計
    - 使用 react-router-dom 建立 /home、/todolist、/todos/:id 等路由，支援動態參數與頁面跳轉。
- 狀態管理與邏輯處理
  - useReducer：集中處理 Todo 的新增、編輯、刪除與狀態切換邏輯，讓資料流更清晰、可擴充。
  - Context API：透過 TodoContext.jsx 管理跨元件的共享狀態，簡化 props 傳遞
 
- UI 與互動設計
  - FilterBar / StatusButton：實作篩選功能與狀態切換，提升使用者操作體驗。
  - NavBar 導覽列：提供頁面切換入口，結合 Router 實現 SPA 導覽。

