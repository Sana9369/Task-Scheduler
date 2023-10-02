
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>🅢🅐🅝🅐'🅢</title>
    <style>

body{
background-image:url('jkl.jpeg');
background-size:cover;
}
.asa{
background-color:red;
}

        body {
            font-family: Arial, sans-serif;
background-color:steelblue;
        }
        
        #todo-list {
            max-width: 300px;
            margin: 0 auto;
        }
        
        #todo-list ul {
            list-style-type: none;
            padding: 0;
        }
        
        #todo-list li {
            display: flex;
            align-items: center;
            margin: 5px 0;
        }
        
        #todo-list input[type="checkbox"] {
            margin-right: 10px;
        }
        
        #add-task input[type="text"] {
            width: 70%;
        }
        
        #add-task button {
            width: 30%;
        }
    </style>
</head>
<body>
    <div id="todo-list">
        <h1>🆃🅾 🅳🅾 🅻🅸🆂🆃</h1>
        <div id="add-task">
            <input type="text" id="new-task" placeholder="𝑶𝒓𝒈𝒂𝒏𝒊𝒛𝒆 𝒀𝒐𝒖𝒓 𝑻𝒂𝒔𝒌𝒔 𝑯𝒆𝒓𝒆">
            <button class="asa" onclick="addTask()">𝑨𝒅𝒅</button>
        </div>
        <ul id="tasks">
            <!-- Tasks will be added here -->
        </ul>
    </div>
    <script>
        function addTask() {
            var taskText = document.getElementById("new-task").value;
            if (taskText === "") {
                alert("Please enter a task.");
                return;
            }

            var taskList = document.getElementById("tasks");
            var newTask = document.createElement("li");
            newTask.innerHTML = `
                <input type="checkbox">
                <span>${taskText}</span>
                <button onclick="removeTask(this)">Remove</button>
            `;
            taskList.appendChild(newTask);
            document.getElementById("new-task").value = "";
        }

        function removeTask(button) {
            var taskList = document.getElementById("tasks");
            var taskToRemove = button.parentElement;
            taskList.removeChild(taskToRemove);
        }
    </script>
</body>
</html>
