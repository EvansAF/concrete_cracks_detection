"# concrete_cracks_detection" 
inside concrete_cracks_detection you should build the file structure.



Thus content should be placed inside concrete_cracks_detection ( root folder). Inside content place concrete_images inside concrete_images the three folders train, validation, test

You can put the archive folder inside content or manually extract its two folders, Negative and Positive, into concrete_images

Otherwise just place the archive folder you get in your google drive and use the file path option for it if working with colabs




Note that using the settings below :
 Define the split ratio-- 
train_ratio = 0.05
val_ratio = 0.02
test_ratio = 0.93


Test Performance --
history = model.fit(
    ds_train,
    validation_data=ds_valid,
    epochs=5,
)

is just meant to make the code work quickly in resouce constrained settings and would not produce a great model

with adequate resources try with : 

 Define the split ratio (e.g., 70% train, 15% validation, 15% test--- playing with 0.05. 0.02 and 0.93)
train_ratio = 0.7
val_ratio = 0.15
test_ratio = 0.15

and Test Performance
with epochs=50
history = model.fit(
    ds_train,
    validation_data=ds_valid,
    epochs=50,
)