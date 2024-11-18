# MiniTorch Module 3

<img src="https://minitorch.github.io/minitorch.svg" width="50%">

* Docs: https://minitorch.github.io/

* Overview: https://minitorch.github.io/module3.html


You will need to modify `tensor_functions.py` slightly in this assignment.

* Tests:

```
python run_tests.py
```

* Note:

Several of the tests for this assignment will only run if you are on a GPU machine and will not
run on github's test infrastructure. Please follow the instructions to setup up a colab machine
to run these tests.

This assignment requires the following files from the previous assignments. You can get these by running

```bash
python sync_previous_module.py previous-module-dir current-module-dir
```

The files that will be synced are:

        minitorch/tensor_data.py minitorch/tensor_functions.py minitorch/tensor_ops.py minitorch/operators.py minitorch/scalar.py minitorch/scalar_functions.py minitorch/module.py minitorch/autodiff.py minitorch/module.py project/run_manual.py project/run_scalar.py project/run_tensor.py minitorch/operators.py minitorch/module.py minitorch/autodiff.py minitorch/tensor.py minitorch/datasets.py minitorch/testing.py minitorch/optim.py


# Training Logs: CPU vs GPU

Below are my training logs for CPU vs GPU, with each row representing the same dataset.

---

### Simple Dataset
<div style="display: flex; align-items: center;">
  <div style="text-align: center; margin-right: 20px;">
    <img width="340" alt="simple_gpu_log" src="https://github.com/user-attachments/assets/8133d8be-0c0c-46bc-9ce3-180872541128">
    <p><strong>GPU</strong></p>
  </div>
  <div style="text-align: center;">
    <img width="341" alt="simple_cpu_log" src="https://github.com/user-attachments/assets/710033c5-c9f9-4a22-afae-928876decbe6">
    <p><strong>CPU</strong></p>
  </div>
</div>

---

### XOR Dataset
<div style="display: flex; align-items: center;">
  <div style="text-align: center; margin-right: 20px;">
    <img width="356" alt="xor_gpu_log" src="https://github.com/user-attachments/assets/96428a04-a5f9-45e6-8109-1176eb6b06e5">
    <p><strong>GPU</strong></p>
  </div>
  <div style="text-align: center;">
    <img width="304" alt="xor_cpu_log" src="https://github.com/user-attachments/assets/c36f0ec1-2500-4db9-be1a-738f4a8a6ef0">
    <p><strong>CPU</strong></p>
  </div>
</div>

---

### Split Dataset
<div style="display: flex; align-items: center;">
  <div style="text-align: center; margin-right: 20px;">
    <img width="340" alt="split_gpu_log" src="https://github.com/user-attachments/assets/c60c3c95-f840-4558-ab0a-d6b5ef0d0e69">
    <p><strong>GPU</strong></p>
  </div>
  <div style="text-align: center;">
    <img width="340" alt="split_cpu_log" src="https://github.com/user-attachments/assets/f99b57f6-13cc-470f-8369-a1d7d70d2473">
    <p><strong>CPU</strong></p>
  </div>
</div>


As can be seen, the average time per epoch on the CPU is roughly .17 seconds and on the GPU it is roughly 1.9 seconds.
