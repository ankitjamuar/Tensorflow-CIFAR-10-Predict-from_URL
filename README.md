Teained Tensorflow on CIFAR-10 and code for predicting image from URL by resizing automaticaaly


<code>
# Predict from url 
import cv2
import urllib.request
from PIL import Image
image = Image. open(urllib.request.urlopen("https://i.insider.com/5cbf50dfd1a2f8074406a8b2?width=1100&format=jpeg&auto=webp"))
numpy_image = np.array(image)
numpy_image = numpy_image/255
resized_image = cv2.resize(numpy_image, dsize=(32, 32), interpolation=cv2.INTER_CUBIC)
prediction = model.predict([[  resized_image   ]])[0]
index =  np.argmax( prediction )
print( classes[index] )
print( prediction[index] )
plt.imshow(resized_image)
  </code>
