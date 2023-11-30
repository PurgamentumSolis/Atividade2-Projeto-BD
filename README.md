[Time_slot.txt](https://github.com/PurgamentumSolis/Atividade2-Projeto-BD/files/13507083/Time_slot.txt)[Course.txt](https://github.com/PurgamentumSolis/Atividade2-Projeto-BD/files/13507082/Course.txt)[Student.txt](https://github.com/PurgamentumSolis/Atividade2-Projeto-BD/files/13507081/Student.txt)[Department.txt](https://github.com/PurgamentumSolis/Atividade2-Projeto-BD/files/13507079/Department.txt)[Section.txt](https://github.com/PurgamentumSolis/Atividade2-Projeto-BD/files/13507076/Section.txt)# Atividade2-Projeto-BD
Atividade2 Projeto BD, 6 semeste

integrantes:<br>
Fernando Chan Lin 22.221.015-5 <br>
William Yang 22.121.043-8 <br>

<h1>Introdução</h1>

Para realizar a atividade foi escolhido o banco NOSQL <strong>document storage</strong> e usamos o MongoDB
A divisão do banco foi feito em 5 Collections, sendo elas;
- Course
- Department
- Section
- Student
- Time_slot
<h2>Divisão</h2>
Seguindo a imagem do banco relacional

![bad](https://github.com/PurgamentumSolis/Atividade2-Projeto-BD/assets/91858664/057a8b98-575b-4723-bc8f-849f9f7814ef)

- Verde -> Section
- Roxo -> Department
- Azul -> Student
- Laranja -> Course
- Vermelho -> Time_slot

<h2>Scripts para inserção</h2>
Para relizar a inserção foi feito o tratamento da query https://db-book.com/university-lab-dir/sample_tables-dir/index.html manualemente e para cada Collection foi feito um script.
<h4>Section</h4>
[Uploading Section.txt…]()
Exemplo:
{"course_id": "BIO-101", "sec_id": "1", "semester": "Summer", "year": "2017", "building": "Painter", "room_no": "514", "time_slot_id": "B", "capacity": "10"},

<h4>Department</h4>
[Uploading Department.txt…]()
Exemplo:
{
        "dept_name": "Biology",
        "building": "Watson",
        "budget": 90000,
        "instructors": [
            {
                "ID": "76766",
                "name": "Crick",
                "salary": 72000,
                "advising": ["98988"],
                "teaches": [
                    {"course_id": "BIO-101", "sec_id": "1"},
                    {"course_id": "BIO-301", "sec_id": "1"}
                ]
            }
        ]
    },
    
<h4>Student</h4>
[Uploading Student.txt…]()
{
    "student_id": "00128",
    "name": "Zhang",
    "dpt_name": "Comp. Sci.",
    "total_cred": "102",
    "takes": [
        {"course_id": "CS-101", "sec_id": "1", "grade": "A"},
        {"course_id": "CS-347", "sec_id": "1", "grade": "A-"}
    ]
}

<h4>Course</h4>
[Uploading Course.txt…]()
{"idCourse": "BIO-101", "title": "Intro. to Biology", "dept_name": "Biology", "credits": 4},

<h4>Time_slot</h4>
[Uploading Time_slot.txt…]()
{"time_slot_id": "B", "days": [{"week_day": "M", "start_hour": "9", "start_min": "0", "end_hour": "9", "end_min": "50"},
                                {"week_day": "W", "start_hour": "9", "start_min": "0", "end_hour": "9", "end_min": "50"},
                                {"week_day": "F", "start_hour": "9", "start_min": "0", "end_hour": "9", "end_min": "50"}]}

















