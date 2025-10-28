<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Опросник продуктивности сотрудников</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 20px;
    background: #f5f5f5;
    line-height: 1.4;
  }
  h1 {
    font-size: 1.5em;
    color: #333;
    text-align: center;
  }
  p {
    font-size: 1em;
    margin-bottom: 20px;
  }
  .question {
    background: #fff;
    padding: 10px 15px;
    margin-bottom: 15px;
    border-radius: 5px;
  }
  .question p {
    margin-bottom: 10px;
  }
  label {
    display: block;
    margin: 5px 0;
    font-size: 0.9em;
  }
  #result {
    margin-top: 30px;
    font-weight: bold;
    font-size: 1em;
  }
  button {
    display: block;
    width: 100%;
    max-width: 200px;
    margin: 20px auto;
    padding: 10px;
    font-size: 1em;
    cursor: pointer;
    background: #4CAF50;
    color: #fff;
    border: none;
    border-radius: 5px;
  }
  button:hover {
    background: #45a049;
  }
  @media(max-width: 600px) {
    body {
      margin: 10px;
    }
    h1 {
      font-size: 1.3em;
    }
  }
</style>
</head>
<body>
<h1>Опросник продуктивности сотрудников</h1>
<p>Ответьте на все вопросы максимально честно. По окончании теста вы сразу увидите результаты.</p>
<form id="quizForm">
  <!-- Вопросы (оставьте как есть) -->
  <div class="question">
    <p>1. Как вы оцениваете свой уровень продуктивности на работе?</p>
    <label><input type="radio" name="q1" value="0" required> Очень высокий</label>
    <label><input type="radio" name="q1" value="1"> Скорее высокий</label>
    <label><input type="radio" name="q1" value="2"> Средний</label>
    <label><input type="radio" name="q1" value="3"> Скорее низкий</label>
    <label><input type="radio" name="q1" value="4"> Очень низкий</label>
  </div>
  <div class="question">
    <p>2. Насколько вы удовлетворены своими основными рабочими задачами?</p>
    <label><input type="radio" name="q2" value="0" required> Полностью удовлетворён(а)</label>
    <label><input type="radio" name="q2" value="1"> Скорее да</label>
    <label><input type="radio" name="q2" value="2"> Нейтрально</label>
    <label><input type="radio" name="q2" value="3"> Скорее нет</label>
    <label><input type="radio" name="q2" value="4"> Совсем нет</label>
  </div>
  <div class="question">
    <p>3. Как часто вы испытываете усталость или выгорание на работе?</p>
    <label><input type="radio" name="q3" value="0" required> Почти никогда</label>
    <label><input type="radio" name="q3" value="1"> Иногда</label>
    <label><input type="radio" name="q3" value="2"> Часто</label>
    <label><input type="radio" name="q3" value="3"> Почти всегда</label>
  </div>
  <div class="question">
    <p>4. Насколько ваша рабочая нагрузка соответствует вашим силам?</p>
    <label><input type="radio" name="q4" value="0" required> Слишком низкая</label>
    <label><input type="radio" name="q4" value="1"> Оптимальная</label>
    <label><input type="radio" name="q4" value="2"> Повышенная</label>
    <label><input type="radio" name="q4" value="3"> Чрезмерная</label>
  </div>
  <div class="question">
    <p>5. Понимаете ли вы свои цели и приоритеты в работе?</p>
    <label><input type="radio" name="q5" value="0" required> Очень чётко</label>
    <label><input type="radio" name="q5" value="1"> Скорее чётко</label>
    <label><input type="radio" name="q5" value="2"> Иногда неясно</label>
    <label><input type="radio" name="q5" value="3"> Совсем неясно</label>
  </div>
  <div class="question">
    <p>6. Как вы оцениваете эффективность коммуникации в вашей команде?</p>
    <label><input type="radio" name="q6" value="0" required> Очень высокая</label>
    <label><input type="radio" name="q6" value="1"> Достаточно</label>
    <label><input type="radio" name="q6" value="2"> Средняя</label>
    <label><input type="radio" name="q6" value="3"> Низкая</label>
    <label><input type="radio" name="q6" value="4"> Очень низкая</label>
  </div>
  <div class="question">
    <p>7. Достаточно ли у вас ресурсов (время, информация, поддержка, технологии)?</p>
    <label><input type="radio" name="q7" value="0" required> Полностью</label>
    <label><input type="radio" name="q7" value="1"> В основном</label>
    <label><input type="radio" name="q7" value="2"> Частично</label>
    <label><input type="radio" name="q7" value="3"> Скорее нет</label>
    <label><input type="radio" name="q7" value="4"> Совсем нет</label>
  </div>
  <div class="question">
    <p>8. Какие факторы чаще всего снижают вашу продуктивность? (можно выбрать несколько)</p>
    <label><input type="checkbox" name="q8" value="1"> Перегрузка задачами</label>
    <label><input type="checkbox" name="q8" value="1"> Неясные цели / приоритеты</label>
    <label><input type="checkbox" name="q8" value="1"> Недостаток мотивации</label>
    <label><input type="checkbox" name="q8" value="1"> Слабая коммуникация</label>
    <label><input type="checkbox" name="q8" value="1"> Стресс / конфликты</label>
    <label><input type="checkbox" name="q8" value="1"> Недостаток ресурсов</label>
  </div>
  <div class="question">
    <p>9. Как часто отвлекают внешние факторы (личные дела, соцсети, шум)?</p>
    <label><input type="radio" name="q9" value="0" required> Почти никогда</label>
    <label><input type="radio" name="q9" value="1"> Иногда</label>
    <label><input type="radio" name="q9" value="2"> Часто</label>
    <label><input type="radio" name="q9" value="3"> Почти всегда</label>
  </div>
  <div class="question">
    <p>10. Насколько вы готовы участвовать в мероприятиях для повышения продуктивности?</p>
    <label><input type="radio" name="q10" value="0" required> Да</label>
    <label><input type="radio" name="q10" value="1"> Возможно</label>
    <label><input type="radio" name="q10" value="2"> Нет</label>
  </div>
</form>

<div id="result"></div>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    const form = document.getElementById('quizForm');
    const totalQuestions = 10; // количество вопросов
    const resultDiv = document.getElementById('result');

    // при выборе ответов на 10 вопрос автоматически показывать результат
    for (let i = 1; i <= totalQuestions; i++) {
      const radios = document.getElementsByName('q' + i);
      radios.forEach(r => {
        r.addEventListener('change', function() {
          // только после 10-го вопроса
          if (i === totalQuestions) {
            calculateScore();
          }
        });
      });
    }

    function getCategoryAndAdvice(score) {
      let category, advice;
      if (score <= 8) {
        category = 'Высокая продуктивность';
        advice = 'Вы эффективно справляетесь с задачами, минимальные проблемы.';
      } else if (score <= 16) {
        category = 'Средняя продуктивность';
        advice = 'Есть факторы снижения эффективности; рекомендуется оптимизировать рабочие процессы.';
      } else if (score <= 25) {
        category = 'Низкая продуктивность';
        advice = 'Замечаются серьёзные проблемы: высокая нагрузка, усталость, нехватка ресурсов.';
      } else {
        category = 'Критическая ситуация';
        advice = 'Необходимы срочные меры: оптимизация процессов, поддержка и мотивация.';
      }
      return { category, advice };
    }

    function buildRecommendations(category) {
      switch (category) {
        case 'Высокая продуктивность':
          return [
            'Продолжайте поддерживать эффективные привычки (планирование, отдых, приоритеты).',
            'Регулярно делайте короткие перерывы и избегайте долгих периодов непрерывной работы.',
            'Поддерживайте ясность целей и баланс между работой и личной жизнью.'
          ];
        case 'Средняя продуктивность':
          return [
            'Идентифицируйте факторы снижения и устраните их по возможности.',
            'Установите конкретные ежедневные цели и тайм-блоки.',
            'Снизьте отвлекающие факторы и улучшите коммуникацию в команде.'
          ];
        case 'Низкая продуктивность':
          return [
            'Перераспределите нагрузку и приоритеты; подумайте об делегировании.',
            'Улучшите режим работы: расписание, сон, перерывы.',
            'Задайте понятные цели, обратную связь и поддержку со стороны коллег.'
          ];
        case 'Критическая ситуация':
          return [
            'Немедленно обсудите перераспределение задач и приоритетов с руководителем.',
            'Установите временные рамки снижения нагрузки и поиска поддержки.',
            'Рассмотрите помощь HR/коучинга и при необходимости психологическую поддержку.'
          ];
        default:
          return [];
      }
    }

    function calculateScore() {
      let score = 0;
      // Радиокнопки
      for(let i=1; i<=totalQuestions; i++){
        let radios = document.getElementsByName('q'+i);
        for(let r of radios){
          if(r.checked){
            const val = parseInt(r.value, 10);
            score += val;
          }
        }
      }
      // Чекбоксы (вопрос 8)
      let q8boxes = document.querySelectorAll('input[name="q8"]:checked');
      for(let box of q8boxes){
        const val = parseInt(box.value, 10) || 0;
        score += val;
      }

      const { category, advice } = getCategoryAndAdvice(score);
      const recs = buildRecommendations(category);
      resultDiv.innerHTML = `
        <p>Ваш результат: <strong>${category}</strong> (${score} баллов)</p>
        <p>${advice}</p>
        <div class="rec">
          <strong>Рекомендации:</strong>
          <ul>${recs.map(r => `<li>${r}</li>`).join('')}</ul>
        </div>
      `;
    }
  });
</script>
</body>
</html>
