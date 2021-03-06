---
title: "Задачи синтеза фотореалистичных изображений "
order: 0
category: 1. Введение
---

Существуют два основных направления создания цифровых изображений (рендеринга): для
их автоматического анализа и для показа человеку. При создании
изображения для компьютерного анализа не требуется показывать его на
экране, достаточно создать матрицу цветовых значений и передать его
соответствующей программе. 

![Синтезированное
изображение. Высокий уровень реализма обеспечивается моделированием
большого количества разнообразных эффектов взаимодействия света с
материалами окружающего мира, высокой точностью самого расчёта и,
наконец, учётом модели фотоаппарата - т. е. того как формируется
итоговое «JPEG» изображение из значений освещённости ячеек матрицы
фотоаппарата.](/images/osi_lecnotes_rt/56.jpg){#fig:figureRefA}


Когда изображение создаётся для показа
человеку, задача становится намного сложнее. Вне зависимости от
конкретной цели, которая приводит к созданию изображения, основная
задача - это информационная коммуникация с другим человеком. А если
требуется передать человеку визуальную информацию, необходимо провести
изображение через зрительную систему этого человека. 

Что нужно чтобы научиться с помощью компьютера синтезировать
изображения, неотличимые от реальности ([@fig:figureRefA])? 

Для этого необходимо создать набор цифровых
моделей, которые с определённым уровнем достоверности позволяют
воссоздать те же процессы, что происходят в реальности. Что же это за
модели? Часть ответа заключена в самом вопросе, а именно
в слове «неотличимые». Похожа картинка на реальность, или нет,
решают наши и глаза и наш мозг. Поэтому первым и одним из ключевых
элементов синтеза фотореалистичных изображений является понимание
принципов функционирования человеческой зрительной системы. Это позволит
создать модель зрительного механизма, генерирующую изображения,
аналогичные тем, которые формируют наши глаза и мозг, получая информацию
из реального мира. Подавая изображение «на вход» системы «глаза-мозг»,
мы и добьёмся желаемой цели -- создания ощущения полной реалистичности
синтезированного изображения. Заметим, что эта же задача решается в
фотоаппаратах, поэтому часто удобно рассматривать процесс синтеза
изображения через создание модели виртуального фотоаппарата, а не глаза.
Остаётся рассчитать сколько света придёт на каждый светочувствительный
элемент фотоаппарата/глаза.

\newpage 
Основная задача реалистичной компьютерной графики --- воспроизвести на
мониторе изображение модели (объекта), неотличимое от наблюдаемого
глазом. В случае виртуального мира можно говорить о задаче создания
изображения объекта, неотличимого от реальности (как если бы объект
существовал в реальности). Для решения этой задачи необходимо, как
минимум, численно измерить свет, попадающий на чувствительный элемент
глаза или камеры.

Но это ещё не всё: одних лишь физических расчётов или измерений
недостаточно. Необходимо также знать, как устроено человеческое
восприятие цвета. В главе
[\[colorchapter\]](#colorchapter){reference-type="ref"
reference="colorchapter"} мы увидим, что цвет - субъективное для
человека восприятие спектра, которое, однако имеет множество различных
математических моделей. В главе
[\[hdrchapter\]](#hdrchapter){reference-type="ref"
reference="hdrchapter"} мы увидим, что на самом деле и этого
(моделирование физики света в совокупности с восприятием цвета)
недостаточно. Как правило, нужно уметь моделировать всю графическую
систему: получение изображения на матрице камеры, хранения и обработка,
вывод изображения на монитор ([рисунок @fig:fig2]).
и, наконец, особенности человечесткого восприятия. В первой главе мы
сосредоточимся на свете - известном и хорошо изученном физикой явлении.


![Типичная
графическая система и операции со светом и
цветом](/images/osi_lectnotes_radiometry_photometry/graphical_system.png){#fig:fig2}
