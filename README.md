# Note-Taking-App
This is a Note-Taking App
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Note-Taking App</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        #notes-container {
            width: 300px;
            margin: 20px auto;
            border: 1px solid #ccc;
            padding: 10px;
            border-radius: 5px;
        }
        #notes-container textarea {
            width: 100%;
            margin-bottom: 10px;
        }
        #notes-container button {
            padding: 8px 15px;
            background-color: #007bff;
            color: #fff;
            border: none;
            cursor: pointer;
        }
        #notes-container button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>

<div id="notes-container">
    <textarea id="noteInput" placeholder="Enter your note here..."></textarea>
    <button onclick="addNote()">Add Note</button>
    <div id="notesList"></div>
</div>

<script>
    function addNote() {
        const noteInput = document.getElementById('noteInput');
        const note = noteInput.value.trim();

        if (note !== '') {
            const notesList = document.getElementById('notesList');
            const newNote = document.createElement('div');
            newNote.textContent = note;
            notesList.appendChild(newNote);

            noteInput.value = '';
        } else {
            alert('Please enter a note.');
        }
    }
</script>

</body>
</html>
