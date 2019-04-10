# The BILINEAR CAPSULE model takes the idea from the paper: http://vis-www.cs.umass.edu/bcnn/docs/bcnn_iccv15.pdf <h1> tag

The structure of the model is:

-----------------------                                         -------            -------             -------
|                     |                                         |     |            |     |             |     |
|                     |      A                                  |  b  |            |  l  |             |     |
| RESNET+CAPSNET1     |-------------.                           |  i  |            |  i  |             |  s  |
|                     |             |                           |  l  |            |  n  |             |  o  |
|                     |             |   MATRIX PRODUCT          |  i  |            |  e  |             |  f  |
|                     |             |  ............             |  n  |            |  a  |             |  t  |
-----------------------             |  .          .             |  e  |            |  r  |             |  m  |
                                    |->.   A*B    . --------->  |  a  | ---------> |     | ----------->|  a  |
-----------------------             |  .          .             |  r  |            |  l  |             |  x  |
|                     |             |  ............             |     |            |  a  |             |     |
|                     |      B      |                           |     |            |  y  |             |     |
| RESNET+CAPSNET2     |-------------.                           |     |            |  e  |             |     |
|                     |                                         |     |            |  r  |             |     |
|                     |                                         |     |            |     |             |     |
|                     |                                         |     |            |     |             |     |
-----------------------                                         -------            -------             -------

MATRIX PRODUCT:
    1 EUCLIDEAN PRODUCT INNER MATRIX https://en.wikipedia.org/wiki/Inner_product_space
    2 PRODUCT OUTER  MATRIX https://en.wikipedia.org/wiki/Outer_product

