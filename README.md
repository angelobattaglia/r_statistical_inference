# Statistical Inference implementation in R

An implementation of some statistical inference topics in R.

## Setting up a Jupyter Notebook environment with R

The idea is to have three terminal instances: one running Rterm, one jupyter and the other to run git.
The R packages will be installed globally. The Rterm will be the one instance through which we will be installing the packages.
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
# If it is for one user, then:
IRkernel::installspec(user = TRUE)
```

The first command installs the IRkernel package, and the second command registers the kernel with Jupyter.

If you want to install some other library that you'll be using in your notebook sessions, like ggplot2,
you can keep the Rterm opened on the terminal and run the following command:

```R
install.packages('ggplot2')
```

it will install the packages globally and usually these are located somewhere in the file system, the R Shell
should be prompting the path, afterwards.

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

## Alternative (not yet tested)
In R, there is a similar mechanism for creating isolated environments, akin to Python's `virtualenv` or `venv`. 
The R equivalent is typically managed through the **`renv`** package, which allows you to create project-specific environments and manage dependencies.

Here’s how to create a virtual environment in R using `renv`:

1. Install the `renv` package (if you don't have it already):

   ```r
   install.packages("renv")
   ```

2. Initialize a new environment in your project:

   ```r
   renv::init()
   ```

   This will set up an isolated environment for the project, where packages are managed separately from your global R environment.

3. From then on, when you install new packages in the project, they will be installed inside the `renv` environment rather than the global library:

   ```r
   install.packages("ggplot2")  # Example
   ```

4. To save your environment state, you can use:

   ```r
   renv::snapshot()
   ```

   This will record the current state of the environment into a `renv.lock` file.

5. To restore the environment on a different machine or later, you can run:

   ```r
   renv::restore()
   ```

This allows you to maintain reproducibility and isolate package versions for your R projects, much like Python's `venv`.`
