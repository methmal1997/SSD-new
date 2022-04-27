In pasacalvoc_2007 file 
edit train and trst sizes according to dataset
edit Train stastics and test stattics(if in phone one image has 2 object  then (5,6) )



In pasacalov_common file 
edit training path
edit path (search using'general')
edit no of classes (search 'Dataset flags')
edit batch size computer performanse (search using'batch') like 6


run model

python train_ssd_network.py --dataset_name=pascalvoc_2007 --dataset_split_name=train --model_name=ssd_300_vgg --save_summaries_secs=60 --save_interval_secs=600 --weight_decay=0.0005 --optimizer=adam --learning_rate=0.001 --batch_size=6 --gpu_memory_fraction=0.9 --checkpoint_exclude_scopes =ssd_300_vgg/conv6,ssd_300_vgg/conv7,ssd_300_vgg/block8,ssd_300_vgg/block9,ssd_300_vgg/block10,ssd_300_vgg/block11,ssd_300_vgg/block4_box,ssd_300_vgg/block7_box,ssd_300_vgg/block8_box,ssd_300_vgg/block9_box,ssd_300_vgg/block10_box,ssd_300_vgg/block11_box

code run in command line