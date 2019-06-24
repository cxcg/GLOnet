# Global optimization based on generative nerual networks (GLOnet)

## Requirements

We recommend using python3 and a virtual environment

```
virtualenv -p python3 .env
source .env/bin/activate
pip install -r requirements.txt
```

When you're done working on the project, deactivate the virtual environment with `deactivate`.

A matlab engine for python is needed for EM simulation. Please refer to [MathWorks Pages](https://www.mathworks.com/help/matlab/matlab_external/install-matlab-engine-api-for-python-in-nondefault-locations.html) for installation.

Path of RETICOLO should be added in the `main_single.py`

## Training the GLOnet

You can change the parameters by editing `Params.json` in `results` folder. 

If you want to train the network, simply run
```
python main_single.py 
```

or 

```
python main_single.py --output_dir results --w 900 --a 60
```

to specify non-default output folder or training set


## Results

All results will store in output_dir/w<wavelength>a<angle> folder.
	-figures/  (figures of generated devices and loss function curve and others for every 200 iterations)
	-model/    (all weights of the generator and discriminator)
	-outputs/  (500 generated devices for every combination of wavelength and angle in `.mat` format)
	-history.mat
	-train.log