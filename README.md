# -Code-Refactoring-and-Bug-Fixing
#  Flask Notes App
This is a simple note-taking web application built using **Python** and **Flask**.  
Users can add short notes through a web form, and all notes are displayed on the same page.

Technologies Used
- Python 3
- Flask
- HTML (Jinja2 templating)

 Clone this repository

```bash
git clone https://github.com/your-username/flask-notes-app.git
cd flask-notes-app

pip install flask
python app.py

flask-notes-app/
 app.py               # Main Flask app
 templates/
 home.html        # HTML form to input and display notes

home.html (Template)

<!DOCTYPE html>
<html>
<head>
    <title>Notes App</title>
</head>
<body>
    <h1>My Notes</h1>
    <form method="POST">
        <input type="text" name="note" placeholder="Enter your note" required>
        <button type="submit">Add Note</button>
    </form>
    <ul>
        {% for note in notes %}
            <li>{{ note }}</li>
        {% endfor %}
    </ul>
</body>
</html>
