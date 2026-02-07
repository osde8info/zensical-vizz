---
title: "cloudinary - howto upload a directory of images"
date: 2026-02-05
categories: 
  - "vizz"
---

upload a directory of images to cloudinary using their cli

- [https://cloudinary.com/documentation/cloudinary\_cli#upload\_dir](https://cloudinary.com/documentation/cloudinary_cli#upload_dir)

```
pipx install cloudinary
pipx ensurepath
$Env:CLOUDINARY_URL="cloudinary://123456:abcdefg@your_cloud_name"
cld sync --push . mycloudfolder

```

upload a directory of images to cloudinary with node & multer

- [https://practicaldev.online/blog/node/cloudinary-image-upload-nodejs](https://practicaldev.online/blog/node/cloudinary-image-upload-nodejs)

- [https://www.geeksforgeeks.org/node-js/how-to-upload-single-multiple-image-to-cloudinary-using-node-js/](https://www.geeksforgeeks.org/node-js/how-to-upload-single-multiple-image-to-cloudinary-using-node-js/)

- [https://dev.to/abhishekjaiswal\_4896/uploading-images-using-cloudinary-in-nodejs-21b9](https://dev.to/abhishekjaiswal_4896/uploading-images-using-cloudinary-in-nodejs-21b9)
