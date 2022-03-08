# hse_hw2_chip

[Google Colab](https://colab.research.google.com/drive/1qnH61N7iZLgjByzsEnZLekWRmTcurRh_?usp=sharing)

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

# Statistic table of aligning on X chromosome

|Index|Reads|Unique alignment|Not unique alignment|Not aligned|
|---|---|---|---|---|
| ENCFF000BGA | 12426059 | 316786 (2.55%) | 1444075 (11.62%) | 10665198 (85.83%) |
| ENCFF000BGD | 15122630 | 423471 (2.80%) | 1677260 (11.09%) | 13021899 (86.11%) |
| ENCFF066LYG | 17162591 | 565071 (3.29%) | 1705577 (9.94%) | 14891943 (86.77%) |


# Venn Diagrams
## BGA intersection with known peaks from Encode
![image](Venn Diagrams/BGA1.pdf)

## Known peaks from Encode intersection with BGA
![image](Venn Diagrams/BGA2.pdf)

## BGD intersection with known peaks from Encode
![image](Venn Diagrams/BGD1.pdf)

## Known peaks from Encode intersection with BGD
![image](Venn Diagrams/BGD2.pdf)

Такое малое количество пересечений связано с тем, что выравнивание производилось только на одну-единственную хромосому -- chrX, а Encode предоставляет информацию с пиками для всех хромосом. 
