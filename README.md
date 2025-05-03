# Image Segmentation Using K-Means Clustering
This project demonstrates image segmentation using the K-means clustering algorithm to isolate distinct color clusters from input images. The segmentation process is visualized by displaying each cluster separately and cleaning digit clusters for better viewing.

# Features:
- Upload multiple images for segmentation.
- Segment each image into k color clusters.
- Visualize each cluster's segmentation as an individual image.
- Clean up isolated noise for digit cluster visualization.
- K-means++ initialization to improve the clustering process.

# Requirements:
Python 3.x

# Libraries:
- opencv-python
- numpy
- matplotlib
- google-colab (for displaying images in a Colab environment)

# Code Explanation:
# Functions:
- load_image(image_path): Loads an image from the provided path, converts it from BGR to RGB, and returns the image.
- aff_cluster(cluster_index, segmented_image, labels)
- Isolates a specific cluster from the segmented image using the provided cluster index and labels. It returns the isolated cluster image along with the average color of that cluster in hex format.
- show_clean_digit_cluster(segmented_image, labels, cluster_index): Displays a cleaned version of a digit cluster after thresholding and morphological cleanup.
- initialize_centroids_plus_plus(data, k): Initializes centroids for the K-means algorithm using the K-means++ strategy to improve clustering performance.
- assign_clusters(data, centroids): Assigns each pixel in the image to the nearest centroid based on Euclidean distance.
- update_centroids(data, labels, k): Updates the centroids of the clusters based on the mean of the pixels assigned to each cluster.
- kmeans(data, k, max_iters=100, tol=1e-4): The main K-means algorithm implementation that performs the clustering until convergence or the maximum number of iterations is reached.
- segment_and_show_clusters_only(image_paths, k): Segments the images into k clusters and visualizes the segmented images. Each cluster is displayed in a separate subplot.

# Usage:
- Upload images that you want to segment into color clusters.
- Set the number of clusters k that you want the image to be segmented into.
- Call the segment_and_show_clusters_only() function with the paths to the images and the number of clusters.
- The function will display each segmented cluster for the images.

# Examples 
1... ![Image](https://github.com/user-attachments/assets/a5a9ae6e-4dc0-499a-bac9-166bda70686a)
![Image](https://github.com/user-attachments/assets/c941cd16-bb1c-4d89-b02d-93a848993283)

2... ![Image](https://github.com/user-attachments/assets/0ce5f843-f721-410f-a77b-54d22150c174)
![Image](https://github.com/user-attachments/assets/f28ef3f0-88d9-479c-a9b4-48f8acd7bfd9)

3... ![Image](https://github.com/user-attachments/assets/f76d106a-75d8-4a0a-a0b5-634c2756d8d4)
![Image](https://github.com/user-attachments/assets/35f8211f-dfe4-4de4-9445-3d4412278a5c)

4... ![Image](https://github.com/user-attachments/assets/648c45b9-76fd-4269-b08e-37dd8a2c1c92)
![Image](https://github.com/user-attachments/assets/3fb0868b-b667-408c-86d8-ac1b20c98a14)


** ![Image](https://github.com/user-attachments/assets/0aa425b7-f18f-4ad2-abc5-cb18cf02a4bf)
** ![Image](https://github.com/user-attachments/assets/5f8b3728-b561-4255-87d7-cf6bcd06009c)
