# Junior+ Fullstack-developer Фарбак Дана

---

## Contacts

- **Telegram**: [@shereposhek](https://t.me/shereposhek)
- **Discord**: shereposhek

## About me

Начала своё путешевствие в IT со школы случайно попав на интересующие меня тогда курсы по вёрстке, на сегодняшний день нахожусь в обучении уже 6 лет.

- **Цели и приоритеты** саморазвитие, карьерный рост
- **Сильные стороны** высокая скорость обучения, адаптивность
- **Опыт работы** разработка enterprize-платформы для B2B компании в роли Fullstack разработчика в тандеме с CI\CD

## Hard skills

- **Языки**: PHP, Js. **В меньшей степени знакома с**: C, C#, C++, 1C, 1C-битрикс
- **Фреймворки**: Laravel, Symfony, Vue. **В меньшей степени знакома с**: React, Node
- **Системы контроля версий**: git

## Примеры кода

Функция вывода статистики пользователя

```php
public function statistics(){
        $user = Auth::user();

        $totalCourses = $user->courses()->count();
        $completedCourses = $user->userCourses()->where('progress_delta', 100)->count();
        $totalFiles = $user->completedFiles()->where('status', \App\Enums\StatusEnum::COMPLETED->value)->count();
        $totalTests = $user->testResults()->where('passed', \App\Enums\TestPassedEnum::PASSED->value)->count();

        return response()->json([
            'total_courses' => $totalCourses,
            'completed_courses' => $completedCourses,
            'completion_rate' => $totalCourses>0 ? round(($completedCourses/$totalCourses)*100, 2) : 0,
            'total_files_completed' => $totalFiles,
            'total_tests_passed' => $totalTests,
            'bonus_points' => $user->bonus_points,
        ]);
    }
```

## Work expirience

Кусочек кода относится к enterprize-платформе находящейся в интранете компании поэтому предоставить ссылку на него я не могу.

## Eduсation

Пермский авиационный техникум им А.Д.Швецова "Разработчик веб и мультимедийных приложений" 2026г.

## English language

**B1-B2**
