## For Development

### Travela have `travela-frontend` and `travela-backend` images for both frontend and backend
The `travela-backend` image creates:
 - app container. This runs the backend functionality of the application
 - database container. This run  Postgres database

#### Image link
- https://drive.google.com/file/d/1hk60pj22ZAd9FNKLd3yOwGMguobhS-le/view?usp=sharing
- https://drive.google.com/file/d/1ncejisAq4GrphsmozoY6FAlQxRYMBOdX/view?usp=sharing


The `travela-frontend` image creates:
- web container. This runs the frontend functionality of the application
- storybook container. This runs the storybook

#### Image Link
- https://drive.google.com/file/d/14YisZgO35NZoftSBpzyrJS5WAZMidkt2/view?usp=sharing


## For Staging

For staging Travela uses GCP (google cloud platform) environment, both travela-frontend and travela-backend images are deployed to  travela-staging cluster. Deployment  on staging only happens when a new feature, bug or chore has been merged to develop branch, this is made possible through the circle ci pipeline

#### Images
##### Circle CI workflow that deploys to staging.
1.[Frontend](https://drive.google.com/file/d/1vuseG_yInP8Y-EUwbgGsp5X_T_4q_aJz/view?usp=sharing)

2.[Backend](https://drive.google.com/file/d/1kcpYZoe-2_WQE6qrFm6pqwbux3Bt5zNG/view?usp=sharing)



## For production

For production, the application is deployed on travela-production cluster, both the frontend and backend container runs on this cluster.

#### Images
##### Circle CI workflow that deploys to production
1.[Frontend](https://drive.google.com/file/d/1PmaNn1E2_6ch8kB0AsOhuI6noPaI69x-/view?usp=sharing)

2.[Backend](https://drive.google.com/file/d/12Xq2fH_B3Q6T0aHnVADYodZy4CNSp97h/view?usp=sharing)



##### Images to circle CI configuration that helps with the deployment

1. Backend configuration:
- https://drive.google.com/file/d/1WKz5tIoGehUuQB5-U6AdnLUhWNnnP4ud/view?usp=sharing
- https://drive.google.com/file/d/1GYmLuy5gOy2EY9gnYI_ACql14fOQjpGT/view?usp=sharing



2. Frontend configuration
- https://drive.google.com/file/d/1Ovegz8tzNno8W3iAH1HU2kNp78Ty_39t/view?usp=sharing
- https://drive.google.com/file/d/1-KDhDEVx0fOBuYgSSMnd-cOCX4n7y9gF/view?usp=sharing

