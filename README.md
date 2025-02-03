# to-do-list
class ToDoList:
    def __init__(self):
        self.tasks = []

    def add_task(self, task):
        self.tasks.append(task)
        print(f"Added task: {task}")

    def remove_task(self, task):
        if task in self.tasks:
            self.tasks.remove(task)
            print(f"Removed task: {task}")
        else:
            print(f"Task not found: {task}")

    def show_tasks(self):
        if not self.tasks:
            print("No tasks in the list.")
        else:
            print("To-Do List:")
            for idx, task in enumerate(self.tasks, 1):
                print(f"{idx}. {task}")

if __name__ == "__main__":
    todo_list = ToDoList()
    while True:
        print("\nOptions: 1. Add Task  2. Remove Task  3. Show Tasks  4. Exit")
        choice = input("Choose an option: ")
        if choice == '1':
            task = input("Enter the task: ")
            todo_list.add_task(task)
        elif choice == '2':
            task = input("Enter the task to remove: ")
            todo_list.remove_task(task)
        elif choice == '3':
            todo_list.show_tasks()
        elif choice == '4':
            break
        else:
            print("In-valid choice. Please try again.")
