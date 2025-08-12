# FewShot_yolov11ResultsGraphs

Comandos especificos para entrenar modelos FewShot

Parte 1. Conocimientos base con clases base, sin las clases a ser novedad.
---------------------------------------------------------------------------------------------------------------------
1. Entrenamiento con estandar sin la clase id = 0 person 
!Ejemplo para generar los pesos yolo11xIdt-seg.pt  sin personas
nohup yolo task=segment mode=train model=./yaml_model/yolo11xIdt-seg.yaml data=./yaml_data/coco.yaml epochs=100 batch=8 imgsz=448 classes=[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79] workers=8 project=COCO_Standar name=TrainxIdtNOPerson pretrained=False save_period=10 warmup_epochs=3 device=0 > ./SalidasStandar/TrainxIdtNOPerson.out 2>&1 &


2. Entrenamiento con estandar sin la superclase "vehicle": [1, 2, 3, 4, 5, 6, 7, 8],
!Ejemplo para generar los pesos yolo11mIdt-seg.pt  sin vehiculos
nohup yolo task=segment mode=train model=./yaml_model_coco/yolo11mIdt-seg.yaml data=./yaml_data/coco.yaml epochs=100 batch=8 imgsz=448 classes=[0,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79] workers=8 project=COCO_Standar name=mediIdtTrainNOVehicle pretrained=False save_period=10 warmup_epochs=3 device=2 > ./SalidasStandar/mediIdtTrainNoVehicle.out 2>&1 &

3. Entrenamiento con estandar sin la superclase "animal": [14, 15, 16, 17, 18, 19, 20, 21, 22, 23],
!Ejemplo para generar los pesos yolo11mIdt-seg.pt  sin animales
nohup yolo task=segment mode=train model=./yaml_model_coco/yolo11mIdt-seg.yaml data=./yaml_data/coco.yaml epochs=100 batch=8 imgsz=448 classes=[0,1,2,3,4,5,6,7,8,9,10,11,12,13,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79] workers=8 project=COCO_Standar name=mediTrain pretrained=False save_period=10 warmup_epochs=3 device=0 > ./mIdtTrainNOAnimals.out 2>&1 &

