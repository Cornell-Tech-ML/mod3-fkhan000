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
        <img width="340" alt="simple_gpu_log" src="https://github.com/user-attachments/assets/32edb2f0-202e-4791-b315-0a0876707676">
    <p><strong>GPU</strong></p>
  </div>
  <div style="text-align: center;">
          <img width="341" alt="simple_gpu_log" src="https://github.com/user-attachments/assets/09c9444b-13f1-4388-8bf0-342d657013a1">
    <p><strong>CPU</strong></p>
  </div>
</div>

---


### XOR Dataset
<div style="display: flex; align-items: center;">
  <div style="text-align: center; margin-right: 20px;">
        <img width="340" alt="gpu_xor_log" src="https://github.com/user-attachments/assets/60d1db6f-c450-4cf0-a82b-4ec7855ca91c">
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
        <img width="340" alt="split_gpu_log" src="https://github.com/user-attachments/assets/a2b8c0f4-5cb1-4de4-95f1-3e0156f97a12">
    <p><strong>GPU</strong></p>
  </div>
  <div style="text-align: center;">
    <img width="340" alt="split_cpu_log" src="https://github.com/user-attachments/assets/f99b57f6-13cc-470f-8369-a1d7d70d2473">
    <p><strong>CPU</strong></p>
  </div>
</div>


As can be seen, the average time per epoch on the CPU is roughly .17 seconds and on the GPU it is roughly 1.9 seconds.


Below is a graph showing the amount of time taken to perform matrix multiplication on a CPU vs a GPU:

<img width="331" alt="image" src="https://github.com/user-attachments/assets/ba1953a2-6bba-4a09-aaa0-44b56d927843">

As can be seen, especially for large batches, performing the operation on a GPU is significantly faster.


And here are the results of training using the CPU vs GPU on a larger model.

<img width="340-" alt="cpu_big_model_log" src="https://github.com/user-attachments/assets/de60ce40-5ddf-492c-92ef-c90925e18582">
<p><strong>CPU</strong></p>

<img width="340" alt="gpu_big_model_log" src="https://github.com/user-attachments/assets/c1a697de-7e12-46d6-a63c-1db56afddccc">
<p><strong>GPU</strong></p>


Finally, here you can see the results of the autograder tests for tasks 3_3 and 3_4.
<img width="625" alt="task3_3" src="https://github.com/user-attachments/assets/fc5b095c-f9d7-43b7-bfd2-ad0c4e363ee0">

<img width="619" alt="task3_4" src="https://github.com/user-attachments/assets/5aafeb44-edd2-4f8f-b8eb-17b4ff1e302c">

