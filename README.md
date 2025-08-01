# YMHA-IDN

## Project description
Project to segment 2D brain sections. You can create **bold** and *italic* fonts.


## Manual Annotations

Here is how you can embed an image in a markdown document:

![A brain section!](https://github.com/tfunck/YMHA-IDN/blob/main/images/example.png)


### Examples, challenges, anatomic structures, etc.

## Automatic Segmentation

### Otsu Thresholding

### K-Means

### Description of the code in your notebook

Here is an example of including a [hyperlink](https://github.com/tfunck/YMHA-IDN/blob/main/Automatic_Brain_Section_Segmentation.ipynb) to the jupyter-notebook.

You can embed code like this.
Here we load a .csv file with information about the brain sections.
```
df = pd.read_csv('/mount/MyDrive/share/YMHA IDN/final_v.2/annotations.csv')
```


Here we have a for-loop that does some stuff.
```
for index, row in df.iterrows() :
  image_path = row['image']
  label_path = row['label']

  print('Row number:', index)
  print('\timage path:', image_path)
  print('\tlabel path:', label_path)
  print(np.unique(label_array))

  image_array = iio.imread(image_path)
  label_array = iio.imread(label_path)

  plt.subplot(1,2,1)
  plt.imshow(image_array)
  plt.subplot(1,2,2)
  plt.title(np.sum(label_array))
  plt.imshow(label_array)
  plt.show()
```


### Automatic vs Manual Segmentation

