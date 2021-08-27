# GAN_art
Генеративно-состязательная сеть, которая позволяет генерировать картины абстрактного стиля.

Для использования в целях самостоятельного обучения модели необходимо загрузить датасет (https://www.kaggle.com/ikarus777/best-artworks-of-all-time) в папку "data" текущего каталога. 

Для корректного использования функции сохранения сгенерированного изображения необходимо наличие папки "Generated_imgs" в текущем каталоге. Для каждого сгенерированного изображения необходимо задавать id_num в качестве параметра сохранения. 

Далее я представлю результаты работы GAN 
Базовая модель: 
Параметры: lr = 1e-3, betas = (0.5, 0.999)
Результаты работы:
После первых 10 эпох:

![Иллюстрация к проекту](https://github.com/AverichkinaVictoria/GAN_art/blob/main/results_1.png)




После первых 50 эпох (изображения цветные, но все еще присутствуют пятна):

![Иллюстрация к проекту](https://github.com/AverichkinaVictoria/GAN_art/blob/main/results_2.png)




После первых 150 эпох (в выборке уже появляются картины, сгенерированные подражанием карандашу, а также светлые пятна – подражания портретам в выборке):

![Иллюстрация к проекту](https://github.com/AverichkinaVictoria/GAN_art/blob/main/results_3.png)

![Иллюстрация к проекту](https://github.com/AverichkinaVictoria/GAN_art/blob/main/results_4.png)




После  220 эпох:

![Иллюстрация к проекту](https://github.com/AverichkinaVictoria/GAN_art/blob/main/results_5.png)

![Иллюстрация к проекту](https://github.com/AverichkinaVictoria/GAN_art/blob/main/results_5.png)




Несмотря на достаточно хорошее качество сгенерированных изображений, график функции потерь на каждой итерации показывает, что к концу обучения ошибка генератора стремительно возрастает. 

 ![Иллюстрация к проекту](https://github.com/AverichkinaVictoria/GAN_art/blob/main/loss.jpeg)

Дискриминатор слишком быстро учится распознавать реальные и сгенерированные изображения. 



