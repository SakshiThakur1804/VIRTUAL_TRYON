The goal of our project is to allow people to see how clothes would look on them without physically trying them on. This is especially useful for online shopping, where customers often face uncertainty about how a garment will fit or look.

Our system works in three main steps:

Understanding the person’s body position – We use OpenPose to detect key points like shoulders, elbows, and hips. This tells us exactly how the person is standing and how the new clothes should be positioned.

Fitting the new garment – We take the cloth image and warp it using a method called Thin Plate Spline. This lets the cloth bend and stretch naturally so it matches the person’s pose and body shape.

Making it look realistic – We use a deep learning model that combines U-Net (for preserving structure) and GAN (for adding realistic textures). This blends the warped cloth into the original image, keeping the face, skin, and background unchanged while making the garment look naturally worn.

We trained on two datasets:

CP-VTON – low-resolution images, which helped us train quickly in the early stages.

VITON-HD – high-resolution images for sharp and detailed final results.

Our model produces outputs where the person’s pose, body shape, and face are preserved, but the clothing changes seamlessly. It can also handle different garments for the same person or the same garment on different people.
