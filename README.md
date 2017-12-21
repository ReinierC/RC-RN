# Running React Native for the first time - Reinier Caron
React Native, first project.

I'm running Linux Mint.18 64m Installation will differ on other systems.

---

## Step 1: Install NodeJs

Run this in your terminal:

$``` sudo curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -```

_Alternatively for Node.js v7 add the following repository._

$``` sudo curl -sL https://deb.nodesource.com/setup_7.x | sudo -E bash -```

---

## Step 2: Install Latest Nodejs and NPM

$``` sudo apt-get install -y nodejs```

***_Optional:_*** _There are development tools such as gcc-c++ and make that you need to have on your system, in order to build native addons from npm._

$```sudo apt-get install -y build-essential```

---

### Step 3: Testing Latest Nodejs and NPM

To have a simple test of nodejs and NPM, you can just check the versions installed on your system by using the following commands:

$ ```nodejs --version```

$ ```npm --version```