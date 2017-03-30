
## Google Code University: Python

mkvirtualenv gcu --python=`which python3`
cd repo
mkdir gcu-python
git init
git add . && git commit -am "it begins!"
hub create -d "Google Code University: Python"


wget https://developers.google.com/edu/python/google-python-exercises.zip
unzip google-python-exercises.zip
mkdir gcu-py3
2to3 --output-dir=gcu-py3 -W -n google-python-exercises 
git add :/ --all && git commit -am "dloaded Google Python class; 2to3 conversion"
git push --set-upstream origin master

cd gcu-py3
python hello.py
chmod o+x hello.py
./hello.py

pip install ipython
