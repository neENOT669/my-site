<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Портфолио педагога дополнительного образования</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #27ae60;
        }

        body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Шапка */
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 2rem 0;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo i {
            font-size: 2.5rem;
            color: var(--light);
        }

        .logo h1 {
            font-size: 1.8rem;
        }

        .logo span {
            font-size: 1rem;
            opacity: 0.9;
            font-weight: normal;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            transition: 0.3s;
            padding: 5px 0;
            border-bottom: 2px solid transparent;
        }

        nav a:hover {
            border-bottom: 2px solid white;
        }

        /* Основной контент */
        .main-content {
            display: grid;
            grid-template-columns: 1fr 300px;
            gap: 30px;
            margin: 30px 0;
        }

        @media (max-width: 992px) {
            .main-content {
                grid-template-columns: 1fr;
            }
        }

        /* Карточки */
        .card {
            background: white;
            border-radius: 10px;
            padding: 25px;
            margin-bottom: 25px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card-header {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }

        .card-header i {
            font-size: 1.5rem;
            color: var(--secondary);
            margin-right: 15px;
        }

        .card-header h2 {
            font-size: 1.4rem;
            color: var(--primary);
        }

        /* Блок программы */
        .program-card {
            border-left: 5px solid var(--success);
        }

        .program-info {
            background: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
        }

        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }

        .info-item {
            padding: 10px;
            background: #f1f8ff;
            border-radius: 5px;
        }

        .info-item strong {
            color: var(--primary);
            display: block;
            margin-bottom: 5px;
        }

        /* Файлы */
        .files-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .file-item {
            display: flex;
            align-items: center;
            padding: 15px;
            background: #f8f9fa;
            border-radius: 8px;
            border: 1px solid #e9ecef;
            transition: 0.3s;
            text-decoration: none;
            color: inherit;
        }

        .file-item:hover {
            background: #e9ecef;
            border-color: var(--secondary);
        }

        .file-icon {
            font-size: 2rem;
            color: var(--accent);
            margin-right: 15px;
        }

        .file-info h4 {
            margin-bottom: 5px;
            color: var(--primary);
        }

        .file-info span {
            font-size: 0.9rem;
            color: #666;
        }

        /* Боковая панель */
        .sidebar .card {
            position: sticky;
            top: 20px;
        }

        .teacher-info {
            text-align: center;
        }

        .teacher-photo {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid #f1f8ff;
            margin: 0 auto 20px;
        }

        .teacher-info h3 {
            color: var(--primary);
            margin-bottom: 10px;
        }

        .teacher-info p {
            color: #666;
            margin-bottom: 15px;
        }

        .contact-list {
            list-style: none;
            margin-top: 20px;
        }

        .contact-list li {
            padding: 10px 0;
            border-bottom: 1px solid #eee;
            display: flex;
            align-items: center;
        }

        .contact-list i {
            color: var(--secondary);
            margin-right: 10px;
            width: 20px;
        }

        /* Кнопки */
        .btn {
            display: inline-block;
            padding: 12px 25px;
            background: var(--secondary);
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            transition: 0.3s;
            text-decoration: none;
            text-align: center;
        }

        .btn:hover {
            background: #2980b9;
            color: white;
        }

        .btn-success {
            background: var(--success);
        }

        .btn-success:hover {
            background: #219653;
        }

        .btn-block {
            display: block;
            width: 100%;
            margin-top: 15px;
        }

        /* Футер */
        footer {
            background: var(--dark);
            color: white;
            padding: 40px 0 20px;
            margin-top: 50px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }

        .footer-section h3 {
            margin-bottom: 20px;
            font-size: 1.2rem;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 10px;
        }

        .footer-section a {
            color: #ddd;
            text-decoration: none;
            transition: 0.3s;
        }

        .footer-section a:hover {
            color: white;
            padding-left: 5px;
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #444;
            color: #aaa;
            font-size: 0.9rem;
        }

        /* Адаптивность */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .info-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Модальное окно */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background: white;
            padding: 30px;
            border-radius: 10px;
            max-width: 500px;
            width: 90%;
            max-height: 80vh;
            overflow-y: auto;
        }

        .close-modal {
            float: right;
            font-size: 1.5rem;
            cursor: pointer;
            color: #666;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
        }

        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }

        .form-group textarea {
            min-height: 120px;
            resize: vertical;
        }
    </style>
</head>
<body>
    <!-- Шапка -->
    <header>
        <div class="container header-content">
            <div class="logo">
                <i class="fas fa-chalkboard-teacher"></i>
                <div>
                    <h1>Портфолио педагога ДО</h1>
                    <span>Официальный сайт-портфолио</span>
                </div>
            </div>
            <nav>
                <ul>
                    <li><a href="#program">Рабочая программа</a></li>
                    <li><a href="#materials">Материалы</a></li>
                    <li><a href="#achievements">Достижения</a></li>
                    <li><a href="#contacts">Контакты</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <div class="container">
        <div class="main-content">
            <!-- Основная часть -->
            <main>
                <!-- Рабочая программа -->
                <section id="program" class="card program-card">
                    <div class="card-header">
                        <i class="fas fa-file-alt"></i>
                        <h2>Рабочая программа дополнительного образования</h2>
                    </div>
                    
                    <div class="program-info">
                        <h3>«Столярный олимп»</h3>
                        <p><strong>Направленность:</strong> Техническая</p>
                        <p><strong>Уровень:</strong> Стартовый</p>
                        <p><strong>Возраст обучающихся:</strong> 11-12 лет (6 класс)</p>
                        <p><strong>Срок реализации:</strong> 1 год (72 часа)</p>
                    </div>

                    <div class="info-grid">
                        <div class="info-item">
                            <strong>Цель программы:</strong>
                            <p>Формирование устойчивых навыков безопасной работы с инструментами, развитие творческих и технических способностей через проектирование и изготовление изделий из конструкционных материалов.</p>
                        </div>
                        <div class="info-item">
                            <strong>Задачи:</strong>
                            <p>• Освоение технологий обработки древесины и металла<br>
                            • Развитие проектного мышления<br>
                            • Воспитание культуры труда</p>
                        </div>
                        <div class="info-item">
                            <strong>Планируемые результаты:</strong>
                            <p>• Умение читать чертежи<br>
                            • Навыки работы с инструментами<br>
                            • Создание творческих проектов</p>
                        </div>
                        <div class="info-item">
                            <strong>Формы аттестации:</strong>
                            <p>• Защита проектов<br>
                            • Выставка работ<br>
                            • Контрольные задания</p>
                        </div>
                    </div>

                    <h3 style="margin: 25px 0 15px;">Учебно-тематический план</h3>
                    <div style="overflow-x: auto;">
                        <table style="width: 100%; border-collapse: collapse;">
                            <thead style="background: #f1f8ff;">
                                <tr>
                                    <th style="padding: 12px; border: 1px solid #ddd;">Раздел</th>
                                    <th style="padding: 12px; border: 1px solid #ddd;">Часы</th>
                                    <th style="padding: 12px; border: 1px solid #ddd;">Теория</th>
                                    <th style="padding: 12px; border: 1px solid #ddd;">Практика</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td style="padding: 10px; border: 1px solid #ddd;">Вводный блок</td>
                                    <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">4</td>
                                    <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">2</td>
                                    <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">2</td>
                                </tr>
                                <tr style="background: #f9f9f9;">
                                    <td style="padding: 10px; border: 1px solid #ddd;">Основы мастерства</td>
                                    <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">20</td>
                                    <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">6</td>
                                    <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">14</td>
                                </tr>
                                <tr>
                                    <td style="padding: 10px; border: 1px solid #ddd;">Проектная деятельность</td>
                                    <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">38</td>
                                    <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">4</td>
                                    <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">34</td>
                                </tr>
                                <tr style="background: #f9f9f9;">
                                    <td style="padding: 10px; border: 1px solid #ddd;"><strong>Итого:</strong></td>
                                    <td style="padding: 10px; border: 1px solid #ddd; text-align: center;"><strong>72</strong></td>
                                    <td style="padding: 10px; border: 1px solid #ddd; text-align: center;"><strong>19</strong></td>
                                    <td style="padding: 10px; border: 1px solid #ddd; text-align: center;"><strong>53</strong></td>
                                </tr>
                            </tbody>
                        </table>
                    </div>

                    <button class="btn btn-block" onclick="openModal('editModal')">
                        <i class="fas fa-edit"></i> Редактировать программу
                    </button>
                </section>

                <!-- Материалы и файлы -->
                <section id="materials" class="card">
                    <div class="card-header">
                        <i class="fas fa-folder-open"></i>
                        <h2>Материалы и документы</h2>
                    </div>

                    <div class="files-container">
                        <a href="#" class="file-item">
                            <div class="file-icon">
                                <i class="fas fa-file-pdf"></i>
                            </div>
                            <div class="file-info">
                                <h4>Рабочая программа (полный текст)</h4>
                                <span>PDF, 450 КБ • Обновлено: 01.09.2024</span>
                            </div>
                        </a>

                        <a href="#" class="file-item">
                            <div class="file-icon">
                                <i class="fas fa-file-word"></i>
                            </div>
                            <div class="file-info">
                                <h4>Календарно-тематическое планирование</h4>
                                <span>DOCX, 120 КБ • Обновлено: 25.08.2024</span>
                            </div>
                        </a>

                        <a href="#" class="file-item">
                            <div class="file-icon">
                                <i class="fas fa-file-excel"></i>
                            </div>
                            <div class="file-info">
                                <h4>Мониторинг результатов</h4>
                                <span>XLSX, 85 КБ • Обновлено: 15.08.2024</span>
                            </div>
                        </a>

                        <a href="#" class="file-item">
                            <div class="file-icon">
                                <i class="fas fa-file-powerpoint"></i>
                            </div>
                            <div class="file-info">
                                <h4>Презентация программы для родителей</h4>
                                <span>PPTX, 2.1 МБ • Обновлено: 20.08.2024</span>
                            </div>
                        </a>
                    </div>

                    <button class="btn btn-block" onclick="openModal('uploadModal')">
                        <i class="fas fa-upload"></i> Загрузить новый документ
                    </button>
                </section>

                <!-- Достижения -->
                <section id="achievements" class="card">
                    <div class="card-header">
                        <i class="fas fa-trophy"></i>
                        <h2>Достижения и результаты</h2>
                    </div>
                    
                    <div class="info-grid">
                        <div class="info-item">
                            <strong>Участие в конкурсах:</strong>
                            <p>• Городская выставка технического творчества (2024) - 2 место</p>
                            <p>• Областной конкурс "Мастер года" (2023) - участник</p>
                        </div>
                        <div class="info-item">
                            <strong>Публикации:</strong>
                            <p>• Статья в журнале "Дополнительное образование"</p>
                            <p>• Методическая разработка на сайте Инфоурок</p>
                        </div>
                    </div>
                    
                    <h3 style="margin: 20px 0 15px;">Фотогалерея работ учащихся</h3>
                    <div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); gap: 10px;">
                        <div style="background: #eee; height: 150px; border-radius: 8px; display: flex; align-items: center; justify-content: center;">
                            <i class="fas fa-image fa-2x" style="color: #aaa;"></i>
                        </div>
                        <div style="background: #eee; height: 150px; border-radius: 8px; display: flex; align-items: center; justify-content: center;">
                            <i class="fas fa-image fa-2x" style="color: #aaa;"></i>
                        </div>
                        <div style="background: #eee; height: 150px; border-radius: 8px; display: flex; align-items: center; justify-content: center;">
                            <i class="fas fa-image fa-2x" style="color: #aaa;"></i>
                        </div>
                    </div>
                </section>
            </main>

            <!-- Боковая панель -->
            <aside class="sidebar">
                <div class="card teacher-info">
                    <img src="https://via.placeholder.com/150" alt="Фото педагога" class="teacher-photo">
                    <h3>Евланов Артём Дмитриевич</h3>
                    <p><strong>Педагог дополнительного образования</strong></p>
                    <p>Квалификационная категория: Первая</p>
                    <p>Стаж работы: 1 год</p>
                    
                    <ul class="contact-list">
                        <li><i class="fas fa-graduation-cap"></i> МБОУ СОШ №10 г. Коломна</li>
                        <li><i class="fas fa-envelope"></i> amigo228007@yandex.ru</li>
                        <li><i class="fas fa-phone"></i> +7 (XXX) XXX-XX-XX</li>
                        <li><i class="fas fa-map-marker-alt"></i> Кабинет технологии №25</li>
                    </ul>
                    
                    <a href="#contacts" class="btn btn-block">Связаться со мной</a>
                </div>

                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-info-circle"></i>
                        <h2>Быстрая информация</h2>
                    </div>
                    <p><strong>Программа в Навигаторе:</strong> Да</p>
                    <p><strong>ID программы в Навигаторе:</strong> 12345</p>
                    <p><strong>Финансирование:</strong> Бюджетное + ПФДО</p>
                    <p><strong>Количество обучающихся:</strong> 15</p>
                    <p><strong>Расписание:</strong> Вт, Чт 15:00-16:30</p>
                </div>
            </aside>
        </div>
    </div>

    <!-- Контакты -->
    <section id="contacts" style="background: #f1f8ff; padding: 40px 0;">
        <div class="container">
            <div class="card">
                <div class="card-header">
                    <i class="fas fa-envelope"></i>
                    <h2>Связь с педагогом</h2>
                </div>
                <p>Для связи по вопросам программы, записи в кружок или сотрудничества:</p>
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin-top: 20px;">
                    <div>
                        <h3>Контактная информация</h3>
                        <p><i class="fas fa-school"></i> <strong>Учреждение:</strong> МБОУ СОШ №10 г. Коломна</p>
                        <p><i class="fas fa-clock"></i> <strong>Консультационные часы:</strong> Среда 14:00-16:00</p>
                        <p><i class="fas fa-external-link-alt"></i> <strong>Страница в Навигаторе:</strong> <a href="#">перейти</a></p>
                    </div>
                    <div>
                        <h3>Форма обратной связи</h3>
                        <div class="form-group">
                            <input type="text" placeholder="Ваше имя" style="margin-bottom: 10px;">
                        </div>
                        <div class="form-group">
                            <input type="email" placeholder="Ваш email" style="margin-bottom: 10px;">
                        </div>
                        <div class="form-group">
                            <textarea placeholder="Ваше сообщение"></textarea>
                        </div>
                        <button class="btn">Отправить сообщение</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Футер -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>О портале</h3>
                    <p>Официальный сайт-портфолио педагога дополнительного образования. Все материалы защищены авторским правом.</p>
                </div>
                <div class="footer-section">
                    <h3>Быстрые ссылки</h3>
                    <ul>
                        <li><a href="#program">Рабочая программа</a></li>
                        <li><a href="#materials">Документы</a></li>
                        <li><a href="#achievements">Достижения</a></li>
                        <li><a href="#contacts">Контакты</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Полезные ресурсы</h3>
                    <ul>
                        <li><a href="https://navigator.edu.ru" target="_blank">Навигатор ДОД</a></li>
                        <li><a href="https://edu.gov.ru" target="_blank">Минпросвещения РФ</a></li>
                        <li><a href="https://dop.edu.ru" target="_blank">Портал ДО</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>© 2024 Портфолио педагога дополнительного образования. МБОУ СОШ №10 г. Коломна.</p>
            </div>
        </div>
    </footer>

    <!-- Модальное окно редактирования программы -->
    <div id="editModal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal('editModal')">&times;</span>
            <h2>Редактирование рабочей программы</h2>
            
            <form id="editProgramForm">
                <div class="form-group">
                    <label>Название программы:</label>
                    <input type="text" value="«Столярный олимп»" required>
                </div>
                
                <div class="form-group">
                    <label>Направленность:</label>
                    <select required>
                        <option value="technical" selected>Техническая</option>
                        <option value="art">Художественная</option>
                        <option value="sport">Физкультурно-спортивная</option>
                        <option value="science">Естественнонаучная</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label>Уровень:</label>
                    <select required>
                        <option value="start" selected>Стартовый</option>
                        <option value="basic">Базовый</option>
                        <option value="advanced">Продвинутый</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label>Возраст обучающихся:</label>
                    <input type="text" value="11-12 лет (6 класс)" required>
                </div>
                
                <div class="form-group">
                    <label>Срок реализации (часы):</label>
                    <input type="number" value="72" required>
                </div>
                
                <div class="form-group">
                    <label>Цель программы:</label>
                    <textarea required>Формирование устойчивых навыков безопасной работы с инструментами, развитие творческих и технических способностей через проектирование и изготовление изделий из конструкционных материалов.</textarea>
                </div>
                
                <div class="form-group">
                    <label>Основные задачи:</label>
                    <textarea required>• Освоение технологий обработки древесины и металла
• Развитие проектного мышления
• Воспитание культуры труда и аккуратности
• Формирование навыков безопасной работы в мастерской</textarea>
                </div>
                
                <button type="submit" class="btn btn-success">Сохранить изменения</button>
                <button type="button" class="btn" onclick="closeModal('editModal')" style="background: #95a5a6; margin-left: 10px;">Отмена</button>
            </form>
        </div>
    </div>

    <!-- Модальное окно загрузки файлов -->
    <div id="uploadModal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal('uploadModal')">&times;</span>
            <h2>Загрузка документа</h2>
            
            <form id="uploadForm">
                <div class="form-group">
                    <label>Название документа:</label>
                    <input type="text" placeholder="Например: Рабочая программа 2024-2025" required>
                </div>
                
                <div class="form-group">
                    <label>Тип документа:</label>
                    <select required>
                        <option value="">Выберите тип</option>
                        <option value="program">Рабочая программа</option>
                        <option value="plan">Календарно-тематический план</option>
                        <option value="presentation">Презентация</option>
                        <option value="methodology">Методическая разработка</option>
                        <option value="report">Отчет</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label>Описание документа:</label>
                    <textarea placeholder="Краткое описание содержимого файла"></textarea>
                </div>
                
                <div class="form-group">
                    <label>Выберите файл:</label>
                    <input type="file" required style="padding: 5px;">
                    <small>Допустимые форматы: PDF, DOC, DOCX, PPT, XLS (макс. 10 МБ)</small>
                </div>
                
                <button type="submit" class="btn btn-success">Загрузить документ</button>
                <button type="button" class="btn" onclick="closeModal('uploadModal')" style="background: #95a5a6; margin-left: 10px;">Отмена</button>
            </form>
        </div>
    </div>

    <script>
        // Управление модальными окнами
        function openModal(modalId) {
            document.getElementById(modalId).style.display = 'flex';
        }
        
        function closeModal(modalId) {
            document.getElementById(modalId).style.display = 'none';
        }
        
        // Закрытие модального окна при клике вне его
        window.onclick = function(event) {
            if (event.target.className === 'modal') {
                event.target.style.display = 'none';
            }
        }
        
        // Обработка форм
        document.getElementById('editProgramForm')?.addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Изменения сохранены!');
            closeModal('editModal');
            // Здесь можно добавить отправку данных на сервер
        });
        
        document.getElementById('uploadForm')?.addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Документ успешно загружен!');
            closeModal('uploadModal');
            // Здесь можно добавить загрузку файла на сервер
        });
        
        // Плавная прокрутка к якорям
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                if (targetId.startsWith('#')) {
                    document.querySelector(targetId).scrollIntoView({
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Обновление текущего года в футере
        document.addEventListener('DOMContentLoaded', function() {
            const yearElements = document.querySelectorAll('.copyright p');
            yearElements.forEach(el => {
                el.innerHTML = el.innerHTML.replace('2024', new Date().getFullYear());
            });
        });
    </script>
</body>
</html>
