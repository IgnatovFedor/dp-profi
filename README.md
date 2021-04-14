## Основная задача

Разработать модель для определения тем реплик на протяжении диалога.

### Данные

- `data/1.csv` - размеченные данные 
- `data/2.csv` - неразмеченные данные
- `data/3.csv` - тестовые данные (станет доступен в 10:00 15.04.21)

Диалоги взяты из https://github.com/alexa/Topical-Chat


### Столбцы:
- `utterance_id` - номер сообщения
- `conversation_id` - номер диалога
- `agent` - автор сообщения (`agent_1` или `agent_2`)
- `message` - текст сообщения
- `topic` - тема сообщения

### Список тем

- Art_Event
- Celebrities
- Entertainment
- Fashion
- Food_Drink
- Games
- Literature
- Movies_TV
- Music
- News
- Other
- Pets_Animals
- Phatic
- Politics
- Psychology
- Religion
- SciTech
- Sports
- Travel_Geo
- Weather_Time

### Оценка качества модели

F1-micro (sklearn.metrics.f1_score с `average='micro'`)

## Дополнительная задача

Предложить алгоритм определения момента, когда бот теряет пользователя внутри заданной темы в процессе диалога.

### Данные:

`data/deepy.csv` 

### Столбцы:

- `utterance_id` - номер сообщения
- `conversation_id` - номер диалога
- `agent` - автор сообщения (`human` или `bot`)
- `message` - текст сообщения

### Оценка решения:

Оценка эксперта на основании презентации. Презентация пройдет в 14.00. Максимальный балл за решение: `0.2`

## Итоговая оценка

Складывается суммы F1-micro за основную задачу и оценки эксперта за дополнительную.
