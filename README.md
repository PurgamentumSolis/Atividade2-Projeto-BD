# Atividade2-Projeto-BD
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
[coisa de bd.txt](https://github.com/PurgamentumSolis/Atividade2-Projeto-BD/files/13507059/coisa.de.bd.txt)
section:
[
{"course_id": "BIO-101", "sec_id": "1", "semester": "Summer", "year": "2017", "building": "Painter", "room_no": "514", "time_slot_id": "B", "capacity": "10"},
{"course_id": "BIO-301", "sec_id": "1", "semester": "Summer", "year": "2018", "building": "Painter", "room_no": "514", "time_slot_id": "A", "capacity": "10"},
{"course_id": "CS-101", "sec_id": "1", "semester": "Fall", "year": "2017", "building": "Packard", "room_no": "101", "time_slot_id": "H", "capacity": "500"},
{"course_id": "CS-101", "sec_id": "1", "semester": "Spring", "year": "2018", "building": "Packard", "room_no": "101", "time_slot_id": "F", "capacity": "500"},
{"course_id": "CS-190", "sec_id": "1", "semester": "Spring", "year": "2017", "building": "Taylor", "room_no": "3128", "time_slot_id": "E", "capacity": "70"},
{"course_id": "CS-190", "sec_id": "2", "semester": "Spring", "year": "2017", "building": "Taylor", "room_no": "3128", "time_slot_id": "A", "capacity": "70"},
{"course_id": "CS-315", "sec_id": "1", "semester": "Spring", "year": "2018", "building": "Watson", "room_no": "120", "time_slot_id": "D", "capacity": "50"},
{"course_id": "CS-319", "sec_id": "1", "semester": "Spring", "year": "2018", "building": "Watson", "room_no": "100", "time_slot_id": "B", "capacity": "30"},
{"course_id": "CS-319", "sec_id": "2", "semester": "Spring", "year": "2018", "building": "Taylor", "room_no": "3128", "time_slot_id": "C", "capacity": "70"},
{"course_id": "CS-347", "sec_id": "1", "semester": "Fall", "year": "2017", "building": "Taylor", "room_no": "3128", "time_slot_id": "A", "capacity": "70"},
{"course_id": "EE-181", "sec_id": "1", "semester": "Spring", "year": "2017", "building": "Taylor", "room_no": "3128", "time_slot_id": "C", "capacity": "70"},
{"course_id": "FIN-201", "sec_id": "1", "semester": "Spring", "year": "2018", "building": "Packard", "room_no": "101", "time_slot_id": "B", "capacity": "500"},
{"course_id": "HIS-351", "sec_id": "1", "semester": "Spring", "year": "2018", "building": "Painter", "room_no": "514", "time_slot_id": "C", "capacity": "10"},
{"course_id": "MU-199", "sec_id": "1", "semester": "Spring", "year": "2018", "building": "Packard", "room_no": "101", "time_slot_id": "D", "capacity": "500"},
{"course_id": "PHY-101", "sec_id": "1", "semester": "Fall", "year": "2017", "building": "Watson", "room_no": "100", "time_slot_id": "A", "capacity": "50"}
]





time_slot:
[
{"time_slot_id": "B", "days": [{"week_day": "M", "start_hour": "9", "start_min": "0", "end_hour": "9", "end_min": "50"},
                                {"week_day": "W", "start_hour": "9", "start_min": "0", "end_hour": "9", "end_min": "50"},
                                {"week_day": "F", "start_hour": "9", "start_min": "0", "end_hour": "9", "end_min": "50"}]},

{"time_slot_id": "C", "days": [{"week_day": "M", "start_hour": "11", "start_min": "0", "end_hour": "11", "end_min": "50"},
                                {"week_day": "W", "start_hour": "11", "start_min": "0", "end_hour": "11", "end_min": "50"},
                                {"week_day": "F", "start_hour": "11", "start_min": "0", "end_hour": "11", "end_min": "50"}]},

{"time_slot_id": "D", "days": [{"week_day": "M", "start_hour": "13", "start_min": "0", "end_hour": "13", "end_min": "50"},
                                {"week_day": "W", "start_hour": "13", "start_min": "0", "end_hour": "13", "end_min": "50"},
                                {"week_day": "F", "start_hour": "13", "start_min": "0", "end_hour": "13", "end_min": "50"}]},

{"time_slot_id": "E", "days": [{"week_day": "T", "start_hour": "10", "start_min": "30", "end_hour": "11", "end_min": "45"},
                                {"week_day": "R", "start_hour": "10", "start_min": "30", "end_hour": "11", "end_min": "45"}]},

{"time_slot_id": "F", "days": [{"week_day": "T", "start_hour": "14", "start_min": "30", "end_hour": "15", "end_min": "45"},
                                {"week_day": "R", "start_hour": "14", "start_min": "30", "end_hour": "15", "end_min": "45"}]},

{"time_slot_id": "G", "days": [{"week_day": "M", "start_hour": "16", "start_min": "0", "end_hour": "16", "end_min": "50"},
                                {"week_day": "W", "start_hour": "16", "start_min": "0", "end_hour": "16", "end_min": "50"},
                                {"week_day": "F", "start_hour": "16", "start_min": "0", "end_hour": "16", "end_min": "50"}]},

{"time_slot_id": "H", "days": [{"week_day": "W", "start_hour": "10", "start_min": "0", "end_hour": "12", "end_min": "30"}]}
]



course:
[
{"idCouse": "BIO-101", "title": "Intro. to Biology", "dept_name": "Biology", "credits": 4},
{"idCouse": "BIO-301", "title": "Genetics", "dept_name": "Biology", "credits": 4},
{"idCouse": "BIO-399", "title": "Computational Biology", "dept_name": "Biology", "credits": 3},
{"idCouse": "CS-101", "title": "Intro. to Computer Science", "dept_name": "Comp. Sci.", "credits": 4},
{"idCouse": "CS-190", "title": "Game Design", "dept_name": "Comp. Sci.", "credits": 4},
{"idCouse": "CS-315", "title": "Robotics", "dept_name": "Comp. Sci.", "credits": 3},
{"idCouse": "CS-319", "title": "Image Processing", "dept_name": "Comp. Sci.", "credits": 3},
{"idCouse": "CS-347", "title": "Database System Concepts", "dept_name": "Comp. Sci.", "credits": 3},
{"idCouse": "EE-181", "title": "Intro. to Digital Systems", "dept_name": "Elec. Eng.", "credits": 3},
{"idCouse": "FIN-201", "title": "Investment Banking", "dept_name": "Finance", "credits": 3},
{"idCouse": "HIS-351", "title": "World History", "dept_name": "History", "credits": 3},
{"idCouse": "MU-199", "title": "Music Video Production", "dept_name": "Music", "credits": 3},
{"idCouse": "PHY-101", "title": "Physical Principles", "dept_name": "Physics", "credits": 4}
]

















