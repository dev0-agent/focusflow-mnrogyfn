# Task List

This file shows the current progress of all tasks in this project.
It is automatically updated by dev0 as tasks are completed.

---

## Phase 1

- [ ] ⏳ **Define Types and Global State Store**
  Create the core TypeScript interfaces (Task, Priority enum, Status enum). Implement a Zustand store in `src/store/useTaskStore.ts` with the `persist` middleware to save tasks to `localStorage`. The store should include actions to add, update, delete, and move tasks between statuses.

- [ ] ⏳ **Create App Layout and Header**
  Implement the main application layout in `src/components/layout/AppLayout.tsx`. Create a `Header` component that includes the app title, a simple logo/icon, and a dark mode toggle (using next-themes or a simple context). Ensure the layout is responsive and provides a clean, centered container for the main content.

## Phase 2

- [ ] ⏳ **Implement Task Creation Form**
  Create a `CreateTaskForm` component. It should include a text input for the task title and a select dropdown for the priority (Low, Medium, High). Use shadcn/ui components (Input, Select, Button). On submit, it should call the `addTask` action from the Zustand store and clear the input fields.

- [ ] ⏳ **Build Task Card Component**
  Create a `TaskCard` component to display individual tasks. It should show the task title, a color-coded badge for priority (e.g., Red for High, Yellow for Medium, Blue for Low), and a delete button (trash icon). The component should accept a `task` object as a prop.

- [ ] ⏳ **Implement Kanban Board Structure**
  Create a `Board` component and a `Column` component. The Board should render three Columns: 'Todo', 'In Progress', and 'Done'. Each Column should filter the tasks from the Zustand store based on their status and render a list of `TaskCard` components.

## Phase 3

- [ ] ⏳ **Integrate Drag and Drop Functionality**
  Implement drag-and-drop using a library like `@hello-pangea/dnd`. Wrap the `Board` in a DragDropContext. Make each `Column` a Droppable area and each `TaskCard` a Draggable item. Implement the `onDragEnd` handler to update the task's status and order in the Zustand store when dropped into a new column.

## Phase 4

- [ ] ⏳ **Add Daily Progress Tracker**
  Create a `ProgressTracker` component that calculates the percentage of tasks in the 'Done' status compared to the total number of tasks. Display this as a visual progress bar (using shadcn/ui Progress component) and a text summary (e.g., '5 of 8 tasks completed'). Place this component below the Header.

- [ ] ⏳ **Implement Clear Completed and Polish**
  Add a 'Clear Completed' button to the 'Done' column header or the main board area that removes all tasks with the 'Done' status from the store. Review the entire UI for consistent spacing, hover states, and responsive behavior on mobile devices.

---

_Last updated by dev0 automation_
