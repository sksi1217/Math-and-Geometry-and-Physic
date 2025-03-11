# Math-and-Geometry-and-Physic


## Скаляр
### **Что такое скаляр?**
Скаляр — это математическое понятие, которое описывает одну числовую величину (например, температуру, массу, время, расстояние). Он не имеет направления, только значение.

#### Примеры скаляров:
- Температура: `25°C`
- Масса: `70 кг`
- Время: `10 секунд`
- Расстояние: `5 метров`

Все эти величины описываются одним числом и не зависят от направления.

---

### **Для чего используется скаляр?**

1. **Описание величин без направления**  
   Если вам нужно описать что-то, что не связано с направлением, вы используете скаляр. Например:
   - Сколько градусов на улице (`20°C`)?
   - Какой вес у предмета (`5 кг`)?

2. **Умножение или деление векторов**  
   Скаляр часто используется для изменения размера вектора. Например, если у вас есть вектор скорости `(3, 4)` и вы хотите его уменьшить в два раза, вы можете умножить каждый компонент вектора на скаляр `0.5`:
   ```
   (3, 4) * 0.5 = (1.5, 2)
   ```

**Вектор:**

![image](https://github.com/user-attachments/assets/eabaf6cd-b398-4588-bac0-8c6c48c6a623)


3. **Вычисление длины вектора**  
   Когда вам нужно найти длину вектора (его модуль), результатом будет скаляр. Например, длина вектора `(3, 4)` равна:
   ```
   sqrt(3^2 + 4^2) = 5
   ```
   
  **sqrt** — это обозначение функции квадратного корня в некоторых языках программирования (√);
  
   Здесь `5` — это скаляр. (Длина Вектора)

4. **Работа с физическими величинами**  
   В физике многие величины являются скалярами:
   - Энергия (`100 Дж`)
   - Работа (`50 Дж`)
   - Плотность (`2 г/см³`)

---

### **Как отличить скаляр от вектора?**

| **Признак**         | **Скаляр**                  | **Вектор**                     |
|---------------------|-----------------------------|--------------------------------|
| **Есть ли направление?** | Нет                        | Да                             |
| **Пример**          | Температура (`25°C`)       | Скорость (`5 м/с на север`)   |
| **Как записывается?**| Одно число                 | Набор чисел (координаты)       |

---

### **Простой пример использования скаляра в коде**

Вот как может использоваться скаляр в программировании:

```cpp
float temperature = 25.0f; // Скаляр: температура
float mass = 70.0f;        // Скаляр: масса

// Увеличим температуру на 5 градусов
temperature += 5.0f;

// Вычислим плотность (плотность = масса / объем)
float volume = 0.1f;       // Объем в метрах кубических
float density = mass / volume; // Скаляр: плотность
```

Здесь `temperature`, `mass`, `volume` и `density` — все скаляры, так как они представляют собой одиночные числовые значения.

---

### **Итог**

Скаляр — это просто одно число, которое описывает величину без учета направления. Он используется в математике, физике и программировании для представления таких величин, как температура, масса, время, энергия и т.д. Если вам нужно работать с величинами, которые не имеют направления, используйте скаляры!

---

Давайте разберем это пошагово и объясним так, чтобы было понятно даже новичку.

---

### Уравнение 1:
$$
V^{AB} = V^B - V^A
$$

#### Что это значит?

$$ V^A $$ - Это скорость объекта $$ A $$ (например, машина, мяч или частица).
- $$ V^B $$: Это скорость объекта $$ B $$.
- $ V^{AB} $: Это **относительная скорость** от объекта $ A $ к объекту $ B $. Она показывает, насколько быстро объект $ B $ движется относительно объекта $ A $.

Простыми словами: если вы находитесь в точке $ A $ и хотите узнать, как быстро объект $ B $ удаляется от вас (или приближается к вам), то нужно вычислить разницу между скоростями $ V^B $ и $ V^A $.

---

### Зачем это нужно?
Представьте, что два объекта ($ A $ и $ B $) сталкиваются. Чтобы понять, как они взаимодействуют, важно знать их **относительную скорость** вдоль направления столкновения. Например:
- Если объекты движутся навстречу друг другу, их относительная скорость будет больше.
- Если объекты движутся в одном направлении с одинаковой скоростью, их относительная скорость будет равна нулю.

---

### Направление столкновения ($ n $):
Теперь добавим еще одно понятие — **нормаль столкновения** ($ n $).

- $ n $: Это вектор, который указывает направление столкновения. Например, если два мяча сталкиваются, нормаль столкновения — это линия, перпендикулярная поверхности мячей в точке контакта.

Мы хотим узнать, какая часть относительной скорости $ V^{AB} $ действует именно вдоль этого направления $ n $. Для этого мы используем **проекцию вектора**.

---

### Проекция на нормаль столкновения:
Чтобы найти относительную скорость вдоль направления $ n $, нужно выполнить **скалярное произведение**:

$$
V^{AB} \cdot n = (V^B - V^A) \cdot n
$$

#### Что это значит?
- $ V^{AB} \cdot n $: Это проекция относительной скорости $ V^{AB} $ на направление $ n $.
- $ (V^B - V^A) \cdot n $: То же самое, но записано через разность скоростей.

Простыми словами: мы "вытягиваем" ту часть скорости, которая действует вдоль направления столкновения ($ n $).

---

### Пример:
Предположим:
- Скорость объекта $ A $: $ V^A = 5 \, \text{м/с} $ (движется вправо),
- Скорость объекта $ B $: $ V^B = 12 \, \text{м/с} $ (движется вправо быстрее),
- Нормаль столкновения $ n $: направлена вправо (вдоль оси $ x $).

1. Вычислим относительную скорость:
   $$
   V^{AB} = V^B - V^A = 12 - 5 = 7 \, \text{м/с}.
   $$

2. Найдем проекцию на нормаль $ n $:
   Если $ n $ направлен вправо, то проекция просто равна $ 7 \, \text{м/с} $, потому что вся относительная скорость действует вдоль $ n $.

---

### Итог:
1. Относительная скорость $ V^{AB} $ показывает, как быстро объект $ B $ движется относительно объекта $ A $.
2. Чтобы понять, как эта скорость действует вдоль направления столкновения ($ n $), мы вычисляем проекцию:
   $$
   V^{AB} \cdot n = (V^B - V^A) \cdot n.
   $$

Это позволяет нам сосредоточиться только на той части движения, которая важна для анализа столкновения.

---

### Важно запомнить:
- $ V^{AB} = V^B - V^A $: формула для относительной скорости.
- $ V^{AB} \cdot n $: проекция этой скорости на направление столкновения.
- Нормаль столкновения ($ n $) помогает определить, как объекты взаимодействуют при столкновении.

---

 # Расчет относительной скорости и импульса при столкновении

Этот документ объясняет, как вычислить относительную скорость объектов до и после столкновения, а также как использовать коэффициент реституции для моделирования физики удара.

---

## 1. Относительная скорость

Относительная скорость — это разница между скоростями двух объектов. Если у нас есть два объекта $A$ и $B$, то относительная скорость $V^{AB}$ показывает, как быстро объект $B$ движется относительно объекта $A$.

### Уравнение 1:
$$
V^{AB} = V^B - V^A
$$

- $V^A$ — скорость объекта $A$.
- $V^B$ — скорость объекта $B$.
- $V^{AB}$ — относительная скорость объекта $B$ относительно объекта $A$.

**Пример:**  
Если объект $A$ движется со скоростью $5 \, \text{м/с}$ вправо, а объект $B$ движется со скоростью $8 \, \text{м/с}$ вправо, то относительная скорость $V^{AB}$ будет:
$$
V^{AB} = 8 - 5 = 3 \, \text{м/с}.
$$

---

## 2. Нормаль столкновения

Когда два объекта сталкиваются, важно знать, как они взаимодействуют вдоль линии столкновения. Линия столкновения задается **нормалью столкновения** $n$. Это вектор, который указывает направление перпендикулярно поверхности столкновения.

Примеры:
- Если мяч ударяется о стену, нормаль столкновения будет направлена перпендикулярно стене (от стены к мячу).
- Если два шара сталкиваются, нормаль столкновения будет направлена от центра одного шара к центру другого.

Чтобы выразить относительную скорость $V^{AB}$ вдоль направления нормали $n$, используется **скалярное произведение**.

---

## 3. Скалярное произведение

Скалярное произведение позволяет найти проекцию одного вектора на другой. В нашем случае это помогает найти компоненту относительной скорости $V^{AB}$, направленную вдоль нормали $n$.

### Уравнение 2:
$$
V^{AB} \cdot n = (V^B - V^A) \cdot n
$$

Здесь:
- $V^{AB} \cdot n$ — проекция относительной скорости на нормаль $n$.
- $(V^B - V^A)$ — разница скоростей объектов $B$ и $A$.

### Уравнение 3:
Скалярное произведение двух векторов $V_1 = [x_1, y_1]$ и $V_2 = [x_2, y_2]$ вычисляется так:
$$
V_1 \cdot V_2 = x_1 \cdot x_2 + y_1 \cdot y_2
$$

**Пример:**  
Пусть $V_1 = [3, 4]$ и $V_2 = [1, 2]$. Тогда:
$$
V_1 \cdot V_2 = 3 \cdot 1 + 4 \cdot 2 = 3 + 8 = 11
$$

---

## 4. Коэффициент реституции

Реституция ($e$) — это мера "упругости" столкновения. Она показывает, насколько сильно объекты "отскакивают" друг от друга после удара. Значение $e$ находится в диапазоне от $0$ до $1$:
- $e = 0$: полностью неупругое столкновение (объекты слипаются).
- $e = 1$: полностью упругое столкновение (объекты отскакивают без потери энергии).

### Выбор коэффициента реституции:
Если участвуют два объекта $A$ и $B$, то используется минимальное значение их реституций:
$$
e = \min(A.\text{restitution}, B.\text{restitution})
$$

**Пример:**  
Если $A.\text{restitution} = 0.8$ и $B.\text{restitution} = 0.5$, то:
$$
e = \min(0.8, 0.5) = 0.5
$$

---

## 5. Закон Ньютона о реституции

Закон Ньютона о реституции связывает скорости объектов до и после столкновения через коэффициент $e$. Он гласит:
$$
v_{\text{after}} = -e \cdot v_{\text{before}}
$$

Где:
- $v_{\text{before}}$ — относительная скорость до столкновения (проекция на нормаль $n$).
- $v_{\text{after}}$ — относительная скорость после столкновения (тоже проекция на нормаль $n$).

### Применение:
1. Вычисляем относительную скорость до столкновения:
   $$
   v_{\text{before}} = (V^B - V^A) \cdot n
   $$
2. Используем закон Ньютона:
   $$
   v_{\text{after}} = -e \cdot v_{\text{before}}
   $$

---

## Пример полного расчета

Пусть:
- $V^A = [2, 3]$, $V^B = [5, 7]$,
- $n = [0.6, 0.8]$,
- $A.\text{restitution} = 0.8$, $B.\text{restitution} = 0.5$.

1. Относительная скорость:
   $$
   V^{AB} = V^B - V^A = [5 - 2, 7 - 3] = [3, 4]
   $$

2. Проекция на нормаль:
   $$
   v_{\text{before}} = V^{AB} \cdot n = 3 \cdot 0.6 + 4 \cdot 0.8 = 1.8 + 3.2 = 5
   $$

3. Коэффициент реституции:
   $$
   e = \min(0.8, 0.5) = 0.5
   $$

4. Скорость после столкновения:
   $$
   v_{\text{after}} = -e \cdot v_{\text{before}} = -0.5 \cdot 5 = -2.5
   $$

---

## Результат

Проекция относительной скорости после столкновения равна:
$$
\boxed{-2.5}
$$

---

### **1. Что означает это уравнение?**
#### Уравнение 5:
$$
V^{AB} \cdot n = -e \cdot (V^B - V^A) \cdot n
$$

Это уравнение показывает, как относительная скорость объектов изменяется после столкновения. Давайте разберём его шаг за шагом:

- $V^{AB}$ — это относительная скорость между объектами $A$ и $B$.
- $n$ — это нормаль столкновения (вектор, который указывает направление удара).
- $e$ — это коэффициент реституции (мера упругости столкновения, от 0 до 1).

**Зачем здесь минус?**  
Минус ($-$) появляется из-за того, что после столкновения объекты начинают двигаться в противоположных направлениях. Например:
- Если мяч ударяется о стену, то перед ударом он движется к стене, а после удара — от стены.
- Минус показывает, что направление скорости меняется на противоположное.

**Пример:**  
Предположим:
- $V^A = [2, 3]$, $V^B = [5, 7]$,
- $n = [0.6, 0.8]$,
- $e = 0.5$.

1. Вычислим относительную скорость до столкновения:
   $$
   V^{AB} = V^B - V^A = [5 - 2, 7 - 3] = [3, 4]
   $$

2. Найдём проекцию этой скорости на нормаль $n$:
   $$
   V^{AB} \cdot n = 3 \cdot 0.6 + 4 \cdot 0.8 = 1.8 + 3.2 = 5
   $$

3. Применим закон Ньютона с коэффициентом $e$:
   $$
   V^{AB}_{\text{after}} = -e \cdot (V^{AB} \cdot n) = -0.5 \cdot 5 = -2.5
   $$

Таким образом, после столкновения проекция относительной скорости будет равна $-2.5$.

---

### **2. Как работает импульс?**
Импульс — это "толчок", который изменяет скорость объекта. Чтобы понять, как это работает, давайте разберём следующее уравнение.

#### Уравнение 6:
$$
V' = V + j \cdot n
$$

- $V$ — это начальная скорость объекта.
- $j$ — это скалярный множитель, который показывает силу импульса.
- $n$ — это единичный вектор, который указывает направление импульса.
- $V'$ — это новая скорость объекта после применения импульса.

**Как это работает?**  
1. Вектор $n$ показывает направление, в котором действует импульс.
2. Скаляр $j$ определяет, насколько сильно этот импульс влияет на объект.
3. Мы добавляем этот "толчок" ($j \cdot n$) к текущей скорости $V$, чтобы получить новую скорость $V'$.

**Пример:**  
Предположим:
- $V = [2, 3]$,
- $n = [0.6, 0.8]$,
- $j = 5$.

Тогда:
$$
V' = V + j \cdot n = [2, 3] + 5 \cdot [0.6, 0.8] = [2, 3] + [3, 4] = [5, 7]
$$

Новая скорость объекта будет $[5, 7]$.

---

### **3. Связь импульса с массой**
Импульс — это физическая величина, которая зависит от массы и скорости. Формально:
$$
\text{Импульс} = \text{масса} \cdot \text{скорость}
$$

Отсюда можно выразить скорость через импульс:
$$
\text{Скорость} = \frac{\text{Импульс}}{\text{масса}}
$$

Теперь мы можем модифицировать уравнение для скорости, чтобы учесть массу объекта.

#### Уравнение 7:
$$
V' = V + \frac{j \cdot n}{\text{масса}}
$$

- $\frac{j \cdot n}{\text{масса}}$ — это изменение скорости, вызванное импульсом.
- Чем больше масса объекта, тем меньше изменение скорости при том же импульсе.

**Пример:**  
Предположим:
- $V = [2, 3]$,
- $n = [0.6, 0.8]$,
- $j = 5$,
- масса объекта = $2$.

Тогда:
$$
V' = V + \frac{j \cdot n}{\text{масса}} = [2, 3] + \frac{5 \cdot [0.6, 0.8]}{2} = [2, 3] + [1.5, 2] = [3.5, 5]
$$

Новая скорость объекта будет $[3.5, 5]$.

---

### **4. Почему важно понимать эти уравнения?**
Эти уравнения помогают моделировать физику столкновений в играх или симуляциях. Они позволяют:
1. Вычислить, как объекты будут двигаться после удара.
2. Учесть массу и упругость объектов.
3. Реализовать реалистичные взаимодействия между объектами.

---

### **Итоговый алгоритм:**
1. Вычислите относительную скорость до столкновения:
   $$
   V^{AB} = V^B - V^A
   $$
2. Найдите проекцию на нормаль:
   $$
   v_{\text{before}} = V^{AB} \cdot n
   $$
3. Примените закон Ньютона:
   $$
   v_{\text{after}} = -e \cdot v_{\text{before}}
   $$
4. Используйте импульс, чтобы изменить скорости:
   $$
   V' = V + \frac{j \cdot n}{\text{масса}}
   $$

---

### **Пример полного расчета:**
Пусть:
- $V^A = [2, 3]$, $V^B = [5, 7]$,
- $n = [0.6, 0.8]$,
- $e = 0.5$,
- масса объекта $A = 2$, масса объекта $B = 3$,
- $j = 5$.

1. Относительная скорость:
   $$
   V^{AB} = V^B - V^A = [5 - 2, 7 - 3] = [3, 4]
   $$

2. Проекция на нормаль:
   $$
   v_{\text{before}} = V^{AB} \cdot n = 3 \cdot 0.6 + 4 \cdot 0.8 = 1.8 + 3.2 = 5
   $$

3. Скорость после столкновения:
   $$
   v_{\text{after}} = -e \cdot v_{\text{before}} = -0.5 \cdot 5 = -2.5
   $$

4. Новая скорость объекта $A$:
   $$
   V'_A = V^A + \frac{j \cdot n}{\text{масса}_A} = [2, 3] + \frac{5 \cdot [0.6, 0.8]}{2} = [2, 3] + [1.5, 2] = [3.5, 5]
   $$

5. Новая скорость объекта $B$:
   $$
   V'_B = V^B - \frac{j \cdot n}{\text{масса}_B} = [5, 7] - \frac{5 \cdot [0.6, 0.8]}{3} = [5, 7] - [1, 1.33] = [4, 5.67]
   $$

---

### **Результат:**
Новые скорости объектов после столкновения:
- $V'_A = [3.5, 5]$,
- $V'_B = [4, 5.67]$.

$$
\boxed{\text{Готово!}}
$$

---

### **1. Что такое импульс?**
Импульс — это физическая величина, которая показывает, как движется объект под действием силы. Она связана с массой и скоростью объекта.

#### Уравнение 7:
$$
\text{Импульс} = \text{масса} \cdot \text{скорость}
$$

Отсюда можно выразить скорость через импульс:
$$
\text{Скорость} = \frac{\text{Импульс}}{\text{масса}}
$$

Теперь мы можем использовать это для изменения скорости объекта под действием импульса $j$ вдоль направления $n$:

$$
V' = V + \frac{j \cdot n}{\text{масса}}
$$

Здесь:
- $V$ — начальная скорость объекта.
- $j$ — величина импульса (скаляр).
- $n$ — единичный вектор, который указывает направление импульса.
- $\frac{j \cdot n}{\text{масса}}$ — изменение скорости из-за импульса.

**Пример:**  
Если объект имеет массу $2$, а импульс равен $5$ в направлении $n = [0.6, 0.8]$, то:
$$
V' = V + \frac{5 \cdot [0.6, 0.8]}{2} = V + [1.5, 2]
$$

---

### **2. Как объекты взаимодействуют при столкновении?**
Когда два объекта сталкиваются, они "толкают" друг друга в противоположных направлениях. Это описывается следующими уравнениями:

#### Уравнение 8:
$$
V'^A = V^A + \frac{j \cdot n}{\text{mass}^A}
$$
$$
V'^B = V^B - \frac{j \cdot n}{\text{mass}^B}
$$

Где:
- $V'^A$ и $V'^B$ — новые скорости объектов $A$ и $B$ после столкновения.
- $V^A$ и $V^B$ — их начальные скорости.
- $j$ — величина импульса.
- $n$ — нормаль столкновения (вектор, указывающий направление удара).
- $\text{mass}^A$ и $\text{mass}^B$ — массы объектов $A$ и $B$.

**Почему разные знаки?**  
- Объект $A$ "толкается" в направлении $n$ (поэтому $+$ перед $\frac{j \cdot n}{\text{mass}^A}$).
- Объект $B$ "толкается" в противоположном направлении ($-$ перед $\frac{j \cdot n}{\text{mass}^B}$).

**Пример:**  
Предположим:
- $V^A = [2, 3]$, $V^B = [5, 7]$,
- $n = [0.6, 0.8]$,
- $j = 5$,
- $\text{mass}^A = 2$, $\text{mass}^B = 3$.

Тогда:
$$
V'^A = [2, 3] + \frac{5 \cdot [0.6, 0.8]}{2} = [2, 3] + [1.5, 2] = [3.5, 5]
$$
$$
V'^B = [5, 7] - \frac{5 \cdot [0.6, 0.8]}{3} = [5, 7] - [1, 1.33] = [4, 5.67]
$$

Новые скорости:
- $V'^A = [3.5, 5]$,
- $V'^B = [4, 5.67]$.

---

### **3. Как связать все уравнения?**
Теперь нам нужно объединить уравнения для импульса и относительной скорости, чтобы найти $j$. Для этого используем закон Ньютона о реституции.

#### Уравнение 9:
$$
(V^A - V^B + \frac{j \cdot n}{\text{mass}^A} + \frac{j \cdot n}{\text{mass}^B}) \cdot n = -e \cdot (V^B - V^A) \cdot n
$$

Это уравнение показывает, что:
1. Относительная скорость после столкновения ($V'^A - V'^B$) должна соответствовать закону Ньютона о реституции.
2. Мы добавляем изменение скоростей из-за импульса ($\frac{j \cdot n}{\text{mass}^A}$ и $\frac{j \cdot n}{\text{mass}^B}$).

Перепишем уравнение для удобства:
$$
(V^A - V^B) \cdot n + j \cdot (\frac{n}{\text{mass}^A} + \frac{n}{\text{mass}^B}) \cdot n + e \cdot (V^B - V^A) \cdot n = 0
$$

---

### **4. Как найти $j$?**
Цель — выразить $j$ (величину импульса). Для этого перегруппируем уравнение:

#### Уравнение 10:
$$
(1 + e)((V^B - V^A) \cdot n) + j \cdot (\frac{1}{\text{mass}^A} + \frac{1}{\text{mass}^B}) = 0
$$

Решаем относительно $j$:
$$
j = \frac{-(1 + e)((V^B - V^A) \cdot n)}{\frac{1}{\text{mass}^A} + \frac{1}{\text{mass}^B}}
$$

**Объяснение:**  
1. $(V^B - V^A) \cdot n$ — проекция относительной скорости на нормаль $n$.
2. $1 + e$ — коэффициент, учитывающий упругость столкновения.
3. $\frac{1}{\text{mass}^A} + \frac{1}{\text{mass}^B}$ — сумма обратных масс объектов.

**Пример:**  
Предположим:
- $V^A = [2, 3]$, $V^B = [5, 7]$,
- $n = [0.6, 0.8]$,
- $e = 0.5$,
- $\text{mass}^A = 2$, $\text{mass}^B = 3$.

1. Вычислим относительную скорость до столкновения:
   $$
   V^{AB} = V^B - V^A = [5 - 2, 7 - 3] = [3, 4]
   $$

2. Проекция на нормаль:
   $$
   V^{AB} \cdot n = 3 \cdot 0.6 + 4 \cdot 0.8 = 1.8 + 3.2 = 5
   $$

3. Вычислим $j$:
   $$
   j = \frac{-(1 + 0.5)(5)}{\frac{1}{2} + \frac{1}{3}} = \frac{-7.5}{0.5 + 0.333} = \frac{-7.5}{0.833} \approx -9
   $$

---

### **5. Итоговый результат:**
Мы нашли величину импульса $j$, которую можно использовать для вычисления новых скоростей объектов $A$ и $B$.

$$
\boxed{j \approx -9}
$$

---

# Зачем мы ищем величину импульса $j$?

Когда мы моделируем физику столкновений, ключевым элементом является **величина импульса $j$**. В этом разделе мы объясним, зачем нужно вычислять $j$, как она используется и почему её нельзя просто задать вручную.

---

## 1. Что такое $j$?

$j$ — это **величина импульса**, которая определяет, насколько сильно объекты "толкают" друг друга при столкновении. Это не просто "сила", а результирующий эффект от взаимодействия, который учитывает:

- Массы объектов ($\text{mass}^A$ и $\text{mass}^B$),
- Их начальные скорости ($V^A$ и $V^B$),
- Направление удара (нормаль столкновения $n$),
- Упругость столкновения (коэффициент реституции $e$).

Импульс — это физическая величина, которая связана с изменением скорости объектов. В отличие от силы, которая действует мгновенно, импульс измеряет общий эффект от взаимодействия.

---

## 2. Почему мы ищем $j$?

Мы вычисляем $j$, потому что это ключевая величина, которая позволяет нам:

### 1. Вычислить новые скорости объектов после столкновения
Без $j$ мы не сможем узнать, как именно изменятся скорости объектов $A$ и $B$. Новые скорости зависят от:
- $j$,
- Масс объектов,
- Направления нормали $n$.

### 2. Учесть физические свойства объектов
$j$ автоматически учитывает:
- Массы объектов ($\text{mass}^A$ и $\text{mass}^B$),
- Коэффициент реституции ($e$), который показывает, насколько упругим будет столкновение.

### 3. Создать реалистичное поведение объектов
Вместо того чтобы задавать $j$ вручную, мы вычисляем его на основе начальных условий (скоростей, масс, направления удара). Это делает симуляцию более точной и реалистичной.

---

## 3. Как $j$ используется для вычисления новых скоростей?

После того как мы нашли $j$, мы подставляем её в уравнения для новых скоростей:

### Уравнение 8:
$$
V'^A = V^A + \frac{j \cdot n}{\text{mass}^A}
$$
$$
V'^B = V^B - \frac{j \cdot n}{\text{mass}^B}
$$

Здесь:
- $j \cdot n$ — это вектор импульса, который показывает, как объекты "толкаются" друг от друга.
- $\frac{j \cdot n}{\text{mass}^A}$ и $\frac{j \cdot n}{\text{mass}^B}$ — это изменения скоростей объектов $A$ и $B$, вызванные импульсом.

#### Пример:
Предположим:
- $V^A = [2, 3]$, $V^B = [5, 7]$,
- $n = [0.6, 0.8]$,
- $j = -9$,
- $\text{mass}^A = 2$, $\text{mass}^B = 3$.

Тогда:
$$
V'^A = [2, 3] + \frac{-9 \cdot [0.6, 0.8]}{2} = [2, 3] - [2.7, 3.6] = [-0.7, -0.6]
$$
$$
V'^B = [5, 7] - \frac{-9 \cdot [0.6, 0.8]}{3} = [5, 7] + [1.8, 2.4] = [6.8, 9.4]
$$

Новые скорости:
- $V'^A = [-0.7, -0.6]$,
- $V'^B = [6.8, 9.4]$.

---

## 4. Почему бы не задать $j$ вручную?

Если бы мы задавали $j$ вручную, то:

1. **Потеряли бы физическую точность:**
   - Мы бы не учитывали массы объектов, их начальные скорости и упругость столкновения.
   - Столкновения могли бы выглядеть нереалистично (например, слишком сильные или слабые).

2. **Пришлось бы каждый раз подбирать $j$:**
   - Для каждого столкновения нужно было бы экспериментировать с разными значениями $j$, чтобы добиться правильного результата.
   - Это заняло бы много времени и усилий.

3. **Не смогли бы автоматизировать симуляцию:**
   - Если у нас много объектов, которые сталкиваются друг с другом, вручную задавать $j$ для каждого столкновения было бы невозможно.

---

## 5. Зачем мы указываем $j$ в уравнениях?

Мы указываем $j$ в уравнениях, потому что это **неизвестная величина**, которую нужно найти. Она связывает все параметры столкновения (скорости, массы, упругость) в одно уравнение. После того как мы вычислим $j$, мы можем использовать её для расчета новых скоростей.

---

## 6. Итог: зачем искать $j$?

1. $j$ — это ключевая величина, которая определяет, как объекты взаимодействуют при столкновении.
2. Она позволяет автоматически рассчитать новые скорости объектов, учитывая их массы, скорости и упругость.
3. Без $j$ мы не смогли бы создать реалистичную физическую симуляцию.

$$

---

### **1. Что мы сделали?**
Мы только что завершили сложные математические вычисления, чтобы найти формулу для расчета импульса при столкновении двух объектов. Эта формула позволяет нам узнать, как объекты будут двигаться после удара друг о друга.

Финальная формула (уравнение 10) выглядит так:
$$
j = \frac{-(1 + e) \cdot \text{velAlongNormal}}{\frac{1}{\text{mass}^A} + \frac{1}{\text{mass}^B}}
$$

Здесь:
- $j$ — это величина импульса, которую мы ищем.
- $\text{velAlongNormal}$ — это проекция относительной скорости на нормаль столкновения.
- $e$ — коэффициент упругости (насколько сильно объекты отскакивают).
- $\text{mass}^A$ и $\text{mass}^B$ — массы объектов.

Эта формула говорит нам, как сильно объекты "толкают" друг друга при столкновении.

---

### **2. Как это работает в коде?**

Теперь мы можем перевести эту математику в программный код. Вот пример функции, которая решает столкновение между двумя объектами:

```cpp
void ResolveCollision(Object A, Object B)
{
    // 1. Вычисляем относительную скорость
    Vec2 rv = B.velocity - A.velocity;

    // 2. Находим проекцию относительной скорости на нормаль столкновения
    float velAlongNormal = DotProduct(rv, normal);

    // 3. Проверяем, нужно ли разрешать столкновение
    if (velAlongNormal > 0)
        return; // Если объекты уже расходятся, ничего не делаем

    // 4. Вычисляем коэффициент упругости
    float e = min(A.restitution, B.restitution);

    // 5. Вычисляем величину импульса (j)
    float j = -(1 + e) * velAlongNormal;
    j /= (1 / A.mass + 1 / B.mass);

    // 6. Применяем импульс к скоростям объектов
    Vec2 impulse = j * normal;
    A.velocity -= (1 / A.mass) * impulse;
    B.velocity += (1 / B.mass) * impulse;
}
```

---

### **3. Что происходит в этом коде?**

#### Шаг 1: Относительная скорость
Мы вычисляем, насколько быстро объект $B$ движется относительно объекта $A$. Это называется **относительной скоростью**:
$$
\text{rv} = V^B - V^A
$$

#### Шаг 2: Проекция на нормаль
Мы находим, какая часть этой относительной скорости направлена вдоль нормали столкновения ($n$). Это важно, потому что столкновение происходит именно вдоль этой линии.

#### Шаг 3: Проверка на разделение
Если объекты уже расходятся (то есть их относительная скорость вдоль нормали положительна), то мы **ничего не делаем**. Это предотвращает ненужные вычисления и делает симуляцию более реалистичной.

#### Шаг 4: Коэффициент упругости
Мы выбираем минимальное значение коэффициента упругости ($e$) из двух объектов. Это гарантирует, что столкновение будет интуитивно понятным (например, мяч отскакивает от стены сильнее, чем два тяжелых камня).

#### Шаг 5: Величина импульса ($j$)
Мы вычисляем величину импульса ($j$), которая показывает, насколько сильно объекты "толкают" друг друга. Это основная формула, которую мы вывели ранее.

#### Шаг 6: Применение импульса
Мы изменяем скорости объектов $A$ и $B$, используя величину импульса ($j$). Чем больше масса объекта, тем меньше его скорость изменится.

---

### **4. Почему важно проверять `if(velAlongNormal > 0)`?**

Эта проверка гарантирует, что мы разрешаем столкновение только тогда, когда объекты движутся **навстречу друг другу**. Если объекты уже расходятся (то есть их скорости направлены в противоположные стороны), то мы **не должны** применять импульс. Это важно, чтобы избежать нереалистичного поведения.

Пример:
- Два мяча сталкиваются, но после удара они начинают двигаться в разные стороны. Если мы попытаемся снова "толкнуть" их друг к другу, это будет выглядеть странно.

---

### **5. Оптимизация: Обратная масса**

В физических движках часто используют **обратную массу** ($1 / \text{mass}$), потому что она упрощает вычисления. Вместо того чтобы каждый раз вычислять $1 / \text{mass}$, мы можем сохранить её заранее:

```cpp
A.inv_mass = 1 / A.mass;
B.inv_mass = 1 / B.mass;
```

Теперь формула для $j$ становится проще:
$$
j = \frac{-(1 + e) \cdot \text{velAlongNormal}}{\text{A.inv\_mass} + \text{B.inv\_mass}}
$$

---

### **6. Распределение импульса между объектами**

Чтобы сделать симуляцию ещё более реалистичной, мы можем распределить импульс ($j$) между объектами пропорционально их массам. Например:
- Маленький объект (например, мяч) получит большую долю импульса.
- Большой объект (например, стена) получит маленькую долю импульса.

Для этого можно использовать следующий код:

```cpp
float mass_sum = A.mass + B.mass;
float ratio_A = A.mass / mass_sum;
float ratio_B = B.mass / mass_sum;

A.velocity -= ratio_A * impulse;
B.velocity += ratio_B * impulse;
```

Этот код делает то же самое, что и предыдущий, но более интуитивно распределяет силу удара.

---

### **7. Итог**

1. Мы вычисляем импульс ($j$), который показывает, как сильно объекты "толкают" друг друга при столкновении.
2. Мы применяем этот импульс к скоростям объектов, учитывая их массы.
3. Мы проверяем, нужно ли вообще разрешать столкновение (если объекты уже расходятся, ничего не делаем).
4. Мы оптимизируем вычисления, используя обратную массу.
5. Мы распределяем импульс между объектами пропорционально их массам.

---

### **Почему это важно?**

Этот код создаёт реалистичную физику столкновений. Он используется в играх, симуляциях и других программах, где важно моделировать взаимодействие объектов. Теперь вы знаете, как это работает!

$$
\boxed{\text{Готово!}}
$$
\boxed{\text{$j$ — это сердце физики столкновений, которое делает всё работающим!}}
$$
