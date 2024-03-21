# Setting up a Jupyter Notebook environment with R
To install and start a Jupyter Notebook session with the R programming language
you'll need to follow these steps (NOTE: highly recommended to use the latest R distribution):

1. **Install R:**

If you haven't already, you need to install R on your system. You can download R from the official CRAN (Comprehensive R Archive Network) website: https://cran.r-project.org/

2. **Install R Kernel for Jupyter:**

To use R in Jupyter Notebooks, you need to install the IRkernel. Open an R console and run the following commands:

```R
install.packages('IRkernel')
# To install it for all users on the local machine
IRkernel::installspec(user = FALSE)
```

The first command installs the IRkernel package, and the second command registers the kernel with Jupyter.

3. **Install Jupyter Notebook:**

If you don't have Jupyter Notebook installed, you can install it using Python's package manager, pip. Open a terminal or command prompt and run:

```bash
pip install notebook
```

4. **Start Jupyter Notebook:**

In the same terminal or command prompt, navigate to the directory where you want to create or open your notebook and run:

```bash
jupyter notebook
```

This command will start the Jupyter Notebook server, and your default web browser will open with the Jupyter dashboard.

5. **Create a New R Notebook:**

Once the Jupyter Notebook dashboard is open, click on the "New" button and select "R" from the drop-down menu. This will create a new notebook with R as the kernel.

Alternatively, you can open an existing notebook or create a new one and change the kernel to R using the "Kernel" menu.

Now you should have a Jupyter Notebook session running with the R kernel, and you can start coding in R within the notebook.

Remember to periodically update your R ages, including IRkernel, to ensure you have the latest versions. You can do this using the `install.packages` function in R.