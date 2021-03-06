# Штучні нейронні мережі для обробки природних мов

### Що таке штучна нейронна мережа? Як це працює? Які види штучних нейронних мереж існують? Яким чином різні типи штучних нейронних мереж використовуються для обробки природних мов?

Штучна нейронна мережа - це обчислювальна нелінійна модель, заснована на нейронній структурі мозку, яка здатна навчитися виконувати такі завдання, як класифікація, прогнозування, прийняття рішень, візуалізація та інше.

Штучна нейронна мережа складається із штучних нейронів чи елементів обробки та організована у три взаємопов’язані шари: вхідний, прихований, який може включати більше одного шару, та вихідний.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/46/Colored_neural_network.svg/800px-Colored_neural_network.svg.png)

### [Штучна нейронна мережа](https://uk.wikipedia.org/wiki/%D0%A8%D1%82%D1%83%D1%87%D0%BD%D0%B0_%D0%BD%D0%B5%D0%B9%D1%80%D0%BE%D0%BD%D0%BD%D0%B0_%D0%BC%D0%B5%D1%80%D0%B5%D0%B6%D0%B0)

Вхідний шар містить вхідні нейрони, які надсилають інформацію до прихованого шару. Прихований шар надсилає дані на вихідний рівень. Кожен нейрон має зважені входи (синапси), функцію активації (визначає вихід із заданим входом) та один вихід. Синапси - це регульовані параметри, які перетворюють нейронну мережу в параметризовану систему.

![](http://en.citizendium.org/images/f/f3/Artificialneuron.png)

## Приклади ШНМ

### 1.Multilayer perceptron (MLP)

1[](https://upload.wikimedia.org/wikipedia/ru/d/de/Neuro.PNG)

Багатошаровий perceptron (MLP) має три або більше шарів. Він використовує нелінійну функцію активації (головним чином гіперболічну дотичну або логістичну функцію), що дозволяє класифікувати дані, які не є лінійно відокремлюваними. Кожен вузол у шарі з'єднується з кожним вузлом у наступному шарі, роблячи мережу повністю зв'язаною. Наприклад, багатошарові програми перцептронної обробки мови (NLP) - це розпізнавання мовлення та машинний переклад.

### 2.Convolutional neural network (CNN)

![](https://upload.wikimedia.org/wikipedia/commons/6/63/Typical_cnn.png)

Конволюційна нейронна мережа (Convolutional neural network/CNN) містить один або більше згорткових шарів, об'єднаних або повністю пов'язаних, і використовує варіації багатошарових перцептронів, обговорених вище. Конволюційні шари використовують операцію згортання на вхід, передаючи результат наступному шару. Ця операція дозволяє зробити мережу глибшою із значно меншими параметрами.

Конволюційні нейронні мережі демонструють неабиякі результати в застосуванні зображень та мовлення. Йон Кім у «Конволюційних нейронних мережах для класифікації вироків» описує процес та результати завдань класифікації тексту за допомогою CNN . Він представляє модель, побудовану поверх word2vec, проводить з нею низку експериментів і тестує її на кількох орієнтирах, демонструючи, що модель працює чудово.

У "Text Understanding from Scratch" Xiang Zhang (Сиян Занг) та Yann LeCun (Ян Ле Кун) демонструють, що CNN можуть досягти видатних результатів без знання слів, фраз, речень та будь-яких інших синтаксичних чи семантичних структур стосовно людської мови. Семантичний аналіз, виявлення парафрази, розпізнавання мови - це також програми CNN.

### 3.Recursive neural network (RNN)

![](https://neurohive.io/wp-content/uploads/2018/10/rekursivnaja-neironnaja-set-533x422.png)

Рекурсивна нейронна мережа (RNN) - це тип глибокої нейронної мережі, сформованої шляхом застосування одного і того ж набору ваг рекурсивно над структурою, щоб зробити структуроване прогнозування вхідних структур змінного розміру або скалярне передбачення на ньому шляхом проходження заданої структури в топологічному порядку. У найпростішій архітектурі нелінійність, наприклад, тан і вагова матриця, що ділиться по всій мережі, використовуються для об'єднання вузлів у батьків.

### 4.Recurrent neural network (RNN)

Рекурентна нейронна мережа (RNN), на відміну від нейронної мережі, що подається, є варіантом рекурсивної штучної нейронної мережі, в якій зв’язки між нейронами здійснюють спрямований цикл. Це означає, що вихід залежить не тільки від теперішніх входів, але і від стану нейронів попереднього кроку. Ця пам'ять дозволяє користувачам вирішувати проблеми NLP, як-от підключення розпізнавання рукописного вводу або розпізнавання мови. У статті "Генерування природних мов, перефразовування та узагальнення відгуків користувачів з періодичними нейронними мережами" автори демонструють модель періодичної нейронної мережі (RNN), яка може генерувати нові пропозиції та резюме документа.

Siwei Lai (Сівей Лай), Liheng Xu (Ліхен Сю), Kang Liu (Кан Лю) і Jun Zhao (Джун Чжао) створили періодичну звивисту нейронну мережу для класифікації тексту без призначених для людини функцій і описали її в " Recurrent Convolutional Neural Networks for Text Classification". Їх модель була порівняна з існуючими методами класифікації тексту, такими як Мішок слів, Біграми + LR, SVM, LDA, Ядра дерева, Рекурсивна нейронна мережа та CNN. Було показано, що їх модель перевершує традиційні методи для всіх використовуваних наборів даних.

### 5.Long short-term memory (LSTM)

![](https://s3.amazonaws.com/media-p.slid.es/uploads/979664/images/5617558/pasted-from-clipboard.png)

Long short-term memory (LSTM) це специфічна архітектура періодичної нейронної мережі (RNN), яка була розроблена для моделювання тимчасових послідовностей та їх далеких залежностей більш точно, ніж звичайні RNN. LSTM не використовує функцію активації в своїх періодичних компонентах, збережені значення не змінюються, а градієнт не має тенденції до зникнення під час тренування. Зазвичай одиниці LSTM реалізуються в "блоках" з кількома одиницями. Ці блоки мають три або чотири "ворота" (наприклад, вхідні ворота, ворота забуття, вихідні ворота), які керують нанесенням інформаційного потоку на логістичну функцію.

У "Long Short-Term Memory Recurrent Neural Network Architectures for Large Scale Acoustic Modeling" Hasim Sak (Хасім Сак), Andrew Senior (Ендрю Сень'ор) та Françoise Beaufays (Франсуаза Бофой) показали, що глибокі архітектури LSTM RNN досягають найсучасніших характеристик для масштабного акустичного моделювання.

У роботі "Part-of-Speech Tagging with Bidirectional Long Short-Term Memory Recurrent Neural Network" від Peilu Wang (Пейлу Ванга), Yao Qian (Яо Цяня), Frank K. Soong (Франка К. Сунга), Lei He (Лей Він) та Hai Zhao (Хай Чжао) - моделі для часткової промови (POS) було подано теги. Модель досягла продуктивності 97,40% точності маркування. Apple, Amazon, Google, Microsoft та інші компанії включили LSTM як основний елемент у свої продукти.

### 6.Sequence-to-sequence models

Зазвичай модель послідовності-послідовності складається з двох періодичних нейронних мереж: кодера, який обробляє вхід, і декодера, що виробляє вихід. Енкодер і декодер можуть використовувати однакові або різні набори параметрів.

Моделі Sequence-to-Sequence в основному використовуються в системах відповідей на питання, чатах та машинному перекладі. Такі багатошарові клітини успішно використовуються в моделях послідовності в послідовності для перекладу в навчанні "Sequence to Sequence Learning with Neural Networks study".

У "Paraphrase Detection Using Recursive Autoencoder" представлена нова рекурсивна архітектура автокодера. Уявлення - це вектори в n-мірному семантичному просторі, де фрази з подібними значеннями близькі один до одного.

### 7.Shallow neural networks

Крім глибоких нейронних мереж, неглибокі моделі також є популярними та корисними інструментами. Наприклад, word2vec - це група неглибоких двошарових моделей, які використовуються для створення вбудовування слів. Представлений у Ефективній оцінці подання слів у векторному просторі, word2vec приймає великий текст тексту як свій вхід і створює векторний простір. Кожне слово в корпусі отримує відповідний вектор у цьому просторі. Відмінна особливість полягає в тому, що слова з загальних контекстів у корпусі розташовані близько у векторному просторі.

## Висновки

У цій роботі ми описали різні варіанти штучних нейронних мереж, такі як глибокий багатошаровий персептрон (MLP), згорткова нейронна мережа (CNN), рекурсивна нейронна мережа (RNN), періодична нейронна мережа (RNN), тривала короткочасова пам'ять (LSTM ), модель послідовності до послідовності та неглибокі нейронні мережі, включаючи word2vec для вбудовування слів. Ми показали, як ці мережі функціонують і як різні типи їх використовуються в завданнях з обробки природних мов. Ми продемонстрували, що звивисті нейронні мережі в основному використовуються для завдань класифікації тексту, тоді як періодичні нейронні мережі зазвичай використовуються для генерації природних мов або машинного перекладу. У наступній частині цієї серії ми вивчимо існуючі інструменти та бібліотеки для обговорюваних типів нейронної мережі.

#### Джерела

1. http://www.aclweb.org/anthology/D14-1181

2. https://arxiv.org/pdf/1502.01710.pdf

3. http://www.aclweb.org/anthology/P15-1128

4. https://www.aclweb.org/anthology/K15-1013

5. https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/CNN_ASLPTrans2-14.pdf

6. https://en.wikipedia.org/wiki/Recursive_neural_network

7. http://www.meanotek.ru/files/TarasovDS(2)2015-Dialogue.pdf

8. https://www.aaai.org/ocs/index.php/AAAI/AAAI15/paper/view/9745/9552

9. https://wiki.inf.ed.ac.uk/twiki/pub/CSTR/ListenTerm1201415/sak2.pdf

10. https://arxiv.org/pdf/1510.06168.pdf

11. https://arxiv.org/pdf/1409.3215.pdf

12. https://nlp.stanford.edu/courses/cs224n/2011/reports/ehhuang.pdf

13. https://arxiv.org/pdf/1301.3781.pdf

14. https://medium.com/@datamonsters/artificial-neural-networks-for-natural-language-processing-part-1-64ca9ebfa3b2 
