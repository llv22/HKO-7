# Run Python Wrapper of VarFlow

## 1. Setup
```bash
cd <git repository>/VarFlow/
mkdir build
cd build
cmake ..
make
```
## 2. Library refinement
in Line 8 of VarFlow/varflow.py:  
```python
_VALID_DLL_PATH = [os.path.join(_BASE_PATH, '..', 'build', 'Release', 'varflow.dll'),
                   os.path.join(_BASE_PATH, '..', 'build', 'libvarflow.so'),
                   os.path.join(_BASE_PATH, '..', 'build', 'libvarflow.dylib')]
```

## 3. In <git repository>/VarFlow/
```bash
python setup.py develop
```

## 4. Run testing
```bash
cd <git repository>/VarFlow/varflow
python varflow.py
```