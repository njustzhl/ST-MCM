Environment

conda create -n ST-MCM python=3.8
conda activate ST-MCM
pip install torch==1.10.2+cu113 torchvision==0.11.3+cu113 torchaudio==0.11.0 --extra-index-url https://download.pytorch.org/whl/cu113
pip install -r requirements.txt

Train

cd tools
python run.py --cfg ../configs/posetimation/ST-MCM/posetrack17/configs.yaml --train 

Val

cd tools
python run.py --cfg ../configs/posetimation/ST-MCM/posetrack17/configs.yaml --val 
