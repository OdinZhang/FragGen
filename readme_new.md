## newly append
# generation
config newly append num_classes arg, you should change it according to your fragment_base

# process data
if you want to process you own data, you should first index your data in this format[pdb_path, sdf_path, 0, 0], download ply creater script (in ipynb), move it to delete project(./utils/masif/), create your ply files and update index file. 

Second, pickle all your ligand in mol object to .pkl file. 

Third, change the path in vocab_creator.py and vocab_modify.py, run `python vocab_creator.py`, `python vocab_modify.py` to get fragbase. 

Fourth, change args according to your path, run `python train_data_process.py`

Fifth, split your data use `python split.py`, also you should change the path args

# train
you should modify num_classes arg according to your fragbase, then start training

# correct data and python scripts
all in [zenodo](https://zenodo.org/records/15075242)