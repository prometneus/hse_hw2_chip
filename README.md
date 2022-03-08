# hse_hw2_chip

Ссылка на Google Colab: https://colab.research.google.com/drive/1qnH61N7iZLgjByzsEnZLekWRmTcurRh_?usp=sharing

Клеточная линия -- HepG2
Гистоновая метка -- H3K4me2

# FastQC and MultiQC

![image](https://user-images.githubusercontent.com/86663451/157294935-c0cc2cde-19ec-40cc-b512-0780068171ed.png)

Качество исходных файлов оказалось довольно плохим, я посчитал, что необходимо подрезание, особенно учитывая количество гэпов везде, кроме файла контроля, выделенного на картинке ниже. Дублицирование было низким, адаптеров совсем не наблюдалось.

![image](https://user-images.githubusercontent.com/86663451/157295005-600767c7-0b8f-45df-bd4c-3d50d1033d05.png)

GC состав:

![image](https://user-images.githubusercontent.com/86663451/157296398-d4f6977d-fa9d-44f4-b695-d9a9e7b94e91.png)


Я решил не подрезать файл контроля, потому что он и так норм, а результаты подрезания остальных файлов представлены ниже. Вкратце: стало лучше, но не так чтобы сильно.

![image](https://user-images.githubusercontent.com/86663451/157295750-328b0827-e74a-4640-abcf-64277312693c.png)

А вот гэпов вообще практически не осталось, что не может не радовать:

![image](https://user-images.githubusercontent.com/86663451/157295883-02c91ad3-9308-4f09-a53e-050540048067.png)

Линия GC состава всё ещё сильно флуктуирует:

![image](https://user-images.githubusercontent.com/86663451/157296537-9c267481-8ecc-4833-8ed7-5c68565e41e3.png)

# Statistic table of aligning on X chromosome:



# Venn Diagrams
