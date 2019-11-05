`https://tensorboard.dev/`  is the new service from Google that enables us to conveniently host, track, and share your ML experiments for free.

Below are some simple instructions on how to use it with Jupyter notebooks.


## Install and run `tensorboard dev`
These command should be run at a shell 


* Install the latest tensorboard to have `dev` option

```
pip install -U tensorboard
```

* Run 
```
tensorboard dev --auth_force_console upload  --logdir ./logs

```

You will be prompted to login to a Google account to grab an authorisation token. A successful run will look like this

```
Upload started and will continue reading any new data as it's added
to the logdir. To stop uploading, press Ctrl-C.
View your TensorBoard live at: https://tensorboard.dev/experiment/<unique-identifier>
```

Open the link in the browser to view experiments results.

## Example with `mnist` dataset

See [mnist.ipynb](mnist.ipynb) for a Jupyter notebook that uses Tensorflow `tf.keras` for training with the `mnist` dataset of handwritten digits. Training statistics are written into `logs` dir and will be uploaded live to `tensorboard.dev`.

Here is a screenshot of the page

![](images/tensorboard-dev-mnist.png?raw=true)

