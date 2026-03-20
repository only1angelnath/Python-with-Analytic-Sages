[Nathaniel Week 2 Assignment.ipynb](https://github.com/user-attachments/files/26142544/Nathaniel.Week.2.Assignment.ipynb)
{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "af08678b-fa52-4f01-ae7d-84f60c8702f3",
   "metadata": {},
   "source": [
    "# Week 2 Assignment"
   ]
  },
  {
   "cell_type": "raw",
   "id": "7b09ea04-cb82-4191-9328-43930accb5f7",
   "metadata": {},
   "source": [
    "Name: Nathaniel Adediran (Angelnath)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "9a6cd393-a695-43cd-bb05-44dff8660143",
   "metadata": {
    "jp-MarkdownHeadingCollapsed": true
   },
   "source": [
    "## Question 1: Variables, Data types and Type Conversion"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "id": "78d63266-4db4-4aac-b960-378e53115ed4",
   "metadata": {},
   "outputs": [],
   "source": [
    "#Question 1A\n",
    "\n",
    "name = 'Nathaniel Adediran'\n",
    "age = 27\n",
    "GPA = 3.87"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "id": "84a48df0-daa5-427e-b899-afb75fe0b804",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Nathaniel Adediran\n",
      "27\n",
      "3.87\n",
      "<class 'str'>\n",
      "<class 'int'>\n",
      "<class 'float'>\n"
     ]
    }
   ],
   "source": [
    "print(name)\n",
    "print(age)\n",
    "print(GPA)\n",
    "print(type(name))\n",
    "print(type(age))\n",
    "print(type(GPA))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "id": "524a5ce7-3b25-4c4e-9d93-311494e30ab6",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Input two numbers separated by a space:  22 13\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "The sum of 22 and 13 is 35\n",
      "The difference between 22 and 13 is 9\n",
      "The product of 22 and 13 is 286\n",
      "The sum of 22 and 13 as a float is 35.0\n",
      "Fuck, I am 27 years old.\n"
     ]
    }
   ],
   "source": [
    "#Question 1B and C\n",
    "\n",
    "prompt = input(\"Input two numbers separated by a space: \")\n",
    "num1, num2 = prompt.split()   #this will split the entered number at the space 20 22 will be 2 numbers 20 and 22 while 202 2 will be 200 and 2 therefore seperate your input by a space or tab\n",
    "num1 = int(num1)\n",
    "num2 = int(num2)\n",
    "sum_result = num1 + num2\n",
    "print(\"The sum of \" + str(num1) + \" and \" + str(num2) + \" is \" + str(sum_result))\n",
    "difference_result = num1 - num2\n",
    "print(\"The difference between \" + str(num1) + \" and \" + str(num2) + \" is \" + str(difference_result))\n",
    "product_result = num1 * num2\n",
    "print(\"The product of \" + str(num1) + \" and \" + str(num2) + \" is \" + str(product_result))\n",
    "float(sum_result)\n",
    "print(\"The sum of \" + str(num1) + \" and \" + str(num2) + \" as a float is \" + str(float(sum_result))) \n",
    "str(age)\n",
    "print(f'Fuck, I am {age} years old.')"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "655106fc-2f54-431d-8eb0-182053e7dd70",
   "metadata": {
    "jp-MarkdownHeadingCollapsed": true
   },
   "source": [
    "## Question 2: Conditionals and Logical Operators"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "id": "6467bb95-00f9-4a54-82d6-99f45280494e",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter any number that comes to your mind:  89\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "Hmmmmm.....Let me think for a second my gee\n",
      "\n",
      "Your lucky number is: 89\n",
      "You entered a positive number.\n",
      "Your number is between 10 and 100 and thats not bad!\n",
      "Your number is odd.\n",
      "\n",
      "Thank you for participating in this quest! The number you entered is 89, it is positive and between 10 and 100 and it is odd.\n"
     ]
    }
   ],
   "source": [
    "# 1. Inputting phase\n",
    "prompt = input('Enter any number that comes to your mind: ')\n",
    "entry = int(prompt)\n",
    "print(f'\\nHmmmmm.....Let me think for a second my gee')\n",
    "print('\\nYour lucky number is: ' + prompt)\n",
    "\n",
    "# --- Check 1: The Sign ---\n",
    "if entry == 0:\n",
    "    sign = \"zero\"\n",
    "    print('You entered zero. Zero is a special number!')\n",
    "elif entry >= 1:\n",
    "    sign = \"positive\"\n",
    "    print('You entered a positive number.')\n",
    "else:\n",
    "    sign = \"negative\"\n",
    "    print('You entered a negative number.')\n",
    "\n",
    "# --- Check 2: The Range (Using Logical Operators) ---\n",
    "if entry >= 10 and entry <= 100:\n",
    "    range_status = \"between 10 and 100\"\n",
    "    print('Your number is between 10 and 100 and thats not bad!')\n",
    "else:\n",
    "    range_status = \"not between 10 and 100\"\n",
    "    print('Your number is not between 10 and 100 but that is still interesting!')\n",
    "\n",
    "# --- Check 3: (Even or Odd) ---\n",
    "if entry % 2 == 0:\n",
    "    parity = \"even\"\n",
    "    print('Your number is even.')\n",
    "else:\n",
    "    parity = \"odd\"\n",
    "    print('Your number is odd.')\n",
    "\n",
    "# --- Final Summary Line ---\n",
    "# We use f-strings (the 'f' before the quotes) to easily plug variables into text\n",
    "print(f\"\\nThank you for participating in this quest! The number you entered is {entry}, it is {sign} and {range_status} and it is {parity}.\")"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "198da1ac-2de9-4195-b5f8-4fa33aa794f3",
   "metadata": {
    "jp-MarkdownHeadingCollapsed": true
   },
   "source": [
    "## Question 3: Loops"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "id": "6c7ccca9-3434-4055-9b1e-26db7314ff61",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "African country: 1.Nigeria\n",
      "African country: 2.Ghana\n",
      "African country: 3.Kenya\n",
      "African country: 4.South Africa\n",
      "African country: 5.Egypt\n"
     ]
    }
   ],
   "source": [
    "#Part A\n",
    "\n",
    "country_list = ['Nigeria', 'Ghana', 'Kenya', 'South Africa', 'Egypt']\n",
    "def print_countries(countries):\n",
    "    for i, country in enumerate(countries, start=1):  #enumerate function allow python to add number to the reult and start=1 hardcore python to bypass 0 and start at 1\n",
    "        print(f'African country: {i}.{country}')\n",
    "\n",
    "print_countries(country_list)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "id": "49fe7b98-16d8-48d5-aa0f-98b3e0553138",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "(Attempt 1 of 3)\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter the passkey:  sickinthehe@d\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Access Denied. Try again.\n",
      "(Attempt 2 of 3)\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter the passkey again:  sick1nthehe@d\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Access Denied. Try again.\n",
      "(Attempt 3 of 3)\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Your last chance:  sickboy\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "--- LOCKOUT ---\n",
      "Too many failed attempts. Try again in 2 hours.\n"
     ]
    }
   ],
   "source": [
    "#Part B\n",
    "passkey = \"S1ck1ndhe@d\"\n",
    "attempts = 0\n",
    "max_attempts = 3\n",
    "\n",
    "while attempts < max_attempts:\n",
    "    attempts += 1\n",
    "    \n",
    "    # Debug line: This shows if the counter working or not\n",
    "    print(f\"(Attempt {attempts} of {max_attempts})\")\n",
    "    \n",
    "    if attempts == 1:\n",
    "        msg = \"Enter the passkey: \"\n",
    "    elif attempts == 2:\n",
    "        msg = \"Enter the passkey again: \"\n",
    "    else:\n",
    "        msg = \"Your last chance: \"\n",
    "        \n",
    "    input_passkey = input(msg)\n",
    "\n",
    "    if input_passkey == passkey:\n",
    "        print(\"Access Granted!\")\n",
    "        break \n",
    "    \n",
    "    # We only print \"try again\" if there are attempts left\n",
    "    if attempts < max_attempts:\n",
    "        print(\"Access Denied. Try again.\")\n",
    "else:\n",
    "    print(\"\\n--- LOCKOUT ---\")\n",
    "    print(\"Too many failed attempts. Try again in 2 hours.\")"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "364fb07f-d4d9-470e-b987-55785761480f",
   "metadata": {
    "jp-MarkdownHeadingCollapsed": true
   },
   "source": [
    "## Question 4: Functions"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "id": "4c852c50-8f80-41ad-99bd-9ac659057daa",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "What is your name?  Angelnath\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "Hello, Angelnath! Welcome to Python programming class with Analytic Sages.\n"
     ]
    }
   ],
   "source": [
    "#Part A\n",
    "name = input(\"What is your name? \")\n",
    "def greet(name):\n",
    "    print(\"\\nHello, \" + name + \"! Welcome to Python programming class with Analytic Sages.\")\n",
    "greet(name)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 18,
   "id": "313c4ab8-1ccb-44fc-9a07-5074291734f4",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "20.41522491349481\n"
     ]
    }
   ],
   "source": [
    "#Part 2a\n",
    "def bmi(weight=59, height=1.7):\n",
    "    \n",
    "    calculated_bmi = weight / (height ** 2)\n",
    "    return calculated_bmi\n",
    "print(bmi())"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "id": "d53679ee-4deb-430b-9b80-2cdc8c5c8a7d",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your weight in kg:  109\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "37.71626297577855\n"
     ]
    }
   ],
   "source": [
    "#part 2b\n",
    "\n",
    "def bmi(weight, height=1.7):\n",
    "    \n",
    "    calculated_bmi = weight / (height ** 2)\n",
    "    return calculated_bmi\n",
    "print(bmi(float(input(\"Enter your weight in kg: \")), 1.7))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 21,
   "id": "a6d352e4-b152-412b-b5bc-e9ce36d6ee21",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter the scores separated by space:  10 15 40\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "The total score is: 65\n"
     ]
    }
   ],
   "source": [
    "#part 3\n",
    "\n",
    "def total_score(*scores):\n",
    "    return sum(scores)\n",
    "scores=input(\"Enter the scores separated by space: \").split()\n",
    "scores = [int(score) for score in scores]  \n",
    "total = total_score(*scores)\n",
    "print(\"The total score is:\", total)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "024c2e14-f2a1-4b8a-8c5c-bf7136589faa",
   "metadata": {
    "jp-MarkdownHeadingCollapsed": true
   },
   "source": [
    "## Question 5: Working with Text files"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 25,
   "id": "954cfa19-9dda-4758-b6ae-f2fdefecb7d7",
   "metadata": {},
   "outputs": [],
   "source": [
    "#creating the text file\n",
    "with open('notes.txt', 'w') as file:\n",
    "    file.write('The first week of Analytics sage python class is hard\\n')\n",
    "    file.write('The second week is kinda easier and more comprehendable\\n')\n",
    "    file.write('All thanks to Tutor freeman style of explaining and carrying everyone along')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 28,
   "id": "26fc42d0-9e32-4cd4-a45e-1f09209eba63",
   "metadata": {},
   "outputs": [],
   "source": [
    "with open('notes.txt', 'a') as file:\n",
    "    file.write('I didnt attend all the second week class except monday class because of electricity problem in the country\\n')\n",
    "    file.write('But I was able to catch up while watching the recording, Thank you \"Agent Y\" your face show, your shoe shine')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 30,
   "id": "c96a0747-92e7-4ba6-82dd-ddcbc7e3a2ef",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "The first week of Analytics sage python class is hard\n",
      "The second week is kinda easier and more comprehendable\n",
      "All thanks to Tutor freeman style of explaining and carrying everyone alongI didnt attend all the second week class except monday class because of electricity problem in the country\n",
      "I didnt attend all the second week class except monday class because of electricity problem in the country\n",
      "But I was able to catch up while watching the recording, Thank you \"Agent Y\" your face show, your shoe shine\n"
     ]
    }
   ],
   "source": [
    "#opening in read mode\n",
    "with open('notes.txt', 'r') as file:\n",
    "    content = file.read()\n",
    "    print(content)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "2090a66a-f1f5-4cdd-a9ef-dfdbf84bd517",
   "metadata": {
    "jp-MarkdownHeadingCollapsed": true
   },
   "source": [
    "## Question 6: Working with CSV files"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 33,
   "id": "905417df-3bc2-4979-a4c7-8c9bd5f489e7",
   "metadata": {},
   "outputs": [],
   "source": [
    "# before using csv in python you must firstly import it\n",
    "import csv"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 35,
   "id": "ba38aa5b-cd6b-44c5-8adf-2530cb6ff17e",
   "metadata": {},
   "outputs": [],
   "source": [
    "#creating the csv\n",
    "with open('product.csv', 'w', newline = \"\") as stuffs:\n",
    "    data=csv.writer(stuffs)\n",
    "\n",
    "    data.writerow(['Product','Price','Quantity'])\n",
    "    data.writerow(['SMP Burner',21000,5])\n",
    "    data.writerow(['Medium Hotplate', 15000, 4])\n",
    "    data.writerow(['Thick Hose', 800, 69])\n",
    "    data.writerow(['Cap and Control', 1600, 25])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 43,
   "id": "326aa63a-8ae4-4888-91ce-51798e3d245d",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "{'Product': 'SMP Burner', 'Price': '21000', 'Quantity': '5'}\n",
      "{'Product': 'Medium Hotplate', 'Price': '15000', 'Quantity': '4'}\n",
      "{'Product': 'Thick Hose', 'Price': '800', 'Quantity': '69'}\n",
      "{'Product': 'Cap and Control', 'Price': '1600', 'Quantity': '25'}\n"
     ]
    }
   ],
   "source": [
    "#reading the data using dictreader()\n",
    "with open('product.csv', 'r') as account:\n",
    "    inventory = csv.DictReader(account)\n",
    "\n",
    "    for goods in inventory:\n",
    "        print(goods)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "6097a6dc-79db-433e-b525-91d403ae9629",
   "metadata": {
    "jp-MarkdownHeadingCollapsed": true
   },
   "source": [
    "## Question 7: Numpy and Pandas"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "cc4ce407-855f-4d99-bdbd-0218cfb35181",
   "metadata": {
    "jp-MarkdownHeadingCollapsed": true
   },
   "source": [
    "### Part A: Numpy"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 44,
   "id": "cd436a40-7a98-401f-99ed-2000439d1bbf",
   "metadata": {},
   "outputs": [],
   "source": [
    "import numpy as np"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 45,
   "id": "eb1bfab7-01ff-4f89-9136-4f9016fbae7e",
   "metadata": {},
   "outputs": [],
   "source": [
    "test_scores = np.array([78,56,89,42,39,49])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 48,
   "id": "1e36ed9d-9cd4-4c2d-bcb0-05bfa3998d4d",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(6,)"
      ]
     },
     "execution_count": 48,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "shape=test_scores.shape\n",
    "shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 51,
   "id": "ec97204d-06a9-4e3f-afb0-a6185c6a7517",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "dtype('int64')"
      ]
     },
     "execution_count": 51,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "types=test_scores.dtype\n",
    "types"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 55,
   "id": "4987001a-ab97-4487-9990-eb84c361cf56",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "The mean score is 58.833333333333336\n",
      "The minimum score is 39\n",
      "The maximum score is 89\n",
      "The standard deviation is 18.524008445498207\n"
     ]
    }
   ],
   "source": [
    "#the arithhmetics\n",
    "avg = np.mean(test_scores)\n",
    "mini = np.min(test_scores)\n",
    "maxi = np.max(test_scores)\n",
    "stdv = np.std(test_scores)\n",
    "print(f'The mean score is {avg}')\n",
    "print(f'The minimum score is {mini}')\n",
    "print(f'The maximum score is {maxi}')\n",
    "print(f'The standard deviation is {stdv}')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 56,
   "id": "79d70277-4a74-415c-ab62-102293233ca1",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[78 89]\n"
     ]
    }
   ],
   "source": [
    "#filtering the array\n",
    "filtered = test_scores[test_scores > 60]\n",
    "print(filtered)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "2f8da04a-84d8-4390-9948-904d974b7933",
   "metadata": {},
   "source": [
    "### Part B: Pandas"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 57,
   "id": "de92acdb-91ae-4aa1-bb68-3000bafd4a93",
   "metadata": {},
   "outputs": [],
   "source": [
    "import pandas as pd"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 63,
   "id": "309dbe32-9ec3-452c-8f31-ec8048ff5b3f",
   "metadata": {},
   "outputs": [],
   "source": [
    "#creating a dataframe from a dictionary\n",
    "student_data = {\n",
    "    'name': ['Nelson', 'Victory', 'Chinyere', 'Dayo', 'Nathaniel', 'Yireal', 'Kagawa', 'Bruno'],\n",
    "    'age': [29,26,29,30,19,18,22,29],\n",
    "    'score': [79, 87, 50, 38, 46, 68, 49, 41],\n",
    "    'grade': ['A','A','C','F','D','B','D','E']\n",
    "}"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 64,
   "id": "5f6718c0-94e7-42ea-9b0c-918c10793edb",
   "metadata": {},
   "outputs": [],
   "source": [
    "df=pd.DataFrame(student_data)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 65,
   "id": "44324ed3-125a-4af6-bbf9-eb2c0968ef7e",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>name</th>\n",
       "      <th>age</th>\n",
       "      <th>score</th>\n",
       "      <th>grade</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Nelson</td>\n",
       "      <td>29</td>\n",
       "      <td>79</td>\n",
       "      <td>A</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Victory</td>\n",
       "      <td>26</td>\n",
       "      <td>87</td>\n",
       "      <td>A</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Chinyere</td>\n",
       "      <td>29</td>\n",
       "      <td>50</td>\n",
       "      <td>C</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Dayo</td>\n",
       "      <td>30</td>\n",
       "      <td>38</td>\n",
       "      <td>F</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>Nathaniel</td>\n",
       "      <td>19</td>\n",
       "      <td>46</td>\n",
       "      <td>D</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>5</th>\n",
       "      <td>Yireal</td>\n",
       "      <td>18</td>\n",
       "      <td>68</td>\n",
       "      <td>B</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>6</th>\n",
       "      <td>Kagawa</td>\n",
       "      <td>22</td>\n",
       "      <td>49</td>\n",
       "      <td>D</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>7</th>\n",
       "      <td>Bruno</td>\n",
       "      <td>29</td>\n",
       "      <td>41</td>\n",
       "      <td>E</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "        name  age  score grade\n",
       "0     Nelson   29     79     A\n",
       "1    Victory   26     87     A\n",
       "2   Chinyere   29     50     C\n",
       "3       Dayo   30     38     F\n",
       "4  Nathaniel   19     46     D\n",
       "5     Yireal   18     68     B\n",
       "6     Kagawa   22     49     D\n",
       "7      Bruno   29     41     E"
      ]
     },
     "execution_count": 65,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 66,
   "id": "a6ed91f2-b90c-4b31-86d5-af1fb7159fa7",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>name</th>\n",
       "      <th>age</th>\n",
       "      <th>score</th>\n",
       "      <th>grade</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Nelson</td>\n",
       "      <td>29</td>\n",
       "      <td>79</td>\n",
       "      <td>A</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Victory</td>\n",
       "      <td>26</td>\n",
       "      <td>87</td>\n",
       "      <td>A</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Chinyere</td>\n",
       "      <td>29</td>\n",
       "      <td>50</td>\n",
       "      <td>C</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "       name  age  score grade\n",
       "0    Nelson   29     79     A\n",
       "1   Victory   26     87     A\n",
       "2  Chinyere   29     50     C"
      ]
     },
     "execution_count": 66,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#showing only the first 3 data\n",
    "df.head(3)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 68,
   "id": "3f8378be-bb93-4cd2-aa8a-4641fb4cc676",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "       name  age  score grade\n",
      "0    Nelson   29     79     A\n",
      "1   Victory   26     87     A\n",
      "2  Chinyere   29     50     C\n",
      "5    Yireal   18     68     B\n"
     ]
    }
   ],
   "source": [
    "#filtering only scores greater than 50\n",
    "filtered=df[df['score']>=50]\n",
    "print(filtered)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 70,
   "id": "65325539-48f6-4fd2-81a9-5c4dfb51a465",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>name</th>\n",
       "      <th>age</th>\n",
       "      <th>score</th>\n",
       "      <th>grade</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Victory</td>\n",
       "      <td>26</td>\n",
       "      <td>87</td>\n",
       "      <td>A</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Nelson</td>\n",
       "      <td>29</td>\n",
       "      <td>79</td>\n",
       "      <td>A</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>5</th>\n",
       "      <td>Yireal</td>\n",
       "      <td>18</td>\n",
       "      <td>68</td>\n",
       "      <td>B</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Chinyere</td>\n",
       "      <td>29</td>\n",
       "      <td>50</td>\n",
       "      <td>C</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>6</th>\n",
       "      <td>Kagawa</td>\n",
       "      <td>22</td>\n",
       "      <td>49</td>\n",
       "      <td>D</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>Nathaniel</td>\n",
       "      <td>19</td>\n",
       "      <td>46</td>\n",
       "      <td>D</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>7</th>\n",
       "      <td>Bruno</td>\n",
       "      <td>29</td>\n",
       "      <td>41</td>\n",
       "      <td>E</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Dayo</td>\n",
       "      <td>30</td>\n",
       "      <td>38</td>\n",
       "      <td>F</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "        name  age  score grade\n",
       "1    Victory   26     87     A\n",
       "0     Nelson   29     79     A\n",
       "5     Yireal   18     68     B\n",
       "2   Chinyere   29     50     C\n",
       "6     Kagawa   22     49     D\n",
       "4  Nathaniel   19     46     D\n",
       "7      Bruno   29     41     E\n",
       "3       Dayo   30     38     F"
      ]
     },
     "execution_count": 70,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.sort_values('score', ascending=False)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 71,
   "id": "7ec144e9-a391-4304-b993-0add9e61faa9",
   "metadata": {},
   "outputs": [],
   "source": [
    "df['Passed'] = np.where(df['score'] >= 50, True, False)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 72,
   "id": "36166b84-aa46-4635-8e89-55b1f7516ef4",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>name</th>\n",
       "      <th>age</th>\n",
       "      <th>score</th>\n",
       "      <th>grade</th>\n",
       "      <th>Passed</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Nelson</td>\n",
       "      <td>29</td>\n",
       "      <td>79</td>\n",
       "      <td>A</td>\n",
       "      <td>True</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Victory</td>\n",
       "      <td>26</td>\n",
       "      <td>87</td>\n",
       "      <td>A</td>\n",
       "      <td>True</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Chinyere</td>\n",
       "      <td>29</td>\n",
       "      <td>50</td>\n",
       "      <td>C</td>\n",
       "      <td>True</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Dayo</td>\n",
       "      <td>30</td>\n",
       "      <td>38</td>\n",
       "      <td>F</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>Nathaniel</td>\n",
       "      <td>19</td>\n",
       "      <td>46</td>\n",
       "      <td>D</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>5</th>\n",
       "      <td>Yireal</td>\n",
       "      <td>18</td>\n",
       "      <td>68</td>\n",
       "      <td>B</td>\n",
       "      <td>True</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>6</th>\n",
       "      <td>Kagawa</td>\n",
       "      <td>22</td>\n",
       "      <td>49</td>\n",
       "      <td>D</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>7</th>\n",
       "      <td>Bruno</td>\n",
       "      <td>29</td>\n",
       "      <td>41</td>\n",
       "      <td>E</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "        name  age  score grade  Passed\n",
       "0     Nelson   29     79     A    True\n",
       "1    Victory   26     87     A    True\n",
       "2   Chinyere   29     50     C    True\n",
       "3       Dayo   30     38     F   False\n",
       "4  Nathaniel   19     46     D   False\n",
       "5     Yireal   18     68     B    True\n",
       "6     Kagawa   22     49     D   False\n",
       "7      Bruno   29     41     E   False"
      ]
     },
     "execution_count": 72,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 73,
   "id": "a01ff633-3209-44bf-80fc-6722ca4446b7",
   "metadata": {},
   "outputs": [],
   "source": [
    "#saving the dataframe as csv\n",
    "\n",
    "df.to_csv('class_result.csv', index=False)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 74,
   "id": "8f65cbc6-c7f4-466a-9368-2c51ecaebfd9",
   "metadata": {},
   "outputs": [],
   "source": [
    "#reloading it back into python\n",
    "reloaded_score = pd.read_csv('class_result.csv')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 75,
   "id": "0f5d20cf-107f-4b75-9eda-315b77bc0f6a",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>name</th>\n",
       "      <th>age</th>\n",
       "      <th>score</th>\n",
       "      <th>grade</th>\n",
       "      <th>Passed</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Nelson</td>\n",
       "      <td>29</td>\n",
       "      <td>79</td>\n",
       "      <td>A</td>\n",
       "      <td>True</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Victory</td>\n",
       "      <td>26</td>\n",
       "      <td>87</td>\n",
       "      <td>A</td>\n",
       "      <td>True</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Chinyere</td>\n",
       "      <td>29</td>\n",
       "      <td>50</td>\n",
       "      <td>C</td>\n",
       "      <td>True</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Dayo</td>\n",
       "      <td>30</td>\n",
       "      <td>38</td>\n",
       "      <td>F</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>Nathaniel</td>\n",
       "      <td>19</td>\n",
       "      <td>46</td>\n",
       "      <td>D</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>5</th>\n",
       "      <td>Yireal</td>\n",
       "      <td>18</td>\n",
       "      <td>68</td>\n",
       "      <td>B</td>\n",
       "      <td>True</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>6</th>\n",
       "      <td>Kagawa</td>\n",
       "      <td>22</td>\n",
       "      <td>49</td>\n",
       "      <td>D</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>7</th>\n",
       "      <td>Bruno</td>\n",
       "      <td>29</td>\n",
       "      <td>41</td>\n",
       "      <td>E</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "        name  age  score grade  Passed\n",
       "0     Nelson   29     79     A    True\n",
       "1    Victory   26     87     A    True\n",
       "2   Chinyere   29     50     C    True\n",
       "3       Dayo   30     38     F   False\n",
       "4  Nathaniel   19     46     D   False\n",
       "5     Yireal   18     68     B    True\n",
       "6     Kagawa   22     49     D   False\n",
       "7      Bruno   29     41     E   False"
      ]
     },
     "execution_count": 75,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "reloaded_score"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "df3cb774-bf88-480d-aeea-7b78e6329c89",
   "metadata": {},
   "source": [
    "## Question 8: Data Visualization"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "4fc47239-f6c0-4e92-9004-ccc702a30870",
   "metadata": {
    "jp-MarkdownHeadingCollapsed": true
   },
   "source": [
    "### Step 1: Load and Explore"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "id": "70243c51-eeb7-49ea-b31d-9aa778d4f684",
   "metadata": {},
   "outputs": [],
   "source": [
    "import pandas as pd\n",
    "import matplotlib.pyplot as plt\n",
    "import seaborn as sns"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "id": "10f93e50-60e8-42de-b3d6-f1b75a5a895c",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>name</th>\n",
       "      <th>abbr</th>\n",
       "      <th>crypturl</th>\n",
       "      <th>price</th>\n",
       "      <th>volume24hrs</th>\n",
       "      <th>marketcap</th>\n",
       "      <th>circulatingsupply</th>\n",
       "      <th>maxsupply</th>\n",
       "      <th>totalsupply</th>\n",
       "      <th>date_taken</th>\n",
       "      <th>Unnamed: 10</th>\n",
       "      <th>Unnamed: 11</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Bitcoin</td>\n",
       "      <td>BTC</td>\n",
       "      <td>https://crypto.com/price/bitcoin</td>\n",
       "      <td>62732.6700</td>\n",
       "      <td>272076.9766</td>\n",
       "      <td>2,51,418.65</td>\n",
       "      <td>3.065439e+06</td>\n",
       "      <td>876052496.2</td>\n",
       "      <td>437497786.1</td>\n",
       "      <td>09-08-2007</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Ethereum</td>\n",
       "      <td>ETH</td>\n",
       "      <td>https://crypto.com/price/ethereum</td>\n",
       "      <td>3027.2200</td>\n",
       "      <td>981408.7883</td>\n",
       "      <td>5,02,924.62</td>\n",
       "      <td>2.326224e+06</td>\n",
       "      <td>444082823.2</td>\n",
       "      <td>705224728.4</td>\n",
       "      <td>13-12-2007</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Tether</td>\n",
       "      <td>USDT</td>\n",
       "      <td>https://crypto.com/price/tether</td>\n",
       "      <td>0.9999</td>\n",
       "      <td>944792.0394</td>\n",
       "      <td>8,15,637.23</td>\n",
       "      <td>2.207000e+06</td>\n",
       "      <td>604510133.4</td>\n",
       "      <td>716566396.6</td>\n",
       "      <td>03-03-2004</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>BNB</td>\n",
       "      <td>BNB</td>\n",
       "      <td>https://crypto.com/price/bnb</td>\n",
       "      <td>593.8500</td>\n",
       "      <td>556334.5330</td>\n",
       "      <td>3,23,746.05</td>\n",
       "      <td>2.400147e+05</td>\n",
       "      <td>150451882.8</td>\n",
       "      <td>685308596.6</td>\n",
       "      <td>06-06-2001</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>Solana</td>\n",
       "      <td>SOL</td>\n",
       "      <td>https://crypto.com/price/solana</td>\n",
       "      <td>152.5900</td>\n",
       "      <td>866929.0575</td>\n",
       "      <td>8,05,143.57</td>\n",
       "      <td>2.957790e+06</td>\n",
       "      <td>284280494.2</td>\n",
       "      <td>647877254.0</td>\n",
       "      <td>06-08-2019</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "       name  abbr                           crypturl       price  volume24hrs  \\\n",
       "0   Bitcoin   BTC   https://crypto.com/price/bitcoin  62732.6700  272076.9766   \n",
       "1  Ethereum   ETH  https://crypto.com/price/ethereum   3027.2200  981408.7883   \n",
       "2    Tether  USDT    https://crypto.com/price/tether      0.9999  944792.0394   \n",
       "3       BNB   BNB       https://crypto.com/price/bnb    593.8500  556334.5330   \n",
       "4    Solana   SOL    https://crypto.com/price/solana    152.5900  866929.0575   \n",
       "\n",
       "     marketcap  circulatingsupply    maxsupply  totalsupply  date_taken  \\\n",
       "0  2,51,418.65       3.065439e+06  876052496.2  437497786.1  09-08-2007   \n",
       "1  5,02,924.62       2.326224e+06  444082823.2  705224728.4  13-12-2007   \n",
       "2  8,15,637.23       2.207000e+06  604510133.4  716566396.6  03-03-2004   \n",
       "3  3,23,746.05       2.400147e+05  150451882.8  685308596.6  06-06-2001   \n",
       "4  8,05,143.57       2.957790e+06  284280494.2  647877254.0  06-08-2019   \n",
       "\n",
       "   Unnamed: 10  Unnamed: 11  \n",
       "0          NaN          NaN  \n",
       "1          NaN          NaN  \n",
       "2          NaN          NaN  \n",
       "3          NaN          NaN  \n",
       "4          NaN          NaN  "
      ]
     },
     "execution_count": 2,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#loading csv in \n",
    "cd = pd.read_csv('Crypto.csv')\n",
    "cd.head(5)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "id": "61e83ca3-8b0f-4d05-b0f5-56b9a692b2a4",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>name</th>\n",
       "      <th>price</th>\n",
       "      <th>volume24hrs</th>\n",
       "      <th>marketcap</th>\n",
       "      <th>circulatingsupply</th>\n",
       "      <th>maxsupply</th>\n",
       "      <th>totalsupply</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Bitcoin</td>\n",
       "      <td>62732.6700</td>\n",
       "      <td>272076.9766</td>\n",
       "      <td>2,51,418.65</td>\n",
       "      <td>3.065439e+06</td>\n",
       "      <td>876052496.2</td>\n",
       "      <td>437497786.1</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Ethereum</td>\n",
       "      <td>3027.2200</td>\n",
       "      <td>981408.7883</td>\n",
       "      <td>5,02,924.62</td>\n",
       "      <td>2.326224e+06</td>\n",
       "      <td>444082823.2</td>\n",
       "      <td>705224728.4</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Tether</td>\n",
       "      <td>0.9999</td>\n",
       "      <td>944792.0394</td>\n",
       "      <td>8,15,637.23</td>\n",
       "      <td>2.207000e+06</td>\n",
       "      <td>604510133.4</td>\n",
       "      <td>716566396.6</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>BNB</td>\n",
       "      <td>593.8500</td>\n",
       "      <td>556334.5330</td>\n",
       "      <td>3,23,746.05</td>\n",
       "      <td>2.400147e+05</td>\n",
       "      <td>150451882.8</td>\n",
       "      <td>685308596.6</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>Solana</td>\n",
       "      <td>152.5900</td>\n",
       "      <td>866929.0575</td>\n",
       "      <td>8,05,143.57</td>\n",
       "      <td>2.957790e+06</td>\n",
       "      <td>284280494.2</td>\n",
       "      <td>647877254.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "       name       price  volume24hrs    marketcap  circulatingsupply  \\\n",
       "0   Bitcoin  62732.6700  272076.9766  2,51,418.65       3.065439e+06   \n",
       "1  Ethereum   3027.2200  981408.7883  5,02,924.62       2.326224e+06   \n",
       "2    Tether      0.9999  944792.0394  8,15,637.23       2.207000e+06   \n",
       "3       BNB    593.8500  556334.5330  3,23,746.05       2.400147e+05   \n",
       "4    Solana    152.5900  866929.0575  8,05,143.57       2.957790e+06   \n",
       "\n",
       "     maxsupply  totalsupply  \n",
       "0  876052496.2  437497786.1  \n",
       "1  444082823.2  705224728.4  \n",
       "2  604510133.4  716566396.6  \n",
       "3  150451882.8  685308596.6  \n",
       "4  284280494.2  647877254.0  "
      ]
     },
     "execution_count": 3,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#selecting only the needed columns\n",
    "ncd = cd[['name', 'price', 'volume24hrs', 'marketcap', 'circulatingsupply', 'maxsupply', 'totalsupply']]\n",
    "ncd.head(5)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "id": "63fdb3b8-8e12-44ff-baa0-6b353313956a",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(21347, 7)"
      ]
     },
     "execution_count": 4,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "ncd.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "id": "8b2d4949-b46c-4bef-b633-b9f26dcd574c",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>price</th>\n",
       "      <th>volume24hrs</th>\n",
       "      <th>circulatingsupply</th>\n",
       "      <th>maxsupply</th>\n",
       "      <th>totalsupply</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>count</th>\n",
       "      <td>2.134700e+04</td>\n",
       "      <td>21347.000000</td>\n",
       "      <td>2.134700e+04</td>\n",
       "      <td>2.134700e+04</td>\n",
       "      <td>2.134700e+04</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>mean</th>\n",
       "      <td>7.524758e+04</td>\n",
       "      <td>488514.745820</td>\n",
       "      <td>2.109302e+06</td>\n",
       "      <td>5.000418e+08</td>\n",
       "      <td>5.005749e+08</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>std</th>\n",
       "      <td>1.092127e+07</td>\n",
       "      <td>283506.240054</td>\n",
       "      <td>1.225969e+06</td>\n",
       "      <td>2.876037e+08</td>\n",
       "      <td>2.893756e+08</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>min</th>\n",
       "      <td>0.000000e+00</td>\n",
       "      <td>103.983721</td>\n",
       "      <td>1.669758e+02</td>\n",
       "      <td>2.041145e+04</td>\n",
       "      <td>5.213366e+04</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>25%</th>\n",
       "      <td>1.000000e-05</td>\n",
       "      <td>241306.259550</td>\n",
       "      <td>1.041184e+06</td>\n",
       "      <td>2.518438e+08</td>\n",
       "      <td>2.498050e+08</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>50%</th>\n",
       "      <td>9.548000e-04</td>\n",
       "      <td>487505.451700</td>\n",
       "      <td>2.103832e+06</td>\n",
       "      <td>5.013132e+08</td>\n",
       "      <td>5.028731e+08</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>75%</th>\n",
       "      <td>3.687500e-02</td>\n",
       "      <td>733224.487850</td>\n",
       "      <td>3.163273e+06</td>\n",
       "      <td>7.469720e+08</td>\n",
       "      <td>7.507950e+08</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>max</th>\n",
       "      <td>1.595659e+09</td>\n",
       "      <td>981555.184500</td>\n",
       "      <td>4.251433e+06</td>\n",
       "      <td>9.989293e+08</td>\n",
       "      <td>9.999478e+08</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "              price    volume24hrs  circulatingsupply     maxsupply  \\\n",
       "count  2.134700e+04   21347.000000       2.134700e+04  2.134700e+04   \n",
       "mean   7.524758e+04  488514.745820       2.109302e+06  5.000418e+08   \n",
       "std    1.092127e+07  283506.240054       1.225969e+06  2.876037e+08   \n",
       "min    0.000000e+00     103.983721       1.669758e+02  2.041145e+04   \n",
       "25%    1.000000e-05  241306.259550       1.041184e+06  2.518438e+08   \n",
       "50%    9.548000e-04  487505.451700       2.103832e+06  5.013132e+08   \n",
       "75%    3.687500e-02  733224.487850       3.163273e+06  7.469720e+08   \n",
       "max    1.595659e+09  981555.184500       4.251433e+06  9.989293e+08   \n",
       "\n",
       "        totalsupply  \n",
       "count  2.134700e+04  \n",
       "mean   5.005749e+08  \n",
       "std    2.893756e+08  \n",
       "min    5.213366e+04  \n",
       "25%    2.498050e+08  \n",
       "50%    5.028731e+08  \n",
       "75%    7.507950e+08  \n",
       "max    9.999478e+08  "
      ]
     },
     "execution_count": 5,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# descriptive analysis of quantitative columns\n",
    "ncd.describe()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "id": "fb1b1ead-a560-47ed-b979-b5502419464c",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>name</th>\n",
       "      <th>marketcap</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>count</th>\n",
       "      <td>21347</td>\n",
       "      <td>21347</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>unique</th>\n",
       "      <td>20807</td>\n",
       "      <td>21347</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>top</th>\n",
       "      <td>MAGA</td>\n",
       "      <td>2,51,418.65</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>freq</th>\n",
       "      <td>11</td>\n",
       "      <td>1</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "         name    marketcap\n",
       "count   21347        21347\n",
       "unique  20807        21347\n",
       "top      MAGA  2,51,418.65\n",
       "freq       11            1"
      ]
     },
     "execution_count": 6,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# descriptive analysis of nominal rolls\n",
    "\n",
    "ncd.describe(include=['str'])"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "ea312802-60a5-4c82-8bee-4377aa175518",
   "metadata": {},
   "source": [
    "### Step 2: Line Chart"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "id": "8111b9e1-49b8-433b-ab16-b9a45882e391",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>name</th>\n",
       "      <th>price</th>\n",
       "      <th>volume24hrs</th>\n",
       "      <th>marketcap</th>\n",
       "      <th>circulatingsupply</th>\n",
       "      <th>maxsupply</th>\n",
       "      <th>totalsupply</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Bitcoin</td>\n",
       "      <td>62732.6700</td>\n",
       "      <td>272076.9766</td>\n",
       "      <td>2,51,418.65</td>\n",
       "      <td>3.065439e+06</td>\n",
       "      <td>876052496.2</td>\n",
       "      <td>437497786.1</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Ethereum</td>\n",
       "      <td>3027.2200</td>\n",
       "      <td>981408.7883</td>\n",
       "      <td>5,02,924.62</td>\n",
       "      <td>2.326224e+06</td>\n",
       "      <td>444082823.2</td>\n",
       "      <td>705224728.4</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Tether</td>\n",
       "      <td>0.9999</td>\n",
       "      <td>944792.0394</td>\n",
       "      <td>8,15,637.23</td>\n",
       "      <td>2.207000e+06</td>\n",
       "      <td>604510133.4</td>\n",
       "      <td>716566396.6</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>BNB</td>\n",
       "      <td>593.8500</td>\n",
       "      <td>556334.5330</td>\n",
       "      <td>3,23,746.05</td>\n",
       "      <td>2.400147e+05</td>\n",
       "      <td>150451882.8</td>\n",
       "      <td>685308596.6</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>Solana</td>\n",
       "      <td>152.5900</td>\n",
       "      <td>866929.0575</td>\n",
       "      <td>8,05,143.57</td>\n",
       "      <td>2.957790e+06</td>\n",
       "      <td>284280494.2</td>\n",
       "      <td>647877254.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "       name       price  volume24hrs    marketcap  circulatingsupply  \\\n",
       "0   Bitcoin  62732.6700  272076.9766  2,51,418.65       3.065439e+06   \n",
       "1  Ethereum   3027.2200  981408.7883  5,02,924.62       2.326224e+06   \n",
       "2    Tether      0.9999  944792.0394  8,15,637.23       2.207000e+06   \n",
       "3       BNB    593.8500  556334.5330  3,23,746.05       2.400147e+05   \n",
       "4    Solana    152.5900  866929.0575  8,05,143.57       2.957790e+06   \n",
       "\n",
       "     maxsupply  totalsupply  \n",
       "0  876052496.2  437497786.1  \n",
       "1  444082823.2  705224728.4  \n",
       "2  604510133.4  716566396.6  \n",
       "3  150451882.8  685308596.6  \n",
       "4  284280494.2  647877254.0  "
      ]
     },
     "execution_count": 7,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#before starting the chart let me reduce the data to just 30 token\n",
    "just30= ncd.head(30)\n",
    "just30.head(5)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "id": "9ec89d24-d7b4-4ebe-b600-fb447368c965",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAABmsAAAHWCAYAAACYKb1QAAAAOnRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjEwLjgsIGh0dHBzOi8vbWF0cGxvdGxpYi5vcmcvwVt1zgAAAAlwSFlzAAAPYQAAD2EBqD+naQAAqhBJREFUeJzs3Qd8HMXZx/FHxZLcJEsyNjZusi3Rew8lAYxNSSGUQEKAUAMBAjaBlxZDKCGhmQ4JhJJAQkkIPTYOPQECmNDBEi7Y4IokS66yLN37+Y89l9X5TjrVa7+vP+c73e3tzc7uzs7uszOTFQqFQgYAAAAAAAAAAICEyE7MzwIAAAAAAAAAAEAI1gAAAAAAAAAAACQQwRoAAAAAAAAAAIAEIlgDAAAAAAAAAACQQARrAAAAAAAAAAAAEohgDQAAAAAAAAAAQAIRrAEAAAAAAAAAAEgggjUAAAAAAAAAAAAJRLAGAAAAAAAAAAAggQjWAAAAAEgJP/nJT2zUqFGWrKqqqmz8+PFWVFRkWVlZ9sQTT3Tr733rW9+ybbbZplt/AwAAAEDPIFgDAAAAoNvdf//9LoDhHwUFBVZRUWFnnXWWLV68OC3WwAknnGAffvihXX311fanP/3Jdtlll6gBlmA+xHpcfvnlCVkGAAAAAImRm6DfBQAAAJCBrrjiCisrK7M1a9bYv/71L7vzzjvtueees48++sj69OnT6nfvvvtua25utmS0evVqe+ONN+ySSy5xAahY9Pkpp5wS/vvtt9+2W265xS6++GLbcsstw+9vt9123Z5mAAAAAMmDYA0AAACAHnPwwQeHW5woaFFaWmo33nijPfnkk/bDH/4w6ndWrlxpffv2tV69eiXtmlq6dKl7HjBgQKvTHXjggS3+VgsjBWv0vlrdAAAAAMhMdIMGAAAAIGH2339/9zxnzpzwuDT9+vWzWbNm2SGHHGL9+/e3Y489NuaYNWppc/PNN9u2227rAh+bbLKJHXTQQfbOO++0mO7BBx+0nXfe2Xr37m0lJSV2zDHH2Pz58+NK43//+18XZCosLHRpO+CAA+zNN98Mf64uy0aOHOlen3/++a4bs86OrXPHHXfY1ltvbfn5+TZ06FA788wzbdmyZW1+7/nnn3ctlBT4WrdunXvvs88+syOPPNItt/JIwbKnnnoqajd1//73v23SpEkuHxUg+/73vx8ORHnK2wkTJtjAgQNdfqql1EknndSp5QUAAAAyHS1rAAAAACSMgjKiFjaeggwKBuy99952/fXXt9o92sknn+wCDQqmqKWOvvvaa6+5YIpvwaMxZH75y1/aD37wAzeNgg+33nqr7bvvvi4Q01prmI8//tj22WcfF6i54IILXOue3/3ud64VzCuvvGK77767HX744W4eEydOdEESBZkU1OkoBX9+9atf2bhx4+yMM86wmTNnuu7i1GWagimxWhg988wzLihz9NFH27333ms5OTku/XvttZdtttlmduGFF7oAzKOPPmqHHXaY/e1vf3PBmKCzzz7biouL7bLLLrO5c+faTTfd5Lp1e+SRR9znS5YssfHjx7tgjuan5dZ0jz/+eIeXFwAAAADBGgAAAAA9qK6uzr7++ms3Zo0CDxrDRq0zvv3tb4enaWhosKOOOsquueaaVuf10ksvuUDNz3/+c9e6xjvvvPMsFAq511988YULPFx11VVuXBhPAZYdd9zRtWAJvh/p0ksvtcbGRje+zujRo917xx9/vG2++eYueKOAjcaXUTBHwZqddtrJfvzjH3c4fxRI0nIrIPKPf/zDsrPXd4awxRZbuKCJWgideOKJG31PwRK1FlLro7vuuiv8vXPOOcdGjBjhAj1qpSM/+9nPXCDs//7v/zYK1ihoptY5amXjWy6pmzatt6KiInv99dettrbWTeODYaL8BQAAANBxdIMGAAAAoMeotYhaZQwfPtwFF9QC5e9//7tr+RGkFiVtUcsQBRUUjInkgw0KYijgoFY1ChL5x6abbmrl5eUu4BNLU1OTC0qoFYoP1MiQIUPsRz/6kQvg1NfXW1f65z//aWvXrrVzzz03HHCRU0891QWEnn322Y2+85e//MW1pvnpT3/qWv3479XU1NiLL77oln358uXhZa+urnYtl6qqquyrr75qMa/TTjstnHeiVkXKBwW9xLdCUiseBbEAAAAAdA26QQMAAADQY26//XarqKiw3NxcGzx4sGuhEgxKiD4bNmxYXF2oaTwXjcUSiwISamWjwEw0sboU861cVq1a5dIYacstt3RBII17o7FluooPikT+Zl5engsY+c89jfWjljxqiaSu3YI+//xzt+zqAk6PaNStWTBQplY4QeoSTdSaRr75zW/aEUcc4bppmzJliusOTsEsBa98yx0AAAAA7UewBgAAAECP2W233Vp0nxWNLvpHBnA6SgEVtRRRl2IawyVSZ8aWSQZq5aPHc889Z++8806LvNWyyy9+8QvXkiaasWPHtvg7Wh6J71ZOefnXv/7VjQn09NNP27Rp0+ykk06yG264wb2X6vkJAAAAJArBGgAAAAApacyYMS5YoO6+YrWu0TQKNJSVlbkWPe2h7tr69OljM2fO3Oizzz77zAWU1J1bVxo5cqR71m8Gu15T12hqRaNu5IIKCgpcl2T777+/HXTQQW4MHd/Sx39frYciv9dZe+yxh3tcffXV9uc//9mOPfZYe/jhh+2UU07p0t8BAAAAMgVj1gAAAABISeqOS4EYdckVqyXI4Ycf7lqLaBr/XnAajd8Si743fvx4e/LJJ23u3Lnh9xcvXuwCFHvvvbcbR6YrKaiiLs9uueWWFun9wx/+YHV1dXbooYdu9J2ioiIXtBo0aJAdeOCBrns40d/qpkzj2CxcuDBqN2/tpe7QIvNxhx12cM8NDQ3tnh8AAACA9WhZAwAAACAl7bfffnbccce5wIbGplHLEnX99dprr7nPzjrrLNey5qqrrrKLLrrIBVw0vkr//v1dK5W///3vdtppp7luwmLRd6dPn+4CMz/72c/ceDoKfigwce2113b5Mqk1j9Kq4JKW57vf/a5rZXPHHXfYrrvu6saniWbgwIHhdCrg869//cuNRaMxgvTetttua6eeeqprbaNg0xtvvGFffvmlvf/+++1K3wMPPODS8v3vf9/l7fLly+3uu+92QatDDjmki3IBAAAAyDwEawAAAACkrPvuu8+222471/Lk/PPPd61MNG7LN77xjfA0F154oesCbcqUKeFWOOq+TK1mFAxpjboUU/BHAZRrrrnGBYN23313e/DBB91zd7j88std0Oa2226ziRMnui7eFFT69a9/7bo0i0XBmX/+85+2zz77uBY2r776qm211VZuLBst9/333+9aEqnFzY477miTJ09ud9q++c1v2ltvveW6PFPQR/mtcYgeeugh19UcAAAAgI7JCkW2YQcAAAAAAAAAAECPYcwaAAAAAAAAAACABCJYAwAAAAAAAAAAkEAEawAAAAAAAAAAABKIYA0AAAAAAAAAAEACEawBAAAAAAAAAABIIII1AAAAAAAAAAAACZSbyB9PJ83NzbZgwQLr37+/ZWVlJTo5AAAAAAAAAAAggUKhkC1fvtyGDh1q2dmtt50hWNNFFKgZPnx4V80OAAAAAAAAAACkgfnz59uwYcNanYZgTRdRixqf6YWFhV01WwAAAAAAAAAAkILq6+tdIw8fP2gNwZou4rs+U6CGYA0AAAAAAAAAAJB4hk5pvZM0AAAAAAAAAAAAdCuCNQAAAAAAAAAAAAlEsAYAAAAAAAAAACCBCNYAAAAAAAAAAAAkEMEaAAAAAAAAAACABCJYAwAAAAAAAAAAkEAEawAAAAAAAAAAABKIYA0AAAAAAAAAAEACEawBAAAAAAAAAABIIII1AAAAAAAAAAAACUSwBgAAAAAAAAAAIIEI1gAAAAAAAAAAACQQwRoAAAAAAAAAAIAEIliDbvXSnJfsW/d/y0596lRyGgAAIA28OOdFG/+n8fZ5zeeJTgoAAAAApA2CNehWjc2N9soXr9jrX75OTgMAAKSB2966zabPnm4PfvBgopMCAAAAAGmDYA26VXlJuXvWnZdNzU3kNgAAQIrzLWpm1c5KdFIAAAAAIG0QrEG3GlE0wvJy8mxt01qbXz+f3AYAAEhhoVAoHKShGzQAAAAA6DoEa9CtcrJzbEzxGPe6srqS3AYAAEhhi1YsslWNq9zrWTW0rAEAAACArkKwBt2uvHR9V2hV1VXkNgAAQAoLtqZZumqp1TfUJzQ9AAAAAJAuCNagx8atqaohWAMAAJDKIsepoXUNAAAAAHQNgjXodhWlFe6ZbtAAAABSW+Q4NYxbAwAAAABdg2ANuh0tawAAANIDwRoAAAAA6B4Ea9BjY9bMqZ1jjU2N5DgAAECKd4O246Y7tvgbAAAAANA5BGvQ7Yb2H2p9evWxplCTzVk2hxwHAABI8ZY1E8ZMaPE3AAAAAKBzCNag22VnZdvYkrHudVV1FTkOAACQgmpW19iyNcvc6wPHHOieaVkDAAAAAF2DYA16BOPWAAAApDbfikatprcbvJ17/WX9l7a6cXWCUwYAAAAAqS/hwZqvvvrKfvzjH1tpaan17t3btt12W3vnnXfCn4dCIZs8ebINGTLEfT5u3DirqmrZOqOmpsaOPfZYKywstAEDBtjJJ59sK1asaDHNBx98YPvss48VFBTY8OHD7dprr90oLY899phtscUWbhql47nnnuvGJc8sFaUV7rmyujLRSQEAAEAHzKpZPz7NmOIxVtq71ArzC93fdHMLAAAAACkerKmtrbW99trLevXqZf/4xz/sk08+sRtuuMGKi4vD0yiocsstt9hdd91l//nPf6xv3742YcIEW7NmTXgaBWo+/vhjmz59uj3zzDP26quv2mmnnRb+vL6+3saPH28jR460GTNm2HXXXWeXX365/f73vw9P8/rrr9sPf/hDF+j573//a4cddph7fPTRRz2YI+mLljUAAADp0bJG3dtmZWWFu7ll3BoAAAAA6LxcS6Df/va3rpXLfffdF36vrKysRauam266yS699FL73ve+59774x//aIMHD7YnnnjCjjnmGPv0009t6tSp9vbbb9suu+ziprn11lvtkEMOseuvv96GDh1qDz30kK1du9buvfdey8vLs6233tree+89u/HGG8NBnZtvvtkOOuggO//8893fV155pQv+3HbbbS5QhM4pLy13z4xZAwAAkJr8+DQ+SKPndxe+G25xAwAAAABI0ZY1Tz31lAuwHHXUUTZo0CDbcccd7e677w5/PmfOHFu0aJHr+swrKiqy3Xff3d544w33t57V9ZkP1Iimz87Odi1x/DT77ruvC9R4ap0zc+ZM17rHTxP8HT+N/51IDQ0NrsVO8IG2u0GbVzfP1qz7X6soAAAApAbfgkbdoAWfaVkDAAAAACkerJk9e7bdeeedVl5ebtOmTbMzzjjDfv7zn9sDDzzgPlegRtSSJkh/+8/0rEBPUG5urpWUlLSYJto8gr8Raxr/eaRrrrnGBY78Qy2EENsmfTZx/ZqHLMTdlwAAAGnSsib4PgAAAAAgRYM1zc3NttNOO9mvf/1r16pGXZKdeuqpKdHt2EUXXWR1dXXhx/z58xOdpKSmfs0ZtwYAACA1rVi7whatWH8T05gSWtYAAAAAQFoFa4YMGWJbbbVVi/e23HJLmzdvnnu96aabuufFixe3mEZ/+8/0vGTJkhafr1u3zmpqalpME20ewd+INY3/PFJ+fr4VFha2eCC+rtAqqyvJKgAAgBQyu3a2ey7tXWoDCga0aFnzRd0X1tjUmND0AQAAAECqS2iwZq+99nLjxgRVVlbayJEj3euysjIXLHnhhRfCn2tsGI1Fs+eee7q/9bxs2TKbMWNGeJoXX3zRtdrR2DZ+mldffdUaG/93Ejl9+nTbfPPNrbi4ODxN8Hf8NP530HnhljXVVWQnAABAKo5Xs6FVjQzpP8QKcgtsXfM6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ZWWFW9dUVleyNgAAABLMt4jpSMua4Pd8d2oAAAAAgLYRrEHClZeuD9ZUVVclOikAAAAZr8ta1tTSsgYAAAAA4kWwBgnnW9ZU1RCsAQAASKSGdQ02v36+ez2mZEyngjW0rAEAAACA+BGsQcJVlFa4Z7pBAwAASKy5y+Zac6jZ+vbqa4P7Du5cN2i1s9y8AAAAAABtI1iDhKNlDQAAQJKNV1Myxo0t2BEjB4y03OxcW7NujS1cvrCLUwgAAAAA6YlgDZJmzJr5dfNtdePqRCcHAAAgY3V2vBpRoGZk0cgW8wMAAAAAtI5gDRJukz6bWFF+kYUsFL6bEwAAAD3PjzMztrjjwZoW49ZQtwMAAACAuBCsQcKpiw3fuqaquirRyQEAAMhYn9d+Hu4GrTP8uDW0rAEAAACA+BCsQVJg3BoAAIAkalnTiW7Qgt8nWAMAAAAAKRCsufzyy12riuBjiy22CH++Zs0aO/PMM620tNT69etnRxxxhC1evLjFPObNm2eHHnqo9enTxwYNGmTnn3++rVu3rsU0L7/8su20006Wn59vY8eOtfvvv3+jtNx+++02atQoKygosN13393eeuutblxyRKoorXDPldWVZA4AAEACNDU32eza2S1axnSUb5lDN2gAAAAAkCIta7beemtbuHBh+PGvf/0r/NnEiRPt6aeftscee8xeeeUVW7BggR1++OHhz5uamlygZu3atfb666/bAw884AIxkydPDk8zZ84cN81+++1n7733np177rl2yimn2LRp08LTPPLIIzZp0iS77LLL7N1337Xtt9/eJkyYYEuWLOnBnMhstKwBAABIrC/rv7TG5kbLy8mzYYXDuqxlTSgU6qIUAgAAAED6SniwJjc31zbddNPwY+DAge79uro6+8Mf/mA33nij7b///rbzzjvbfffd54Iyb775ppvm+eeft08++cQefPBB22GHHezggw+2K6+80rWSUQBH7rrrLisrK7MbbrjBttxySzvrrLPsyCOPtClTpoTToN849dRT7cQTT7StttrKfUctde69994E5UrmYcwaAACAxPJdlpUNKLOc7JxOzUvzkPqGeqteXd0l6QMAAACAdJbwYE1VVZUNHTrURo8ebccee6zr1kxmzJhhjY2NNm7cuPC06iJtxIgR9sYbb7i/9bztttva4MGDw9OoRUx9fb19/PHH4WmC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8b158+bZoYcean369LFBgwbZ+eefb+vWrWsxzcsvv2w77bST5efn29ixY+3+++/f6Pdvv/12GzVqlBUUFNjuu+9ub731VjcuLdqDljUAAADp0bJGxhaPbZEeAAAAAMh0SROsefvtt+13v/udbbfddi3enzhxoj399NP22GOP2SuvvGILFiywww8/PPx5U1OTC9SsXbvWXn/9dXvggQdcIGby5MnhaebMmeOm2W+//ey9995zwaBTTjnFpk2bFp7mkUcesUmTJtlll11m7777rm2//fY2YcIEW7JkSQ/lAFrDmDUAAADpMWZNi5Y1G1r6AAAAAECmS4pgzYoVK+zYY4+1u+++24qLi8Pv19XV2R/+8Ae78cYbbf/997edd97Z7rvvPheUefPNN900zz//vH3yySf24IMP2g477GAHH3ywXXnlla6VjAI4ctddd1lZWZndcMMNtuWWW9pZZ51lRx55pE2ZMiX8W/qNU0891U488UTbaqut3HfUUufee+9NQI4gkr+gUL262mpW15BBAAAA7bRy7UpbuGJhi7pVovjfpxs0AAAAAEiiYI26OVPLl3HjxrV4f8aMGdbY2Nji/S222MJGjBhhb7zxhvtbz9tuu60NHjw4PI1axNTX19vHH38cniZy3prGz0NBHf1WcJrs7Gz3t58mUkNDg/uN4APdp19ePxvaf6h7XVVdRVYDAAC00+za2e65uKDYinv/7wapRAZr5i6ba+uaW3ZfDAAAAACZKOHBmocffth1O3bNNdds9NmiRYssLy/PBgwY0OJ9BWb0mZ8mGKjxn/vPWptGAZbVq1fb119/7bpTizaNn0ckpbeoqCj8GD58eIeWH/GrKK1wz5XVlWQbAABAO82qnZUUrWpEN+Hk5+S7QM28unmJTg4AAAAAZHawZv78+XbOOefYQw89ZAUFBZZKLrroItdNm39oWdC9ykvK3XNVDS1rAAAA2st3OebHi0mk7KzscDpm1awPIgEAAABAJktosEZdjy1ZssR22mkny83NdY9XXnnFbrnlFvdaLVvURdmyZctafG/x4sW26aabutd61t+Rn/vPWpumsLDQevfubQMHDrScnJyo0/h5RMrPz3ffDz7QvQjWAAAAdJwPiowtTnzLGhlTvD5Yw7g1AAAAAJDgYM0BBxxgH374ob333nvhxy677GLHHnts+HWvXr3shRde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Tz9tjz32mJt+wYIFdvjhh4c/b2pqcoGatWvX2uuvv24PPPCAC8RMnjw5PM2cOXPcNPvtt5+99957du6559opp5xi06ZNC0/zyCOP2KRJk+yyyy6zd99917bffnubMGGCLVmypAdzBN1FgZrRxaPd66rqKjIaAACkpFkbuv7K1C7QJDsr28qKy1oErwAAAAAg1SU0WDN16lT7yU9+YltvvbULjijIolYyM2bMcJ/X1dXZH/7wB7vxxhtt//33t5133tnuu+8+F5RRgEeef/55++STT+zBBx+0HXbYwQ4++GC78sorXSsZBXDkrrvusrKyMrvhhhtsyy23tLPOOsuOPPJImzJlSjgt+o1TTz3VTjzxRNtqq63cd9RS5957701Q7qC7ukKrrK4kcwEAQErywYkxxeu7AstUPlg1q4ZxawAAAACkh6Qas0bBGSkpWd//toI2am0zbty48DRbbLGFjRgxwt544w33t5633XZbGzx4cHgatYipr6+3jz/+ODxNcB5+Gj8PBXX0W8FpsrOz3d9+mkgNDQ3uN4IPJLfyknL3XFVDyxoAAJCaaFmz3tji9cEaWtYAAAAASBdJE6xpbm523ZPttddets0227j3Fi1aZHl5eTZgwIAW0yowo8/8NMFAjf/cf9baNAqwrF692r7++mvXnVq0afw8oo23U1RUFH4MHz6803mA7kWwBgAApE3LmpLMblnjl98HrwAAAAAg1SVNsEZj13z00Uf28MMPWyq46KKLXEsg/5g/n8FNkx3doAEAgFTW2NRoXyz7wjJ9zJrg8tOyBgAAAEC6yLUkoDFknnnmGXv11Vdt2LBh4fc33XRT10XZsmXLWrSuWbx4sfvMT/PWW2+1mJ8+95/5Z/9ecJrCwkLr3bu35eTkuEe0afw8IuXn57sHUkd56fpu0GbXzrZ1zessNzspNn8AAIC4fFH3hTWFmqx3bm8b0m9IRueaH7NHLWtCoZBlZWUlOkkAAAAAkLota3RipUDN3//+d3vxxRetrKysxec777yz9erVy1544YXwezNnzrR58+bZnnvu6f7W84cffmhLliwJTzN9+nQXiNlqq63C0wTn4afx81BXa/qt4DTqlk1/+2mQ+oYVDrOC3AIXqPF3pQIAAKSKWTWzwl2AZXpwYuSAkZaTlWOrGlfZohXRuy0GAAAAgFSSneiuzx588EH785//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ay978cUX250H0eYb7TwmuB1qecaOHWtXXHFFl+4P3a217V/7z8EHH+xe+7Jzv/32a9f8u+IcMJiOzmrP+bH2u80339zti/369XPH2V122cVdjP3d7363UfBZ8z399NNbzEPnfHpf+dfW70de6H3llVds//33d3XjPn36WHl5uZ1wwgm2du3amGl+//337bvf/a47Xqkc0W/tvffetmTJEvd55DEw+HjzzTfdNNr//XuqS+g4ufvuu7ttW3X4zuRvsD4f7eHrvHvuuafb7wcOHOjKuoqKCps8ebI7f4rl6KOPtsrKSuuO87a2vP3223baaae167cj6/oqOy+44AJbs2aN9bS2ruW05wal1h6aJlXFc4xuq1xtT/kTa500NjbaKaecYlVVVTGPoV1ZNgd/u2/fvq4cUtpmzJjR6f0vsr4Ra3/srGj7sz9XisyHv//977bHHnu4OkT//v1t6623bpGmzpSPXS0d6iCpjGANWtABUxVWPXRipouW3/72t91nKix00NB73UkFV7TKSzBt/vGXv/ylR9egDpTdXTgFl08Vap1EBt/Txe1koAvlnbmo29q25unAoIpzV8yrPY444gj773//aw888ICrFDz11FPu4F5dXW2pQidzqtzdeuut9tlnn9nUqVPtyCOP3GgZTj31VJdvs2bNsr/97W+21VZb2THHHNPmCYFOxnbeeWd3keK6666zDz/80P2GTrLPPPPMuNOpk1NdBOsIlUmq0Oh3H3roofD7utCkE8/LLrss/N4///lPt5yvvvqqDR061G0fixcvbjE/VZY0jZbtt7/9rf3+97+38847L232XVWyVIb7i19+v9Hy/uMf/3Dr7pxzznF5k2qVMJ14KnDR2e2xK8u4nihnItdpT/nDH/7g9jPtTwsWLLBM0Z59/L777nPPt912W7jM0TrW+vrPf/7j8k0nayqbdDKuYPlf//pX+/zzz90FpNmzZ7vv+4tmOnFXuVRbW2upqq1jtcr03r17h6f705/+5N7XRXzt191dz+xIehNZL24PXbhRGfnHP/7R3cjx7rvvuv1XFz908U4XALrquN6R5WnP9j1z5syNzgd04ThIdQMF/nTxS/tbNNpH9d133nnHBV1UR9Iyt8V/T4F1XejVNuH310i66NVZfjvUhTPVSXQxuiv3h0TS/qML5cmQjuzsnr8sctxxx7kyXzdWvfTSSy7w8stf/tIFDj/++OONptd+ouOvtoXO+uSTT9y2peCQygJt+zpnUL1C9Z9YN5kccMABro49bdo0+/TTT937+nvlypUtpvX17uBD5Yvnj58KrL7++ut28sknu/JJrSg6W6/w9Xn/UFmgoJSv81577bXuQrDqYArSKC+uvvpqV27oxqVYwSodnyLLmp6im+4UUOto+aEyasqUKS4IGDw/6kntvZYTWX76G5SC6zVynpomGa7ndMcxuqfWieo0Oj/XhflY9ZvWArqtfdbWcVXl3u233+5ublKAQvnRmf2vK+pPnT1X8jdnieqSWqc6B3zrrbdcOaSyJ3JbV1mvMtKXj7ou01XlY3ulcx0k6YWADU444YTQ9773vRb58dprrymMH1qyZElozpw57vV///vf8OvgQ9+Xpqam0G9/+9vQmDFjQnl5eaHhw4eHrrrqqvA8P/jgg9B+++0XKigoCJWUlIROPfXU0PLly2Om45vf/GZoiy22CI0dOzZUXFwcGjx4cOiyyy4Lfz5y5MgW6dDfomm233770B//+Ef3XmFhYejoo48O1dfXh7+rtP76178OjRo1yqVnu+22Cz322GPhz1966SU3z+eeey600047hXr16uXea+t79913X6ioqKhFXv7973938/J8+v7whz+4POrbt2/ojDPOCK1bt87ln5azf//+bv5Bd999t8uP/Pz80Oabbx66/fbbw59FrhPlXTBPr7vuutCmm27q8v1nP/tZaO3ateHvrlmzJnTeeeeFhg4dGurTp09ot912c8sauUxPPvlkaMsttwzl5OS47aA7tjW/LL/4xS9C2dnZoQ8//DA8nb7nt7V459UetbW17rsvv/xyzGm++OKL0He/+123zrSOjjrqqNCiRYs2WrfeW2+9FRo3blyotLTUbYf77rtvaMaMGS3mqd/Uuj3ssMNCvXv3dtu78trTdnHSSSe59a68r6ioCN10000xtzm9vv/++1tdVm0f55xzzkbv33vvvS4906dPj/ndgw8+OLTZZpuFVqxYETUPO5pX8WyrkW6++WZXNixYsCD0xBNPuP30vffec58Fy61gGaT3gvkbmQ5R2aQ0dETk+lCZ8atf/crlmcpF/dY//vGP8Oc+nX/7299C3/rWt9w2oHLl9ddfbzHff/3rX2696fMBAwaExo8fH6qpqQnvw2effXZok002cdvJXnvt5ba9yPJM60f5vOOOO7o0Tp061ZUpWke77LJLeFuMZ/3JlVde6X6zX79+oZNPPjn0f//3fxvlZWvllsyfPz90zDHHuPWo8mfnnXcOvfnmm+HP77jjjtDo0aPdutW2r3I9SGnW/qXtMTIvfRmtvNlmm23c/IcNG+bK2+CxJ1YZt3jx4tC3v/1tNx+V+Q8++KA7pkyZMiX83RtuuCGuefu81nQ+ja1tI22VC8F1GvwdHW80rfJb28i8efPC3/n888/dOh00aFB4nbe2rwfnK1oupU/rcffdd3fbocq1ESNGhA4//PDwd5RH119/vVsvDzzwgHuvrKzMHe80L+3bhx56qEuPF7m/+nLPH2sjy732HN8uuOACt26UdtVP7rnnnhZ5+M9//tNtd8rnPffcM/TZZ5+1+B2VLdpnlKdaDv1m5HE+chmGDBkSuuaaa8JljvLnzDPPdNvXd77zHZf/CxcudMcEf1z78Y9/7Ja1vLzcfV/Lrs922GEH9772AdUPfvjDH7r14usVfjmeeeaZ0LbbbuvSqfUTPH7Gs31EW9bLL7881NjYGP68srIytM8++7jPtSzPP/+8+23NN5Z4jtU+77TfRqtnqow47rjj3DanfNC60rOvZ/rl8/VM7cN6+HqmtjUtj7Zd7QP+2Jybm+u2C20fKueUv9r/lN7gsgbrm1pWn8ZHH300tMcee0StF+vYEvm+9r3O1otVnp1//vlR68XRqEzS9vbVV19t9Jl+S+tXx3XNT9uaynO/nakM9GWM0q/6ofJLr5X/Sktw/e2///5uWfRa00XWMyKXR7+j7VzLrnz2yxOsN+tZxxo9v//++y3Kich9WL+t+ajs1PFI+Rl5jPfrQftjc3OzOzfQe6pPtCZyO1d+6r277ror/LmOV9q/Vc779dLaMSzWeYxou9J8gt878MAD3fs69uu8xq+LrKwst18//fTT7rvaH/Tdrbbayn1f00SuC61vPXT8ER1ffNmg/VD1yOAxRv7617+6eep3fTkfpPeuvvrq0Iknnui2I6Uhsk4QLT+jncP4bX3ChAnufMAf630dIjLvNI2vQ1x77bXhckzf0XJqX/f5GFxXeq281PpSmaa/Va/xZcjWW28dro+1dg7Y2vlxpEceecR9rnlHrhdtk1pGlWe+bqCySetYeaoyyXv22WfdfG699dbQ3nvvHV7Xb7/9tivjlBfa9w866CBXVvq6y6677urySuX7wIED3fx/+tOfhhoaGlqsy2Bdx++Tv/zlL2Nuuz4PbrzxxpjHEX/sitxXVNYoLccee2wolsh6T6Ro9flgmaO81fbr6z7BOq/Og3251lpdrj1inWsF5xVPPSa4LrQMWk6tT+2Hqiv4cljbgbYpP1+V11qmO++8072neojW9SWXXOL+1jFO27zfv3Rc9es3mN+al/Yhnz/BaUR1HZWp2j5Vb4s8F/D1mFjnAqr7Ru47yqPWruf4fPP7pOqh2l+1LMoXbfNaPr8MEydOdJ/56zk6n/HXPfy+rGOe37e1DeizyLzQw9cXNY2WqbXrOSpLgsf8jh6jg9uBX/bI8w/VbYL7h8ombU/+GKHX/txDy6ptx5cZKh91vNRv+H1bx1nNS+tVeaJ56H3l8ze+8Q1XZ9Vnft6qn+l1tLI5ss7vxao/Hn/88W5b9ee50fa/ts5Bg/u+XkduYyqv2nOuEUtk2rTOlCadS+h3fJmmssCf38Wqr2sZItPpy0flscpT5bO2P7+Ne3PnznXnrPrcH/91jOioaMvt6yDxXjvs7DlHJiNYg5g7owoZVdq0c+kgGLwAoUJNBb3+njlzprvYsGzZMvc9XRDRwVwVfBXIOhn3lSBdSNNBQRUFFUgvvPCC2ylbu/iuSo4OIjqoqzDSRR8dBHRxQHSS7w/oSoc/6VehpkLS/9arr77qKkAXX3xxeN46cOoAqwtos2bNcvNQQeEv1PuDsg7e+j0tT3V1dZvfizdYo/QdeeSRoY8//jj01FNPuYqFTkhU4VLhrgOHvuMvWuoiofJPeT979mz3rELbX5RXpdyfsCovlFafp6rcnH766aFPP/3UncipUP39738fTs8pp5ziDrrKJy2nKoxaJn8A0DJpPWiaf//73y59K1eu7JZtLXjgVqVDB/d4gzXR5tUeOjhovZx77rnuIBRJ81RlUydE77zzjls3qrD5wFi0EwVt53/6059c3n/yySeuMqHKWzBwqOVVJevPf/5zqKqqKvTzn//cpcOvQ1XYJ0+e7IKGP/nJT9y2oHWok71o25z2lx/84ActfiPeEwgto/ZhVRyjUZq0D6pi3JqO5FU822oknbToosIBBxzgThRUcYt18XfVqlUuCKj3gsGSaCd3Wgfavzoicn3opFXL9Ze//MXtOyontT/5/cunU+WKKm8qV1U2qLLrKyxaBu2TWi8KRn300UfupGzp0qXh9KrCpOCyyhR/YuW3oWjBGqVBFyt1Uq8Aok7YVMHTRbt41p+2Q1VsFeBTmnVBQcsZzMu2yi3ts7qIpYsPOl5o+9d27S+MPP744y6dOqnTb+jERCcJL774ovtcy6fl0glDa3mpvNCJuT7XPql9JLiNxyrjlBdanjfeeMPlgz5XBTl4AUOvlZ625u3z+j//+Y87cdF0vpyJto1oOXTcilUuRAvW6Hd0EUL5p/Sq8qw0e9p2dGFRx0Vtf5deeqlbhwrMxbM964RU25nSoaCGTk5feeUVt93oRM9f2NC2q+OK8sqXQ3pP5ZKWRduzLtLoRMWX1ZH7qy/3lGfadiLLvXjLDP2m0qltScdsHSMffvjhFnmoEyUdw7XvaFsM5pmOi/oNbbP6vuoDuvin/TFScBl+9KMfuXXuyxydAOrEWccoffe0005zZZJe+/1By+Mvvmo71H7uL3JoXekzXVBV3ut4EBms8cETBQB0wqaTT3/BJ57tI9qyah46eRKtK10YUHmrbUnrXmVJe4M10Y7VwWBNsJ6pi//aTrQvavl0gUEn8EqHtiktu+qZfjv19UztgwrMqZ6pbU37ki5Q+bT4Y7MuWuoiiZZDFwq1f+h3lcd+WZVfqo9oXUUGa/Sd73//+64c8MdybXOqF2s5tZ8r3xUIUDmisqKz9WKtI62TaPXiWMd0bW+x+OO60qFjiNa90qo8UL57/kKd6sHKdx9I1vd9fmjfUF5oP9P2pfmqDIu1PKoPqezQBTjlr76r7/hAV7zBGr8Pq4xSGpV25am2lYsuuih8XPLf13FBdIz1685f0IwlcjvXRSS9d8stt4Q/Vz1Ex0TlocrVto5hsc5j9D3lg85Bgt/T/qp9X9u08l77p9Ktckvbks4nxOffFVdc4b6vC7j6vn7HU7p08URUxupvlVc6BulY5C+g+mOMygwdu/w8NS+lIThP7ZM6xmt5Vdb7cioyAB6Zn/4cRsvnz2H8zSk63qi+o8CQ8kTrVGWUzztdrNP617LrN7VvaJ/WNAoIaLm1Xer8yudjcF3ptY4ZyjN9T39rP/zNb37j5q36hK+PtXYO2Nr5cSSVJyob2rqY7+sGRxxxhPtdXcDU/P0FVx+sUT1KafIBNm3vKkt1k8+7777rylrlo6+76CYBTadAsY4zqi9pWYPnyZHBGpUJft9R3TvatuvLAZ//0Y4jPlgTua+I8kLrV3nZHcEa5YW+78skTevLOC2r6rk6zsSqy3VXsKatekxwXageoelVVivfVKf00+rYr31E60Lz1XahY5TKV5WHOg5qH/Y36Shgrfd03FOZ7YOXvp7l81vf0YV8bW86ruo9f8zRtNoHdBOM9nMdZ7UOg+vB3/QQ61xAZYs/fmg+qvfpJrzWruf49er3SV1AVtpU3quupGO7tnsflFM9UPmq6xzKJ+WL1oGWSdugfkN5p0Cv/tb5ur4XeV3Iv6f6ogJEypvWruf4MiZ4E1p7j9GR24Ff9sjzDy2j3z+0nP4GT21TurFE24Mu8IvyTMde3Ryk443KbL2nMjcYrFE91t+AoXmp7NL61e/rmKPrEvqOymBdG9Ax1pcN2r5Uf1LaIuv8Xqz6o347uC1G7n/xnIMG932VxaoXaDtWeaWHypl4zzXaE6xRPUR1bb982mZVZiqoqelaq6+rfqjl0rL4dPpzK60/bW/aFlUH13ambdzX83XNTMEUzVPbsNa76ukdFW25tf51XI/32mFnzjkyHcEatNgZVaCrcuUrqiqAfQuAyIso0SpLuiDj72aLRhUJHYyCd+PrAKlCx9+tHe2kVJW5YNr8XRG6cytWIa+Duwra4MVq3YWoA4noApk+j7xzXQdmXQgILqMivl4834s3WBOZPhW4KqD8QUzz0bKqYBdVQIInvKKTVx14oq0jT3mqg26w4qs75FVxE1X0lL+Rd3PoAoUqPD4tmrdvsdCd21pwnario2lVmMcK1rQ1r/bSXYPaTnWg1AFFeaCKh+ggot8L3hWgNOp3fSuGaCcKQVq/quT4ux/98upCnKd9JDKgEFnpVwVIJ2/RtjkdmHXByB8kFXzSCVuseUXSfhK8QBOkkwKlTRW71nQkr9raVmPRyY3mq0pg8G4Mv0+oEqntw98RpJOx4B1rkelQhUKVeH8xp70i14cubvvyytNJhO6cC6bT3+0fzCstm6h8UWuZaLS9aF0/9NBD4fe0fPpdnXTECtbo7+BdTqqoB++Wb2v9aTvRdhikNAbzsq1y63e/+53bH3wAIpL2QVWsg7RNHHLIIS22R92JFG9e+pNdnRR60co4Vf6Dyxvc1oIXMCLFmncwr1XJ1fboyxmdjPo7Iz2/rcYqF6IFayJPCH16lU+x6CKeLoTFsz0rrTpW6filC5XaT5QO3V2lkz5/x7j2Y1Xmg/uutotgCwAFGpU2fzdZrGNYULDci6fM8OswVuuh4F35nr/4tXr16vCxMDI4rW1S6y9SsMzxQRc9FGxR/ugEVhdW/TakE1i99heqtDwKfAXXWbBepIsRupFDJ5V+3sHl8EEo0T6ldARPdNvaPqItqwIaOq7KtGnT3HIE6wvaHuMJ1rR1rA4Ga0QXIPS3yiQFBfx69PXMr7/+2i2fLkD45dPfvp7py3WdQOq7ftuLVs9UUDp4bNb+648XviWc0qv9JDJYo+/o9/w6UH77eq3qeHqt9d+V9WKlN/J44svASLobU+nSRd9YYh3X/XbmLxT4i8DRyqTWyl4fEIgVrPE3RvjtW8ujAFi0YI1fH/647i8q+X1YQVLN3+/DvpWUnhUA9XeHq+z15xT6W/XvWMchL7idK5ivY7i2a19H1Oeqb7XnGBY53+D3dBEt2CJAF9iVXr8/aBtVGSeR+4PyUvuqp+1Sy6yLcaJ9T/Pwd8hr+1FwMkgXXYPHGOWtLgQF6dxKd+96Wh/+5gm/vlUWRguEBZc7cv/327rSHKxDaNvQhV9fh/DrMrjuguWYz/9gOab8D64rnw6VEcrD4Has5VPATO9pPcd77hgrmOCpnqWLXm1dzPf1x2A9VfuLAmnB45UCS8Hf10PHF0/nktoefN1FrRT9MUoXErVN6bipfcKfh0YGa0Tn5NoGlQZd9PXBGs+vR9VJfXmvh8ptn//+WBS5r4g/Pqrc6miwRukL/raWW/u36BgZrGdombUuPN0Uo20gVl2uu4I1bZ37BNeFAo66aB6t1wGVE0qz0u5bEgTrIsoblVkqv2Jd01AdxNc9fX5rv/P8NufLde2L/nzG0/lB8Fih42TkevE9sAS3G5X/8V7P0fLpIre/sK7vq4z3+6SCL1qXPnCtOrbyXAEUnSNru/DT+7xQQCF4PUdpjNy3g9dzVCZG9uYReT1HFPjz13M6coyOFqwJ1qn8w7eS0f6hPNB+GrzwrZvitB50bNR+HzyW6qG06z1/XFUgRBfT9VD++G1O53YK9OpmGgU69LuRPZpEHtci6/yxpvOURn2mFkrR9r94zkGj1Z9iXfto61yjPcEaHXd86xwtg/JP24/qTEq33vNBVAV2FJj09XVfl40saxQE8dufLx8jj/u6DtKVgY7IVom+Dq4AXbzXDjtzzpHpGLMGLahfavWXq4f6UdRgxxpwMXKQ91jUd21DQ4PrzzbW59tvv70bPMxTP9EaF0B9UMeigbWCaVO//hrcMHKQxWgDKWrgLm/IkCHhARDVR7AGEVTftOqX0z/UH6TG7whSf75ee77Xlsj0acBDjRkS7DdZYxEozeoLWPNXn77B373qqqvi+l3136v+1aPlhfopVv/E6rc3OG8NPBmct/ox3m677awntzXlx/HHH28XXnhhp+cVL/Ujqv5ANb6A+unUYH077bST68tY27AG3NUjmEb1h+r7bo6ksVE0NowGzFPfqeqDVH2xRg4iHcxb7SOazq8jUR+u6ttU/Q1r/WhMlch5ePvuu6/rn1h9o6ofdvUBu88++9iVV14ZVx6obhFrHIzIQQ5j6UhetbWtxnLvvfe6vpznzJnj+neN9Mgjj7i+qTUuj/rg1brUYJtB2g+Ur+oTd7fddnODj2q8ic5Sn/nanlTWBenvyHwIbgNabvHLru07Vtmq/VT93QZ/Q8un5Wgtr5Vn6is9+Jsqw7Xu41l/Krf1G0HBv+Mpt7RcGihafZ5Ho99qLe9ibY/R8vLYY491Y4Oo3FVf8RofJjiYbGQZp99Qf83BftY18Gdk/8fqm13rprV5R+b1IYcc4tKuckZlmMoE7eORA4kHB4KNVi5EUno15klken1+6Xc0tsqWW27p3tf60GexypIgrW+Vsdtuu607funYrL6X1S+zll37jh8/Ssd1DQiuPPe0bWkf1ODlWg7NQ1r7beWJ8l/9tccq91orM7R96bNvfvObrS5ba/ueBlTWgJrBbVj9a2v9xRqMWGXOs88+614rb3QM0DFWy6GyxffrreOL8mPEiBHh7wZfB/sz10DvKtdV3qmMj8bPW7RPafDqYBnQ1vYRbVn92GZaVl8uaByeaL/ZmniP1a+99pr7XX0u3//+990gp0q79gFfz9R4Z5HLp+0uWM/UtuL759eYBdGOzUqLHsFjs/ZX7cvDhg1zeeLTq7yJpPUarNeqn3Vfr1Xa9Fpjm3RlvTiyLtbacTKeY7afRuWytjNtg1p+v98E9zmlWf2mqx995U1kmaR0+33WHw/aKl9UNxKNW6NxvLT+Y/XR/+ijj7rnhx9+2G1LGtPI54n2E43Xd9RRR7n3lK4f//jH7vivNKju7sdC1PgN+r7GbNOx7Z577ol5HAr64Q9/6NKn/FF5pvIvuD6C5ww+v+I5/kfS5+qf/5lnnnG/pz7s//Wvf7ltU/uDzhW0fWr7k8j9QfWOYLmowah1jFO/86rz61ijefpl1noLlg0SeXyPtSx+nrG2T/1OW/W4aDRPHQODdQiN5aDxgoLnJypDg+suWI6pv3+dowXLMb8MketKlKfBZdC+5bdFbUdddQ4Yb106Wv1R58B6//nnn29RlkfSsTp4jhkch0/bj+arOrPGcNFxSuNVqd4WObB3kPJD4xbcdddd7tgrZ511VtTxnvR7/qHl9fnvRct/ny+dGYtP+4E/1uihMi0yf/zvBM93VJdT+bF69eqYdbnu0p5zH5VvSqO2e23XGrDcj8GiZVH9QHUL1TH095tvvumWR2WA6ts6Rqkc8dc0VM5re/ADiascjRwXQ8fvYNpEY/34ckHzDArWC7RNLV++fKNtQrQcQTpHa8/1HM1by3DCCSe4v8ePHx/eJ7Vta1vwdYyysjL3ezof1rUk5ZmfXvVZzefpp5929Te999Of/tTlYWv7tqaLXI5o13P0XmeO0dFonaiOrP1cdYjgfLQsKgd1DqoxRrRtqfxX2aW81/myH/9Fx3sd11S3VN02eI6jMTVVL9J8VBYrn7TM+r7qgtq/dK6s7UnlY6QbbrihXXX+9pQFbZ2Dtkc85xrx8udKylNPZa3qClpPvs6iczH9lspTXW/SdaLW6gX6zG9TPk8ij/s///nP3Tm2fk913w8++MA6K1gHUZ1d5326thTPtcPOnnNkuu4dERMpRwVI8CCpExedQN199912yimntPl9XajpDiqYgmnTAVs7c1snVZEXY1Ww+cqBDjyiiymqoAZFDnYZPImO53tKb+SBN9ogo9HSF/meKM3+d7UuIitEwcpdR/NC81DlPHJevhLi129XDWTd2ramg0zQr371K3cweOKJJzo9r3jpgKQKjR4a7FPbvw567Rlw3lMFUpX9m2++2UaOHOm2E1ViIwfga20d6aKEDuo6kKuyc+ONN7rB3fzAuapY+4sdwfmpQqrH//3f/7m80AFRr1Vhi0UHX514R560e0qD0vbZZ59Zd2gtH6LRibguuuikVcuok3qdcAW3VVUolW49VDnXxT9dSA7u66rs6MK5Kha6ENlaHnWX4LL79Ptl747yNVpe+xOarhBPudXZ5dI6la+++irmss2fP98964RBFXIdO3TRS9uK9kM/aGtHyjgNVqsBps844ww3SGSsecfKa5Uxyht9V5V1lTO6EBc5Xbz7Q1tUjkyfPt2uv/56V25qmVXpjmdAUJ1oaP/RyZeOcdpX9Kz9SCemWlYFiHVCqpM6LbOWyVOgQfuitgftY1qObbbZJuZv+3JPv6cyU8f+YLkXT5kR7/bV2r6n7VjHocMPPzw8jS7Sap3pWBGNllMXtHXhb++997ZLLrnEDYYrOrFWPUEnNToBjgwiqL6gNPjjmv5+44033Hr661//apdeemn4va4WbVm9WMsar3iP1bqA9+CDD7o6yTHHHGN33nmnG2i3I+WFTrx1QUL7ZOQA2P7YrCCq1pX2veCxWetI24VPs09ve3RXvbg9x0nlgU6OWztm++O68kAX9BR01fd0sUJBquA+qosYonJEQTOVAcHfvuWWW1wdRXmpz3QBJFodODL9oouM+j1dkFdAORp/A4EuMGnd+Bs0lCd//vOfXdnjL9ypzPfpU91JDz+gtQaV1/f10AUqBdB18bGtAYxV3xg3bpzbFpRHkYLnDF1BF+S0D6hOov1fF8Y6UhfX93WBUhcjtT6VV12dVi/WuUx7+QBQsA6hY62OBTouxFOOaftT+evLtGA5Fm35/YDafhmC+5YvQ+I5d2yLzmu0T6ruGS0wqXq9LnBG+0z7s46hupHN34Tl06vvxDquaTkiyzAth4ISeuginPZBlb86B4h1PqtjvQIGemg9qN6jOoUCrd7PfvYzF8SJ1Fb+6yKelkEXITtK23rwWKP5+XXog5v6HQUu9Kw6r6/L6aK6vqt1HK0u116x1mHkeVt7ynSVgbogrHMdlcPKa9WNVKfQfLSfq5zWsmhb0XKqnqH6ps4B/c0evo6umwlUr9A5qtaP1psGuw+KvJG0PUEG/ztKh+p1QZHXHaLVM1rLGx+k0rm6AvHBaxnaJxXY9PS3Hiq/X3rppRb7soIO2p617evYooCQgmA6b1a5G0tkfdG/19XH6Fi/rYCSykQdl7Qfqp6ibUH7qfJdn2m5tLzanvWsvFK9R/uY5qFtQnV3HTfPPPPMFr+hC+bKC9WVtF8oTzyl+dZbb7WTTjrJzVd1XOVtML+Uhnjr/JH8Bf2uOieNJd5zjbb2cx0ftIz+XCl4U9O0adPcthe8CVTBHG1rOj6pXApO3xqlL1b5qOtVqkNpu9Z1kWuuucYt19lnn21dUQdRGnWMVEAznmuHiTznSAe0rEGrVIDr4Bx514P4C5nBO6l0sqcTUxX40ejESxHU4Amz7o7Sb6iy2lE6IAbTEQ9dWFKhqRNRf7LmH8E7yTvyPR10dQdJcDlVCegMVbhUQOpiV+Tv+oNYtHUSD1We9B1dYIuct05mE72tKV9Vcbz44ovjWrbW5tVRWu9an9qGdeHXX/wVndyr0q1potE2rjsddCFAd05p+/n666/b9fuahyrOOgDrDiGtm+CdC7qw4U9AWlsGVR6Cd+pHo5Ot2tpa18IoGlUGlQ5d9I68+CXKC+lIXrWXKpG6sK3KqCoTqiDpbhbd8ReLLniqonHHHXdEPbnTxZyuDNSoAqd9V+swSH+3Jx90l2esslWVbqU5+BuqqL/99tvt+g1/B47WfTzrT+W2fiMo+Hc85ZaWS+VjTU1N1DQpHa3lnQ/a6+7oWNujL3+1neyxxx5uX4m8azAa3QGkfSZ4l6lOkP02LvpMlXNVhtsz72jbiE58I5ehteNRNErvO++8s1F6/YVP5Z32GQUsFTRQGa+LFG1R2nSnopZTrVq1nMpXHdOVdpVBqlgrvarE62RM69mfsOo39J6Cx7rAq/SonImn3NOFCB2nIsu9eGgZtX50EaOj1LJS+RjcfrVt6zgTvIARjcolneSq3PVlr76j+pIusqi8Ct6xqmOc7lhUGeu3bQV0lHe6G0/5p5M93SkbTfB95a/uigxe9G5r+4i2rP6hdPtyQXe9RfvN9oh1rFY9MlinUp7od5V2LZOvZypfldZgGaf5BeuZmnbixInutS5Q+Lt7g8dmnfTqEXls1rYbXFalN9rFKeWxfs8fNxRE8/VarWedyMa6o7a76sVBmpeCXgrARCubdLKsMkgXKXRM1QUvbWcq/3y6g/mmC4y6qKOLWjfddJNr6RSklkJ+n1WwpL20nS9atMiWLl3a7u+qDqCbavwFQV2wUP7qgojyWHeI+gsAwe1Od+Pqor4CsG3xQZ5ogZqOHMNincfoe8p/H+TUMmhf0/f0mco1Baq0/Unk/qByOXKeuiirbVgttLU/BS9Aa3sLlg0SeXyPtSw6HsRz41hr/P4T3Mf0npY/WIfwLUx9HUK/qzIzWIcIlmO6OKgWBMFyLHIZ4qX6YVvngPGei/3oRz9y607p1/EzSHmgda11Eqv+qBYB+r6Cb0Eqc6Idl/y+HDxX0L4R3A9Ux9N3fcBK23iwrNexSHkdpG1Xx8PIuouO+bGOI7EojQoiKmDc1rG1oxSYV9mmi9sKdqhFkOq8qstpnWnd6oJnR+py0WgdRq7feM/bWqNjm1oMKTiuVjQ67vjWTWopo3WpdeBbdSqAo5ZTOjfQtqX1rrJCxzWV/SqzDz30UBcU1ToPtmSRyLJBfEBM5ULkhe1gvUDbh9KrbSTWuYDX3msYSqf2SV+G+qCCHirfVA74Fh2i7epPf/qTK/O17NoHNK3qXJqPylUd/3zZoTTH0+Kyu4/RPigVpLpb5PmHlj9YDmo70PLouK6L9wpK6OZXlVM6lqus0XL647nOn4PnOFq3Oh4rf5U2BfR8/mrbUlms7/u6v25kUlns06GL8PHW+SMpPZq/AkDRtHUOGo2WO3Ib64pzDaXF16/9uZLOkXSsFeW9ynJ/s0hwH9H2qf1D+Rysr0emUzeSaH2r1YwvH6PVg7UudJ6mVoKqDylY1hnBOog/NsR77bCz5xyZjpY1aEEnXCooRAWqLgjoAKHKQCQV1jrI6cRHF6FVyCiSqui8ukZQYajCRCdb6oJJd6aoOxTdtaeTPDXJ1GeK9OpuHh3I402bLniokqGTah0oVMjpxF2/pwOtmmjGc3DXAUsn8Sr4dOer7nxRga0Dg78rryPf882LFVzQhQBVYCK7tukIRZ41Px1cdbey8kQFoNbVpEmTXCGu9TB16lR3N69OSOO5C1QHd60bdTemg4sKYK0b5akupKrylshtTS666CJ3sNFJgu786sy8WqODnu5A0V0iWnatb+Wxugj43ve+5yoMuvin/FIlQgchHdxVMY7WnN+fOKliqM91onP++ee3+25bzUMHf+0ruotFlUxVwLSedQerDv7BEzZVynXHhn5TF6E0rbZHXRQM3nWnCzPKOy2HTvp1x4xOYHzwIxYFarS/KR2660h5pXno4qPuvtDdMB3Jq/bSdqGKpm9SrLJAd/dpH1VT3WhUbmk/UhmkO5I6erdce2idq+zzd3DrLl5V4nyXUfEuq/JTeahKmMpY3cmk7VXloNaZfkcnFapQaZvV+lXZG43Wh8owtUhRd0AqN3QHjqgsUCWprfWn8lvNlfW3KrqqqCvgE7xA11a5pe3017/+tTs51+/rDi41pVelVieQWibdraVySduUtnNVQHWSHaRl0fbo7+TUxR3dja/t0d8Jru9pG1F53VpAL1j5Vpq1nWg+qqSee+65LfZfVSh18qv9UmVOPPNWOaMLx6L8UjmjOx61jyt/VXHVNiK607M9dEKl9aITeKVX+aGTON81gMoS5YPSqn1B6Yjnjmd/oVzbk8oI5YFO0EQXOlQGaZvRBSgtvy7u6kK3urTS3Xd+eXWBQhfOdEGkte4tfVqVJ7ojTSf0Kkd1Itaeu+y0vnVcVpmuPNGFZAW8dYLhW7q0RSe5Wg/arxTs1XLquN5W4FtUjupORQVbnnvuObdPqszRPqF1s2H8SJdXOr7phE7rQ2Vs8ERJv6ltTPu+ptM2o+NJJJXHKvNVp9LdeiobtG/Fu31EW1ZdzFBLRLV+0T6oOoPyVHceKg36nXi091gdWc9UXUTp1UUNlR1aBtV7dGKoi/S+mw/VfZQ+fab5qwzRdqltTscFzTd4bNbFGKVLZV1w31ZeqSzT72m/17YYrVsG1Tv1eyqD/fFF5bLWm9KifVoX09TFl+5uVj5oH+9svbg9FIRQGnwrPpXZWj7tnyp3tV+pnNd2oGO7tiOte39sVfpUpoq2fe37Wg6tm8iL9Kpv+H22IxcJdNxR3SZWdyA+oKZnrTd/kV4XKlW+6Ljq902V4SoDlF7tW1pXCuBo/9Eyatvzd4FqHSuIrXOYyFYTnRHPMSzaeYy+pwtd2ibV2jn4PW27qpOqzqVjlNKsAJW+54NRuvioi0FqeaF6sy7mqpzWMUvnaioTdZODp+Oc6pP6TNum6ij+3MXfPa4LP2pxEZyn9uPIm18i6aKO1lXwxrXIO4O1v/rApuokfjlUPmkb9XUIlTla90qrygFtZ9pvVEZoX9I6136m76gcUzqVbqVBeavlVz52hMruts4BY50fR9I2oTq3LpwqbSpndCOFLrDrXEzlvOahu+21XKojaJ/TcdPXH7WfqK4XpG1bv6vv6pijepSOL6oHKX99iwmVQcpLTat1rt/Tsul45FsjKB+1DWg/0XH8tNNOc/UdBYn00LRaLwp0qN4YvBir7VXz83UNHzzwZYpoegUGdPFO25LqgppfcJpYtL8HAwr6DR3ffX3FH2tE1wy0rHpPea39Rdu7jgdahzpnUmsAfU/7opZfx4Z46olt0XFB+4iOCwoC+TIo8rytPbROtBz+eoMutGs788c2nZOpLNA61f4jWkatD9G+pTqG/tbx/Mknn3TloS6cantS+em7OPNU7usz1SdU15cTTzzRPZ9zzjlu29VxRWWYtk1d+wmeC+jcR/NQPUL1ItWJfDddvmtK0Q0sWk/xXs/RcUzLoeOryljtg9pHVGZq+1dZHtmNoPYDdaepY43KEFH9Qsdj1bF07qB5KJ80fx0XdA4Qed7RleI5Rkd2waw6RuT5h3qI8LRf6yYEbc/a3jWtgik+IK5juvY3rTu1rNJ2pP0oWA9SelSGaN1pnel3VL/ReZy+r6CxymOVTY899pirj/l0qg6heeq4p3K9tZshVAZovWs+KlsU5FDZqHpX5HJ78ZyDRtL+rWVRWeR76emKcw3djKu80PFGdRIFqHRdRfVkvae/da6kY6eCZ6LzIk2r82/VQ5V32r8UsNZ6UP1V26nvjlfHBe3vyne1klL5p+1U27jqA74eo3JN+7XKV10niNVKuTPivXbY2XOOjJfoQXOQPPwgdP6hgeA0mJwGW4818O8VV1zhBifTAJd+0HcNpnbVVVe5gck02NiIESNaDBz1wQcfuAHJNBikBj3ToI9+4NJYA4Fp4L9g2vxDg7XJU089FRo7dqwbKE6/G2uQdw3I5j/3A2Vp8C/NR2ndZJNN3MBqGpy9tUEM2/qeaKA0pUmDfmnwOw0iGxyQLlr6IpddA3Np8K7gQGgaQFwD1WrAOw2SqsFGgwPCatBdDdanweOUd9HmK5qn/1w0YJwGiNOAeFomDeylwV21vjo6qGJHt7VYg81pO9L7fluLd17toQEGL7zwQjcwtpZXg+lpPV966aWhVatWuWk0ELQGBdVAfPo9DQLpBwKOtm7ffffd0C677OK2eQ0Wq0EfIwftjLa8+n0/aKfSpcHc9J4GItfAiEqb1rMGqouWVxrwUfuYfnf06NFu0EwNROdp/ft80/akda5tNXKA4Vg0GJ4G4NOy6Psa7FT5ov3Ga29exbOtei+//LLbPzRYYiQNeqlBD2fPnr1RuSUaWFP7jx+0MNr+2BmR+4vKRQ34pzzS/qXf8oPExypfVe7ovWB+apk1aKEG99MAoCp3fPmkgRg1eKYGLNTnGmTxrbfeCn83WJ4F9xuVmyrDxo0bFzrrrLNalFNtrT9/HNBvarvUwKDazjSwcVBb5dbcuXPdQI5+AEvtL37wQbnjjjvcNqy806CqfhB7T2nWAI3aHpXH+luD4Prt0eelBl1Vmax80zyC5XusMm7hwoWhQw891OWpjmf6XuT+q0FBtf/EO2/tzxr4VNMEyxnliwYT9ttIW+VC5DHK/87f/vY3l19Ks9arH7zeb2s6BiutOlbcdtttbQ64qflqO/EDYkfuL35wcuXBJ5984l4rr37wgx+4darfuf/++12a/PapAZu1PUcbYNrvB8FyT9v7GWec4crn9pYZ2jcmTpzo0qdtUMdmDZoaLQ9Fv6/3lB5v6tSpbt9TvmmZysrKwoMQB0Uug/9b6zdY5mib1/taLuWP1rkGWtegrcHB2P0yarBfHZ+VdyrbdawPDnTrl+Ppp58Obb311m45d9ttt/DA5/FuH9GWVfNRHcbTgOYa4F6/of1R08caILY9x+poA4wH65nHHHOMGxRby6D80rFN26WvZ/rl8/VMHR/08PVMPbRcymft0/7YrOOo1kPw2Kx1ElnnVH6pLuCX1adXA7v6eq3yTI9gvVhlptar3tP0+v3O1osj91d9HqwbRbNs2TK3/6geonWndGj9a1lUr5Xbb7/drRs/eL3KTL3W9iZ6rfqHllFp1e9qeuW9zw+Vu36f1TFB72n5Yy2P0qHtMUiD2Gu9+O1bz1deeWXUcwH/UL75ge4j9+HzzjvP/f3kk0+G5+fLXA34K8qDLbbYwpUzsbS1ncf6vK1jWLTzGNGxVMeHaN+rqalxZawfPFz5pXX7zDPPuM+1TvRd5Yk/H7vuuuvcsVLTq34QeSxT/igd2ta1H/rB3lWGetpnI+cZFDnPyH3fPzT4dWR+qWzTtuXPYfy2HqxD+LLS1yGUdyobtb3q4esQN998c7gc076lZVJ54PMx+Nv+tY5t/pzTl+HB8kDlbDzngNHOj6NR3VB5rN/UMmt6pVF5+PDDD7eoP/r9Mlh/rKurc/uh3teg7960adPce1pWLb+OV8pLzcNTfV/7svZTv06UZh0fPM1fA2D74/i1117rfs/XpfRdbXOqb/lt15cD0R6nnHJKeNv072mZVV7oOKN802+2JjjIe/ChfBM/mHysh6/zat/ScVXHZa1HlVEqd5QH7a0ntkX7muat39X3I8/b4qnHBPcrfVfz0HpR/VzL8s9//rPF9zU/5a2OdX470rJqWg10r7So7NN5kvZ5f3xSXV7THXnkkS3yW8cOnQNo//LHhWAd6eqrrw6fC2h5Lrjggo3qatHWh+rs4rcbbWfxXs/x+eb3SW2Lfj/Ss+oYGpTdL4OOb8H1p2sfqov6ckV5omOAr5Ppb5U7SqO2CZVPwXqX/PSnP90oL6Ktz3gGto/nGO23A/8bkecfGtxd6VEdU7TO9JlPt9btJZdc4j7bcccd3fbjj7Wa7oYbbnC/oYcvB+vr613ZoWl9Oat1pHLXHws0Dw0Wr3qVp/1Zn2k+eo6s83vB7UFltfZFLd+MGTNaTBdt/2vrHDRyXaj+qs99nmi9dfRcI5LKCeWJ9hHNX+tR+4Gvz/lzJX9+pzxUuaX81DHA19eD5aN/6NxQy6r16uvBfp1rG/d0Hq/80/FO26+mDV77aa/Wljvea4edPefIZFn6L+MjVgAAoEvo7k/dHaQ7kwD0DN2RqbtVdSddrLsQdTeu7roLdnEBILPozl7dAR3PwMO6E1qtC4LdoSI96G56HQtijQcKBFsjqO6gB/D/7d1riJVVFwfwZdnNLmoWmtJFKc3SyAIps5AKKzCywlBK0A8pqYVQWEJJWnS/WEYQJVgGRVAJ4qVUEiujMi1KwiIRFczS6ENpeJuXtWEGj868TY75TPr7wWHmuZx99n4+efzPWrs1+y98B23Ov9cPB75ztJw2aADAAcmWQPkfOdluJdsKZFuH+g1PAYDWIVuqZOuXbMnUVHuRbGeWbc6yRVm21MkWLo1tEg8AVfIdlMOdsAYAOCDZUzd7Qudf32aP6+wVn/2Qm9oMEgA49DJ0yT+oyJ74uV9NY3Kfhwxyso9+9pDPvV5yvzwAaE18B+Vwpw0aAAAAAABAhY6q8sMBAAAAAACOdMIaAAAAAACACglrAAAAAAAAKiSsAQAAAAAAqJCwBgAAAAAAoELCGgAAgINs27Ztceutt8Ypp5wSbdq0id9///2gjn/OOefE9OnTD+qYAABAdYQ1AABAZUaNGlXCjCeeeKLm/Jw5c8r5/6rXX389Pv7441i+fHls2rQp2rdvX3N90KBBZX1NvfI6AABw5Ghb9QQAAIAj2/HHHx9PPvlkjB07Njp27BiHg59++il69+4dffr0afT6e++9Fzt27Ci/b9iwIfr37x+LFy+OCy+8sJw79thjD+l8AQCAaqmsAQAAKnXttddGly5d4vHHH2/ynq1bt8aIESOiW7du0a5du+jbt2+89dZbNfdkNcrdd98dEydOLKFP586d49VXX40///wzRo8eHSeffHKce+65sWDBgpr3fffdd3HDDTfESSedVN4zcuTI2LJly/+d87vvvluCleOOO660JHv22Wdr5pHHy5Yta7JK5tRTTy1rztfpp59eznXq1Knh3EcffdTk+I157bXXokOHDrFkyZJmrSnndM8998SkSZMa5vLwww83XK+rqyvHZ511VplD165dy/0AAMC/Q1gDAABU6uijj47HHnssZsyYERs3bmz0nr/++isuvfTSmDdvXgkixowZUwKIL774Yr/2Y6eddlo5n8HNXXfdFcOGDYsBAwbEypUrY/DgweV9uadMyr1krr766ujXr1+sWLEiFi5cGJs3b47bbrutyfl+9dVX5frw4cPj22+/LaHGQw89FLNmzWqomrnzzjvj8ssvLy3Q8vif+Lvx9/XUU0/FAw88EB9++GFcc801zV5TPqsTTzwxPv/88zLGtGnTYtGiRQ1h1PPPPx+vvPJK/Pjjj6UtXQZkAADAv6NNXf7JFAAAQEV71mS4kGFAhhsXXHBBzJw5sxzffPPNpcKjKUOGDInzzz8/nnnmmYZqkd27d5e9YlL+nnvF3HLLLfHGG2+Ucz///HOcccYZ8dlnn8Vll10Wjz76aLn/gw8+aBg3A6Mzzzwz1qxZEz179tzvc2+//fb49ddfSzhSLytUMkhavXp1Oc7qnq+//jqWLl36t89g3bp10b1791i1alVcfPHFzRo/q23yMzIMmj17dglZ6luoNWdN+z6rlK3YMuTJ/YOee+65EtRkMHbMMcf87RoAAICWUVkDAAC0CrlvTVZ7fP/99/tdy2DhkUceKdUd2bYr23tlGLF+/fqa+y666KKaip1sLbZ3RUi2BEu//PJL+fnNN9+UlmM5Xv0rA6D6fWcak/O74ooras7lcVag5DxbqrnjZ2u0bPP2ySefNAQ1/2RNez+rlCFW/XPJaqTt27dHjx49SpXQ+++/H7t27Wrx2gAAgMYJawAAgFbhqquuiuuuuy4mT56837Wnn346Xnjhhbj//vtLEJFVK3nvjh07au7btwok94zZ+1wepz179pSff/zxR9x4441lvL1fGYzkfFqzK6+8soQ377zzTs355q6psWdV/1zqq3BefvnlOOGEE2LcuHHlvTt37jxEqwMAgCNL26onAAAAUC9bcGUrsF69etU8lE8//TRuuummuOOOO8pxhgo//PBDaZvWEpdccknZnyXbirVt27yvR7179y7z2Xd+2V4sq3laqrnjZ9uyCRMmxPXXX1/mft999x3wmhqTIU2GPvkaP358qc7JPXRyfAAA4OBSWQMAALQa2bIs92x58cUXa86fd955ZV+W5cuXlzZhY8eOjc2bN7f48zKE+O2332LEiBHx5ZdfljZh2V5t9OjRTbY0u/fee2PJkiWlLVsGRtm67aWXXmoIS1rqn4w/YMCAmD9/fkydOjWmT59+wGva16xZs8reQblnzdq1a+PNN98s4c3ZZ599UNYIAADUEtYAAACtyrRp0xracdV78MEHS0VHtj4bNGhQdOnSJYYOHdriz+ratWupWskQY/DgwSUsmjhxYnTo0CGOOqrxr0s5j2w99vbbb0efPn1iypQpZc6jRo1q8XwOZPyBAwfGvHnzyjOaMWPGAa1pX3lv7oeTe+Xk3jaLFy+OuXPnlj2AAACAg69NXV1d3b8wLgAAAAAAAM2gsgYAAAAAAKBCwhoAAAAAAIAKCWsAAAAAAAAqJKwBAAAAAACokLAGAAAAAACgQsIaAAAAAACACglrAAAAAAAAKiSsAQAAAAAAqJCwBgAAAAAAoELCGgAAAAAAgAoJawAAAAAAAKI6/wPxfCppaI21zAAAAABJRU5ErkJggg==",
      "text/plain": [
       "<Figure size 2000x500 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "#creating a line chart using the top30 data\n",
    "plt.figure(figsize=(20,5))\n",
    "plt.plot(just30['name'], just30['price'],color='green')\n",
    "plt.title('Price of Tokens')\n",
    "plt.xlabel('Name of Tokens')\n",
    "plt.ylabel('Price_USD')\n",
    "plt.savefig('line_chart.png')"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "557aa319-9738-43d7-b4c9-04dbc572e139",
   "metadata": {},
   "source": [
    "### Step 3 Bar chart"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "id": "d1fa3d57-6850-4c22-a208-7445eae29fff",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAABpMAAAHWCAYAAACbsnE9AAAAOnRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjEwLjgsIGh0dHBzOi8vbWF0cGxvdGxpYi5vcmcvwVt1zgAAAAlwSFlzAAAPYQAAD2EBqD+naQABAABJREFUeJzs3Xd0VGX3//0dOgLSq/Tei4AU6b1IlybSEVEQAUFB6VVFEKXjTS+CSBEBQXpR6aCA0nsHBek9z9r798x8J8lMMgnBzMD7tdZZZOacuc41h/xx33zcewcEBgYGCgAAAAAAAAAAAOBGNHdvAgAAAAAAAAAAAIRJAAAAAAAAAAAACBWVSQAAAAAAAAAAAPCIMAkAAAAAAAAAAAAeESYBAAAAAAAAAADAI8IkAAAAAAAAAAAAeESYBAAAAAAAAAAAAI8IkwAAAAAAAAAAAOARYRIAAAAAAAAAAAA8IkwCAAAAAA9OnDghAQEB8sUXX/CMwjBz5kzJmTOnxIwZUxIlSvRUnxd/LwAAAMB/izAJAAAAgE+bNm2aBTp6bN68OcT5wMBASZcunZ1/7bXXxJfNmTNHRo0a5fH89evXZcCAAVKgQAGJHz++xI0bV/LmzSsfffSRnDt3TnzVgQMHpFWrVpIlSxb55ptvZNKkSR4DIG8OvRYAAACA74gR1RsAAAAAAG/EiRPHwphSpUoFeX/Dhg1y5swZiR07ts8/SN3/vn37pEuXLiHOHTt2TCpVqiSnTp2Shg0bSvv27SVWrFjyxx9/yOTJk2XRokVy6NAh8UXr16+Xx48fy1dffSVZs2Z1e03y5MmtesnViBEj7O/uyy+/DHEtAAAAAN9BmAQAAADAL9SoUUPmz58vX3/9tcSIESNIQFO4cGG5cuVKpN1Lg5H79+/Lf+Xhw4dSv359uXjxogUzwQOzIUOGyGeffSa+6tKlS/ZnaO3t4sWLJ2+++WaQ9+bOnStXr14N8T4AAAAA30KbOwAAAAB+oWnTpvL333/LqlWrnO9p4PP999/LG2+84fYzOuuoZMmSkjRpUmsZp6GTXh+ctlbr1KmTzJ49W/LkyWNVTitWrHC7prbVc1QNLVy40Pn+rFmzbH29T5IkSaRJkyZy+vRp5/ly5crJsmXL5OTJk852bhkzZrRzCxYskN9//10++eSTEEGSevHFFy1Qcti0aZNVL6VPn972qm3+unbtKnfu3AnyOW09p+3ytOqpatWqFuikSZNGBg4caN/DG+PGjXM+E/1sx44d5dq1a87z+h369evnrCjS79W/f395kmCqbdu2kjJlSqtG05Z/06dPD/NzEf17cfzdaDvBP//8U8qXLy8vvPCCvPTSS/L555+HuM/o0aPteeg1iRMnliJFiligCQAAADzLCJMAAAAA+AUNLUqUKCHffvut872ffvpJ/v33XwsI3NG2a4UKFbLwZOjQoVbRpCGMhjrBrV271gKZxo0b2+ccQY+rR48eWUAzY8YMazun1URKg54WLVpItmzZZOTIkdbGbs2aNVKmTBln8KJBUcGCBSVZsmTW7k0Px/ykJUuW2J/Nmzf36llohdbt27flnXfesXBDgyL9U/fgbs/VqlWzcEbDEQ1WNPxxBECh0VBIwyMNkbQlXYMGDWTixIlSpUoVefDggV2j36FevXr28/jx4+17OZ5LeGkYpsGOrtGsWTMZPny4JEyY0J65/p148iR/Lw5aIaXPScMr/a45c+a0WVX6O+ag86A6d+4suXPntu+t863073Tr1q0R+r4AAACA3wgEAAAAAB82depULaEJ3L59e+CYMWMCEyRIEHj79m0717Bhw8Dy5cvbzxkyZAisWbNmkM86rnO4f/9+YN68eQMrVKgQ5H1dP1q0aIH79+8P8v7x48ft3PDhwwMfPHgQ2Lhx48C4ceMGrly50nnNiRMnAqNHjx44ZMiQIJ/du3dvYIwYMYK8r/vTfQZXqFChwIQJE3r9TIJ/LzVs2LDAgICAwJMnTzrfa9mype3/vffec773+PFj20esWLECL1++7PEely5dsmuqVKkS+OjRI+f7+nega06ZMsX5Xr9+/ey90NZzJ/jzGDVqlK0za9asIH9nJUqUCIwfP37g9evXn8rfS9myZW29GTNmON+7d+9eYKpUqQIbNGjgfK9OnTqBefLkCdd3BAAAAJ4FVCYBAAAA8BuNGjWy6pWlS5fKjRs37E9PLe6UtjZzrTzRKqbSpUvLrl27QlxbtmxZqzhxR9vpaUWT3m/58uVWmeOgLdV0xpLuTec2OY5UqVJZRcy6devC/F7Xr1+XBAkSePEEQn6vW7du2f20nZ/mYrt37w5xvbbwC97ST7/T6tWrPd5Dz+k1Ws0TLdr//V/Ht956y9ruuavuelL6bPW5aUtDh5gxY1o10M2bN2XDhg1P7e9F2wG6zm7SdnmvvPKKtQh00JlQZ86cke3bt0f6dwcAAAB82f9NrQUAAAAAH6czeSpVqmQzarTNm7Y3e/311z1eryHD4MGDZc+ePXLv3r0ggUpwmTJl8rjOsGHDLMzQlmfahs3V4cOHLcTRgMIdDUPCouGMa2gRllOnTknfvn2tPZ6GZK40MHOlQVDmzJmDvJc9e3b788SJEx7vobOdVI4cOYK8ryGLruc4H5l0TX2OruGVypUrV5A9PY2/l7Rp04b4vdCZSH/88Yfztba905BNQ6asWbNaeKVh5quvvhrBbwwAAAD4B8IkAAAAAH5F//Feq2MuXLgg1atXt2oRdzZt2iS1a9e2+Tjjxo2T1KlTW4AwdepUC6NCq/YJTmcSrVixwmYOaWgRJ04c5zmtftEQQgON6NGjh/isVryERefzaEXR6dOnJV26dKFeqwFa5cqV5Z9//rFwQz8bL148OXv2rM0N0v08LyLz78XdNer/dUH8v1Dr4MGDFlLqfRcsWGC/Wxrs6fwkAAAA4FlFmAQAAADAr9SrV0/efvtt2bJli8ybN8/jdfoP/RourFy5UmLHju18X8Ok8CpevLh06NBBXnvtNWurtmjRIokR4//936ksWbJY4KCVTY6KH0/cVUSpWrVqybfffiuzZs2SXr16hbrG3r175dChQzJ9+nRp0aKF8/1Vq1a5vV5DFa16ct2bfl5lzJjR430yZMhgf2p44lrZpK3ljh8/bhVikU3vqZVAumfX6qQDBw4E2VNk/72EhwZ3jRs3tkOfRf369WXIkCH29+YaZgEAAADPEmYmAQAAAPArWlEyfvx46d+/v4UwnmiliYY3WsnjoG3dFi9eHKH7angyd+5cq0hp3ry5swJIwwS9l1amuFaxKH39999/BwkigrehU9qqL1++fBZK/PbbbyHO63yoTz75xPm9HGu73uerr77yuPcxY8YEuVZfa5VWxYoVQ/2+2tLu66+/DnKvyZMn23eoWbOmRLYaNWpYxZlrSPjw4UMZPXq0/b3rXKun8ffireCf0eejc7Z0vQcPHoR7PQAAAMBfUJkEAAAAwO+0bNkyzGs07Bg5cqRUq1bNWuNdunRJxo4da7NuXOfghEfdunWtskkrgnTO0cSJE60CRucyaWWKhlV6TYIECax6Rytl2rdvL927d7fPFy5c2IKSbt26SdGiRS0g0UBMg52FCxdaMKJt+Ro1amRzePT9/fv3W1s+nd+jYZO2tdN76pra2k73oVVYwWcnOWi1jAYt+syKFStmbd+WLVsmH3/8sc2g8kTP6XfSMEafobYM1Colbeume3/zzTclsumz0meq7fp27txplVPff/+9/PLLLzJq1Ch7rk/j78VbOiMpVapU9neTMmVK+euvvyyY0981T3sDAAAAngWESQAAAACeSRUqVLAqmk8//VS6dOli7c4+++wzCxYiGiYpDVG0Uujdd9+14GL48OHSs2dPa6X25ZdfOmfn6OwjDR80hHHQz+zZs8eCD71W27Y5qqs05NJz+r6GHVpBpVU2+n67du2kc+fOdp0GTD/++KO9HjZsmIVF2vqvU6dOUqBAgRD71eocDZPeeecd6dGjh4Ue/fr1szk/YdHqLw2VNDDp2rWrJEmSxEKYoUOH2j4im86tWr9+vT1PbeN3/fp1yZEjhz0vDZie1t+Lt7S94uzZsy2kvHnzpqRNm9b+Hnr37h3h7wwAAAD4g4DA4PX+AAAAAIBnggYwWtmjwQcAAAAARBQzkwAAAAAAAAAAAOARYRIAAAAAAAAAAAA8IkwCAAAAAAAAAACAR8xMAgAAAAAAAAAAgEdUJgEAAAAAAAAAAMAjwiQAAAAAAAAAAAB4FMPzKTxLHj9+LOfOnZMECRJIQEBAVG8HAAAAAAAAAABEocDAQLlx44akSZNGokULvfaIMOk5oUFSunTponobAAAAAAAAAADAh5w+fVrSpk0b6jWESc8JrUhy/FK8+OKLUb0dAAAAAAAAAAAQha5fv25FKI78IDSESc8JR2s7DZIIkwAAAAAAAAAAgPJmNE7oTfAAAAAAAAAAAADwXCNMAgAAAAAAAAAAgEeESQAAAAAAAAAAAPCIMAkAAAAAAAAAAAAeESYBAAAAAAAAAADAI8IkAAAAAAAAAAAAeESYBAAAAAAAAAAAAI8IkwAAAAAAAAAAAOARYRIAAAAAAAAAAAA8IkwCAAAAAAAAAACAR4RJAAAAAAAAAAAA8M0wafz48ZI/f3558cUX7ShRooT89NNPHq8vV66cBAQEhDhq1qxp5x88eCAfffSR5MuXT+LFiydp0qSRFi1ayLlz5554H3fv3pWOHTtK0qRJJX78+NKgQQO5ePFikGvc7W3u3LlePYt79+5JwYIF7TN79uxxvt+/f3+36+r3AwAAAAAAAAAAeKbDpLRp08qnn34qO3fulB07dkiFChWkTp06sn//frfXL1y4UM6fP+889u3bJ9GjR5eGDRva+du3b8uuXbukT58+9qdef/DgQaldu/YT76Nr167y448/yvz582XDhg0WUNWvXz/EWlOnTg2yx7p163r1LD788EMLv4Lr3r17kPX0yJ07t/M7AwAAAAAAAAAAPE0BgYGBgeJDkiRJIsOHD5e2bduGee2oUaOkb9++FrB4qtTZvn27vPLKK3Ly5ElJnz59hPbx77//SvLkyWXOnDny+uuv2/kDBw5Irly55LfffpPixYvbe1oxtGjRIq8DJAetgurWrZssWLBA8uTJI7t377YqJXd+//13O7dx40YpXbq01/e4fv26JEyY0L6LVl8BAAAAAAAAAIDn1/Vw5AY+MzPp0aNH1hLu1q1b1mbOG5MnT5YmTZqE2vJNH4KGPIkSJYrwPrRiSVvoVapUyXldzpw5LZzSMMmVtsJLliyZBVhTpkyRsLI6bZX31ltvycyZM+WFF14Ic3//+9//JHv27GEGSdo2T38RXA8AAAAAAAAAAIDwiiFRbO/evRba6EwinUWklT3axi0s27ZtszZ3Gih5omvqDKWmTZuGmaqFto8LFy5IrFixQgRSKVOmtHMOAwcOtBZ5Ggr9/PPP8u6778rNmzelc+fObu+pQVOrVq2kQ4cOUqRIETlx4kSoe9S9zZ49W3r27ClhGTZsmAwYMCDM6wAAAAAAAAAAiCwBAb75LH2rR5v/ifIwKUeOHLJnzx6rIPr++++lZcuWNpMorEBJQ6R8+fJZBZA7WknUqFEjC2zGjx//1PbhSmc1ORQqVMiqm7RVnqcwafTo0XLjxg3p1auXV+trwKXX697Comtq6zwHrUxKly6dV/cBAAAAAAAAAADwmTZ3WvGTNWtWKVy4sFXTFChQQL766qtQP6Mhjbai8zRXyREk6ZykVatWeTUjKLR9pEqVSu7fvy/Xrl0L0aJOz3lSrFgxOXPmjLWcc2ft2rXWJi927NgSI0YMu7/SKiV3gZG2uHvttdesIiosuqZ+b9cDAAAAAAAAAADA7yqTgnv8+LHH8MVh/vz5ds2bb77pMUg6fPiwrFu3TpImTfrE+9CAKWbMmLJmzRpp0KCBvXfw4EE5depUqPOdtNIpceLEFuy48/XXX8vgwYOdr8+dOydVq1aVefPmWRDl6vjx4/Z9lixZEqHvAwAAAAAAAAAA4HdhkrZiq169uqRPn97at82ZM0fWr18vK1euDLPFXd26dUMERRokvf7667Jr1y5ZunSpPHr0yDnTKEmSJFZ9FJF9JEyY0KqgtG2crqNVPu+9954FScWLF7drfvzxR6tU0tdx4sSxiqihQ4dK9+7dg8x5atGihYVSL730kt3Plc5qUlmyZJG0adMGOTdlyhRJnTq17RMAAAAAAAAAAOC5CJMuXbpk4cr58+ctsMmfP78FOJUrV7bzrVq1khMnTliw46AVQZs3b5aff/45xHpnz551Vu4ULFgwyDmt6ilXrpz9rH9mzJhRpk2b5tU+1JdffinRokWzyiStWNIKonHjxjnPa+XS2LFjpWvXrjanSVvWjRw5Ut566y3nNbdv37b9a+gV3iop3as+j+jRo4frswAAAAAAAAAAAE8iIFCTDx9VtmxZKV++vPTv3z9S182QIYMMGDDAwpnnxfXr1y0o+/fff5mfBAAAAAAAAAB4KgICfPPB+m4S4h+5gc/NTHLQzR89elSWLVsWqevu37/fHo5WIgEAAAAAAAAAAMCPK5MQeahMAgAAAAAAAAA8bVQmPZu5QTSJQuPHj7f5RLpJPUqUKCE//fRTqFVFOrNI5x0FBATIqFGjQlxz48YN6dKli7Wyixs3rpQsWVK2b98e6j50VtIbb7wh2bNnt7lI+vnQzJ071+5ft27dIO/fvHlTOnXqJGnTprV7586dWyZMmBDqWjoLSddyPeLEieM8r/OVPvroI8mXL5/EixdP0qRJY1VV586dC3VdAAAAAAAAAACAyBClYZKGLp9++qns3LlTduzYIRUqVJA6depYaOTO7du3JXPmzPaZVKlSub2mXbt2smrVKpk5c6bs3btXqlSpIpUqVZKzZ8963Me9e/ckefLk0rt3bylQoECoez5x4oR0795dSpcuHeJct27dZMWKFTJr1iz566+/LJTScGnJkiWhrqlBmgZajuPkyZNBvvOuXbukT58+9ufChQvl4MGDUrt27VDXBAAAAAAAAAAAeCbb3CVJkkSGDx8ubdu2DfU6rU7SsMa1iujOnTuSIEEC+eGHH6RmzZrO9wsXLizVq1eXwYMHh3n/cuXKScGCBd1WPT169EjKlCkjbdq0kU2bNsm1a9dk8eLFzvN58+aVxo0bW/Dj7b21Mkm/g67lLa20euWVVyx0Sp8+vVefoc0dAAAAAAAAAOBpo82d//CbNnfBgxptH3fr1i1rdxcRDx8+tHVc28QpbTm3efPmJ97jwIEDJUWKFB6DLm2pp1VIWgWlGd26devk0KFDVh0VGm2Pp2350qVLF2plloP+xWo7vESJEoVabaW/CK4HAAAAAAAAAABAeEV5mKSt6OLHjy+xY8eWDh06yKJFi2zWUERoVZIGUYMGDbKZQhosacu53377zdrHPQkNoyZPnizffPONx2tGjx5te9f2fbFixZJq1arJ2LFjrZrJkxw5csiUKVOsmkr3+vjxYwulzpw54/b6u3fv2gylpk2bhpoUDhs2zBJFx6FBFQAAAAAAAADAP6p7fO3A8y3KwyQNU/bs2SNbt26Vd955R1q2bCl//vlnhNfTWUlaFfTSSy9ZQPX1119b8BItWsS/6o0bN6R58+YWJCVLlizUMGnLli1WnaRzoEaMGCEdO3aU1atXe/yMhl8tWrSw1nply5a1mUg6v2nixIkhrn3w4IE0atTIvt/48eND3XOvXr2sgslxnD59OpzfGgAAAAAAAAAAQCRGVD8EreDJmjWrc76QzgP66quv3IYp3siSJYts2LDB2uVpa7fUqVPbHKPMmTNHeI9Hjx6VEydOSK1atZzvaQWRihEjhhw8eFDSpEkjH3/8sVVWOeY15c+f34KyL774QipVquTVvWLGjCmFChWSI0eOuA2SdE7S2rVrw+xfqEGaHgAAAAAAAAAAAH4dJgWnIY3O+3lS8eLFs+Pq1auycuVK+fzzzyO8Vs6cOa0dn6vevXtbxZIGX9pCTtvPaeATvAIqevTozuDJG9qaT+9Vo0aNEEHS4cOHbQ5T0qRJI/xdAAAAAAAAAAAA/CZM0lZs1atXl/Tp01swM2fOHFm/fr2FP+7cv3/f2QJPfz579qxV/ujMJUd1k35W28Bp+zyt7unRo4eFQa1btw51L7qOunnzply+fNlea9WUzkCKEyeO5M2bN8j1iRIlsj8d7+u12qZO7xc3blzJkCGDVUjNmDFDRo4c6fyctrTTFnw600gNHDhQihcvbvu/du2aDB8+3KqP2rVr5wySXn/9ddm1a5csXbrUwqYLFy7YuSRJkth9AQAAAAAAAAAAnskw6dKlSxaunD9/XhImTGht4TQMqly5sp1v1aqVtZfTgEmdO3fOWsA5aPs4PTTEcVyj84E0pDpz5oyFLQ0aNJAhQ4ZY+ziH/v37y7Rp02xtB9d1dd6RBlsaCLleE5a5c+favZs1ayb//POPfV7v3aFDB+c1p06dClK9pJVTb731lgVEiRMntlZ/v/76q4VYSgMzncGkdK6SK61SKleunNf7AwAAAAAAAAAACK+AQC3j8VEaEpUvX97Cn8jUsmVLCQgIsEDpeaHzozSw07AtrHlLAAAAAAAAAICoExDge0/f2yTBF/eufDcJ8Y/cwOdmJjno5o8ePSrLli2L1HU1O9Mqps2bN0fqugAAAAAAAAAAAM+i/+u3FgW04kgrhFwPnW+kNA3TVnU6D8nVqFGjbB6SziVKly6ddO3aVe7evevVmkpf60wi/azD/v37rR1exowZ7bzeIzidVdSnTx/JlCmT3TtLliwyaNAgC6dc13Z36BykiDyD4PReOmNKr1m8eLHXzxkAAAAAAAAAACCiorwyKU+ePLJ69Wrn6xgxPG9J5xj17NlTpkyZIiVLlpRDhw7ZXCUNV0aOHBmhNdXt27clc+bM0rBhQwun3Pnss89k/PjxMn36dFt/x44d0rp1awu9OnfubNfo7CdXP/30k7Rt29aCqsh4Bhpy6XcFAAAAAAAAAAB4bsIkDU5SpUrl1bW//vqrvPrqq/LGG2/Ya60katq0qWzdujXCa6qiRYvaoTSs8nTvOnXqSM2aNZ33/vbbb2Xbtm3Oa4Lf84cffrCZTxpUhcab/e7Zs0dGjBhhIVbq1Km9/m4AAAAAAAAAAAB+2+ZOHT58WNKkSWOBS7NmzeTUqVMer9VqpJ07dzoDnGPHjsny5culRo0aEV7TW3rvNWvWWDWU+v33323ukradc+fixYs270krk8IS1n61ckoDtLFjx3odkt27d8+GZ7keAAAAAAAAAAAAflWZVKxYMZk2bZrNQNIWcQMGDJDSpUvLvn37JEGCBCGu10DlypUrUqpUKZsf9PDhQ+nQoYN8/PHHEV7TW1qxpIGMzjOKHj26zVAaMmSIhT/uaDs8vV/9+vWf+Blo6z0Ns7QyylvDhg2ztQAAAAAAAADgeeOr00ICA6N6B4AfhkmuVT358+e3YCVDhgzy3Xffua3oWb9+vQwdOlTGjRtn1x45ckTef/99GTRokPTp0ydCa3pLPz979myb26QzjrTtXJcuXayiqGXLliGu17lOGjTFiRPniZ7BkiVLZO3atbJ79+5w7bdXr17SrVs352sNwtKlSxeuNQAAAAAAAAAAAKJ8ZpKrRIkSSfbs2S0kckcDo+bNm0u7du3sdb58+eTWrVvSvn17+eSTTyRatGjhXtNbPXr0sOqkJk2aOO998uRJqwAKHiZt2rRJDh48KPPmzQv3fYLvV4Oko0eP2vuuGjRoYBVMGrC5Ezt2bDsAAAAAAAAAAAD8emaSq5s3b1pwkjp1arfndXZQ8MBIW84pbXsXkTW95enejx8/DnHt5MmTpXDhwlKgQIFw3yf4fjXA+uOPP6wSynGoL7/8UqZOnRrh7wMAAAAAAAAAAODzlUndu3eXWrVqWVu3c+fOSb9+/Sygadq0qdvr9dqRI0dKoUKFnG3utFpJ33eESuFdU92/f1/+/PNP589nz5610CZ+/PiSNWtW5711RlL69OmtzZ22ndO9tGnTJsha2k5u/vz5MmLECLf3qlixotSrV086derk1X5TpUplR3C6j0yZMnn5pAEAAAAAAAAAAPwwTDpz5oyFJn///bckT55cSpUqJVu2bLGfVatWreTEiRPOVm69e/eWgIAA+1MDH73OEfJ4u6a7dTXE0YDK4YsvvrCjbNmyzmtGjx5twdW7774rly5dsllJb7/9tvTt2zfId5o7d65VSXkKr7Tq6MqVK+HaLwAAAAAAAAAAQFQJCPTUH84HaJhTvnx56d+/v1+s68u0YiphwoTy77//yosvvhjV2wEAAAAAAACApyYgwDcfrrf/Gu+L+/fnvSvfTUL8IzeI0sqk0OjmtYpn2bJlfrEuAAAAAAAAAADAs8hnwyRNw7QFnL+sCwAAAAAAAAAA8CyKFtUb0NlHb775piRNmlTixo0r+fLlkx07dni8/vz58/LGG29I9uzZJVq0aNKlS5dQ19cZRjpnqW7dumHuZfbs2VKgQAF54YUXJHXq1NKmTRubZeRq/vz5kjNnTokTJ47tdfny5UHOa+s8PR8vXjxJnDixVKpUSbZu3fpEz+HBgwfy0Ucf2Xu6rs5ratGihc16AgAAAAAAAAAAeGbDpKtXr8qrr74qMWPGlJ9++kn+/PNPGTFihIUwnty7d0+SJ08uvXv3tuAnNCdOnJDu3btL6dKlw9zLL7/8YgFN27ZtZf/+/RYabdu2Td566y3nNb/++qs0bdrUrtm9e7cFVHrs27fPeY2GXGPGjJG9e/fK5s2bJWPGjFKlShW5fPlyhJ/D7du3ZdeuXdKnTx/7c+HChXLw4EGpXbt2mN8LAAAAAAAAAADgSQQEBkbd2KmePXtaiLNp06YIfb5cuXJSsGBBGTVqVIhzjx49kjJlylh1ka5/7do1Wbx4sce1vvjiCxk/frzNU3IYPXq0fPbZZ862eI0bN5Zbt27J0qVLndcUL17c9jBhwoRQB1itXr1aKlasGGnPYfv27fLKK6/IyZMnJX369JE6SAsAAAAAAAAA/FlAgPgkb/813hf37897V1GXhPiu8OQGUVqZtGTJEilSpIg0bNhQUqRIIYUKFZJvvvkmUtYeOHCgralVRN4oUaKEnD592trWab528eJF+f7776VGjRrOa3777TdrW+eqatWq9r479+/fl0mTJtlfRmhVVBF5DvqXq+37EiVK5LGCS38RXA8AAAAAAAAAAIDwitIw6dixY1YNlC1bNlm5cqW888470rlzZ5k+ffoTravt5SZPnhyuYErbzOnMJK0+ihUrlqRKlcpCoLFjxzqvuXDhgqRMmTLI5/S1vu9KK5fix49vc5W+/PJLWbVqlSRLlizSnsPdu3dthpK23POUFg4bNsz27zjSpUvn9bMAAAAAAAAAAK0w8cUDwHMWJj1+/FhefvllGTp0qFXjtG/f3mYUeWoZ540bN25I8+bNLUgKLcAJTucUvf/++9K3b1/ZuXOnrFixwmYudejQIdx7KF++vOzZs8dmLFWrVk0aNWokly5dipTn8ODBA1tPq6c0gPKkV69eVr3kOLTqCgAAAAAAAAAAILxiSBRKnTq15M6dO8h7uXLlkgULFkR4TZ15pCFQrVq1goQ1KkaMGHLw4EHJkiWL20oerU7q0aOHvc6fP7/EixdPSpcuLYMHD7a9arWStr9zpa/1fVf6uaxZs9qhM5W04kgrpTTgeZLn4AiSdE7S2rVrQ+1hGDt2bDsAAAAAAAAAAAD8tjJJwxsNd1wdOnRIMmTIEOE1c+bMKXv37rXKIMdRu3ZtZ7WQp3Zvt2/flmjRgj6O6NGj259aBeSYq7RmzZog12gLO30/NBpm6QyjJ3kOjiDp8OHDsnr1akmaNGmo9wQAAAAAAAAAAPD7yqSuXbtKyZIlrb2bBiXbtm2TSZMm2REaDYXUzZs35fLly/Za5xxpdY/OKcqbN2+Q6xMlSmR/Bn/flVYyaWs5bR1XtWpVOX/+vHTp0kVeeeUVSZMmjV2jbfDKli0rI0aMkJo1a8rcuXNlx44dzv3eunVLhgwZYuGVVhtduXLFZi6dPXtWGjZs6LxXxYoVpV69etKpUyevnoMGSa+//rrs2rXL5jE9evTIOacpSZIk9t0BAAAAAAAAAACehoBAR9lNFNFwRNu/acVNpkyZpFu3bhbqOPTv31+mTZtmrescAtxMWdMqHtdrXLVq1UquXbsmixcvDnXd0aNH25yi48ePWwBVoUIF+eyzz+Sll15yXjN//nzp3bu3fU7b133++edSo0YNO3f37l154403ZOvWrRYkafVQ0aJF7Xr90yFjxoy2J92DN89B76XvubNu3TopV65cmM/5+vXrkjBhQpufFFp7PAAAAAAAAABQbv4Z1id48y/a/rx3X92/P+9dRW0S4pvCkxtEeZgUlpYtW1p4pMGPP6zrqwiTAAAAAAAAAISHP4cC/rx3X92/P+9d+XYS4vu5QZS2uQuL5lzr16+XzZs3+8W6AAAAAAAAAAAAzxqfDpO0cujkyZN+sy4AAAAAAAAAAMCzJlpU3lxnBmmw43rkzJnTq8/OnTvXrq9bt26IqqO+fftK6tSpJW7cuFKpUiWbQxSWs2fPyptvvmlzjvRz+fLlkx07dgTZq+4tXrx4kjhxYltXZyO5ql27tqRPn17ixIlj92/evLmcO3cu1PvqnKWOHTvafePHjy8NGjSQixcvBrmmc+fOUrhwYYkdO7YULFjQq+cDAAAAAAAAAADg92GSypMnj5w/f955eNN67sSJE9K9e3cpXbp0iHOff/65fP311zJhwgQLezT8qVq1qoU2nly9elVeffVViRkzpvz000/y559/yogRIyw0csiePbuMGTNG9u7da3vMmDGjVKlSRS5fvuy8pnz58vLdd9/JwYMHZcGCBXL06FF5/fXXQ/0uXbt2lR9//FHmz58vGzZssPCpfv36Ia5r06aNNG7cOMxnAwAAAAAAAAAAEJkCArWUJ4potc/ixYtlz549Xn/m0aNHUqZMGQtXNm3aJNeuXbM1lH6VNGnSyAcffGBhk9LBUSlTppRp06ZJkyZN3K7Zs2dP+eWXX2y98A6mWr16tVSsWNHtNUuWLLHKqXv37llQFZzuLXny5DJnzhxn6HTgwAHJlSuX/Pbbb1K8ePEnfl4RGaQFAAAAAAAAAAEBvvkMvPkXbX/eu6/u35/3rqIuCfFd4ckNorwySVvQaQCUOXNmadasmZw6dSrU6wcOHCgpUqSQtm3bhjh3/PhxuXDhgrWgc9AHUaxYMQtnPNHQp0iRItKwYUNbu1ChQvLNN994vP7+/fsyadIkW7tAgQJur/nnn39k9uzZUrJkSbdBktq5c6c8ePAgyH61lZ62ygttv97QAEt/EVwPAAAAAAAAAACA8IrSMElDHq0YWrFihYwfP97CIG1dd+PGDbfXa3u5yZMnewx6NEhSWonkSl87zrlz7Ngxu3+2bNlk5cqV8s4779icounTpwe5bunSpTbXSGciffnll7Jq1SpJlixZkGs++ugja62nM5A0GPvhhx883lf3FCtWLEmUKFG49uuNYcOGWdjlONKlS/dE6wEAAAAAAAAIP63S8MUDAPwmTKpevbpVA+XPn9/mGi1fvtza1uncoeA0YGrevLkFScEDnCf1+PFjefnll2Xo0KFWldS+fXt56623bO6SK52JpC3mfv31V6lWrZo0atRILl26FOSaHj16yO7du+Xnn3+W6NGjS4sWLaz93n+tV69eVprmOE6fPv2f7wEAAAAAAAAAAPi/GOJDtEIne/bscuTIkRDnjh49KidOnJBatWoFCYFUjBgx5ODBg5IqVSp7ffHiRUmdOrXzOn1dsGBBj/fVa3Pnzh3kPZ1btGDBgiDvacVR1qxZ7dB5RlrJpJVSGtw4aNClh34PXUMrgrZs2SIlSpQIcV/dr7bM0wDNtTpJ9+v4LhEVO3ZsOwAAAAAAAAAAAJ5ElM9McnXz5k0LjVyDINdZQnv37rXKIMdRu3ZtZ7WQhjaZMmWyEGbNmjXOz+msoK1bt7oNcxxeffVVC6NcHTp0SDJkyBDqfjXM0tlEoZ1Xnq4pXLiwzVNy3a/uQ9vjhbZfAAAAAAAAAACA56IyqXv37lZppKHNuXPnpF+/ftYarmnTpiGu1TlFefPmDfKeo5rH9f0uXbrI4MGDrWpIw6U+ffpImjRppG7duh730bVrVylZsqS1udPWddu2bZNJkybZoW7duiVDhgyx8EqDritXrsjYsWPl7Nmz1qZPaWC1fft2KVWqlCROnNhCMb13lixZnMGQXl+xYkWZMWOGvPLKKzbLqG3bttKtWzdJkiSJvPjii/Lee+/Z9Vr55KCVWhq06RylO3fuWHimtJpKZy4BAAAAAAAAAAA8k2HSmTNnLDj6+++/JXny5BbEaEs4/Vm1atXKWtutX7/e6zU//PBDC3907pG2j9M1V6xYYWGUQ7ly5SRjxowybdo0e120aFFZtGiRtasbOHCghVCjRo2SZs2a2XkNuA4cOCDTp0+3IClp0qT2mU2bNkmePHnsmhdeeEEWLlxogZjeX0MnnavUu3dvZ7u5Bw8eWOXR7du3nXv58ssvJVq0aNKgQQOrYNLZUePGjQvyndq1aycbNmxwvta5Tur48eP2PQAAAAAAAAAAAJ6WgMDAwEDxUWXLlrU2dv3794/UdbUSasCAARZWPS+03Z9WQv37779WAQUAAAAAAADg6QsI8M2n7M2/CrP3qHnuvvrs/XnvyneTEP/IDaK0Mik0unltFbds2bJIXXf//v32cFq0aBGp6wIAAAAAAAAAADyLokXlzbVFW0BAQIijY8eOFvhoG7z48eMH+Yy2n8uRI4fEjRtX0qVLZ/OO7t696zx/48YNm5uk1Ud6jc5C0llGDtqW7o8//rDWcg6bN2+WV1991drX6Wdy5sxp7eeC0zlJumdtmVesWDGbreRK96F713V039q67uLFi6E+Az2vFVI610lb5WlrvMOHDwe5RtvyBX9GHTp0CMeTBgAAAAAAAAAAiJgorUzSkOfRo0fO1/v27ZPKlStLw4YN3V4/Z84c6dmzp0yZMsVCokOHDlkQo+HKyJEjnfOFdJ2ZM2daQDNr1iypVKmS/Pnnn/LSSy+5XTdevHjSqVMnyZ8/v/2s4dLbb79tP+vsJTVv3jzp1q2bTJgwwYIkDbV0vpHOQEqRIoVdo8GWVlLNnz/fwjBds379+vLLL7+4va92GKxbt67EjBlTfvjhBysj0+/h2K/e3+Gtt96yeU4OGjwBAAAAAAAAAAA8VzOTtKJo6dKlVpmjAVFwGs789ddfsmbNGud7H3zwgWzdutUCoDt37kiCBAksmKlZs6bzmsKFC0v16tVl8ODBXu9FQyANczSUUhogFS1aVMaMGWOvHz9+bJVR7733ngVc2pYvefLkFni9/vrrds2BAwckV65c8ttvv0nx4sVD3EPDMK2y0vBLK6Yc66ZKlUqGDh1qwZijMqlgwYIWYEUUM5MAAAAAAACA/54/z49h71Hz3H312fvz3pXvJCG+Izy5QZS2uXN1//59qyJq06aN2yBJaTXSzp07ne3ljh07JsuXL5caNWrY64cPH1qlk7ahc6Wt6zRs8tbu3bvl119/lbJlyzr3pvfViiEHbZOnrzUoUnr+wYMHQa7Rdnnp06d3XhPcvXv37E/X/eq6sWPHDrHf2bNnS7JkySRv3rzSq1cvuX37dqjfQdfWXwTXAwAAAAAAAAAAwK/a3LlavHixXLt2zdrWefLGG2/IlStXpFSpUtYiTsMjnR308ccf23mtSipRooQMGjTIKoJSpkwp3377rYU5WbNmDXMPadOmlcuXL9u6/fv3d1YG6T01pNL1XOlrrT5SFy5ckFixYkmiRIlCXKPn3HGETRoOTZw40SqhdFaTzoo6f/58kO+tM6C0bZ/Oe/roo4+svd7ChQs9fpdhw4bJgAEDwvzOAAAAAAAAgC+jygEAop7PVCZNnjzZWtFpYOLJ+vXrrf3buHHjZNeuXRam6IwiDY8ctC2dBk06H0krfL7++mtp2rSpVfyEZdOmTbJjxw6bi6Qt5TSIepp0VpJ+B213lyRJEpuDtG7dOnsOrvvVuU06nylfvnzSrFkzmTFjhixatEiOHj3qcW0NqLQ0zXGcPn36qX4XAAAAAAAAAADwbPKJyqSTJ0/K6tWrQ620UX369JHmzZs7K4Y0XLl165aFLZ988okFMFmyZJENGzbY+9raLXXq1NK4cWPJnDlzmPvIlCmTc92LFy9adZIGUdpeLnr06PaeK32t842U/qnt8LS6yrU6yfUad3Se0549eyzw0c/r3CWdz1SkSBGPn9Hz6siRI/Z93dEgTQ8AAAAAAAAAAAC/r0yaOnWqpEiRQmrWrBnqdTonKHiFkYY8SquRXGnLOA2Srl69KitXrpQ6deqEa0+PHz92zjTS9nUa+qxZsybIeX2tbfWUntdKI9drtBXdqVOnnNeERodcaZB0+PBhq44Kbb8aPin9fgAAAAAAAAAAAM90ZZKGMhomtWzZUmLECH07tWrVkpEjR0qhQoWsOkcrc7RaSd93hEoaHGmwlCNHDjvfo0cPm03UunVrj+uOHTvWZhfpdWrjxo3yxRdfSOfOnZ3XdOvWzfaoFUOvvPKKtcHT6ifHuhoGtW3b1q7TlnUvvviivPfeexYkFS9e3LmO3kPnGdWrV89ez58/30Ikvf/evXvl/fffl7p160qVKlXsvLaymzNnjtSoUUOSJk1qM5O6du0qZcqUkfz58z/RswcAAAAAAAAAAPD5MEnb22n1Tps2bUKca9WqlZw4ccJmJanevXtLQECA/Xn27FkLYTRIGjJkiPMz2i5O5wWdOXPGQp0GDRrYea0actD2ddOmTbO1HYGWfub48eMWaGnruM8++0zefvtt52e0Vd7ly5elb9++cuHCBSlYsKCsWLFCUqZM6bzmyy+/tMopvadWNemcI53v5EqrlXSPDufPn7cAStvhaaVRixYtLCBz0KoofUaO8CpdunS2vj4DAAAAAAAAAACApy0gMHh/OB9StmxZKV++vIU/kUkrjDSU0kDpeaHzo7R6SoMsrZoCAAAAAAAA/EFAgPgkb/9V1Z/3z96j5rn76rP3570r301C/CM3iPLKJE9089ribdmyZZG6rmZnWum0efPmSF0XAAAAAAAAAADgWeSzYZKmYdqqLrJpRdLJkycjfV0AAAAAAAAAAIBnUbSovHnGjBkt3Al+dOzY0e31Dx48kIEDB9pMozhx4kiBAgVsbpGrjRs32hylNGnS2FqLFy8Ocx86m8ndPvLkyeP1XnX+krvzesyfP9/jvT19Zvjw4c5rdu3aJZUrV5ZEiRJJ0qRJpX379nLz5k2vnjEAAAAAAAAAAIDfhknbt2+X8+fPO49Vq1bZ+w0bNnR7fe/evWXixIkyevRo+fPPP6VDhw5Sr1492b17t/OaW7duWcg0duxYr/fx1VdfBdnH6dOnJUmSJEH2EdZe06VLF+S8HgMGDJD48eNL9erVPd47+GemTJliYVKDBg3s/Llz56RSpUqSNWtW2bp1q4Vn+/fvtwAMAAAAAAAAAADgaQsI1CFCPqJLly6ydOlSOXz4sAUqwWm10SeffBKkcklDl7hx48qsWbNCXK9rLFq0SOrWrRuufWg1U/369eX48eOSIUOGCO1VFSpUSF5++WWZPHmy1/fWvd64cUPWrFljrydNmiR9+vSxoClatP+X/e3du1fy589v99aQKbIHaQEAAAAAAAC+wsM/vUU5b/9V1Z/3z96j5rn76rP3570r30lCfEd4coMorUxydf/+fQuE2rRp4zGcuXfvnrW3c6VB0ubNmyN1Lxr+aDWQpyDJm73u3LlT9uzZI23btvX6vhcvXpRly5YF+Yx+51ixYjmDJMd3VqF9b/2c/iK4HgAAAAAAAAAAAOHlM2GSVgNdu3Yt1PZtVatWlZEjR1pFzuPHj63V3MKFC61qJ7JoW7mffvpJ2rVr90R71UAqV65cUrJkSa/vPX36dEmQIIFVRTlUqFBBLly4YDOUNMS6evWq9OzZ086F9r2HDRtmiaLj0DZ8AAAAAAAAeD7pfw/tiwcAwD/4TJik4YvOFtJWdqHNNsqWLZvkzJnTqnU6deokrVu3DlK186Q00EmUKFGorfHC2uudO3dkzpw54apKUjovqVmzZkGqr/LkyWN7GjFihLzwwguSKlUqyZQpk6RMmTLU792rVy8rTXMcOgcKAAAAAAAAAADAL8OkkydPyurVq0OtBlLJkye3qqBbt27ZZw4cOCDx48eXzJkzR8o+dHyUBjrNmze3sCqie/3+++/l9u3b0qJFC6/vvWnTJjl48KDbdd944w2rTjp79qz8/fff0r9/f7l8+XKo3zt27NjW49D1AAAAAAAAAAAA8MswaerUqZIiRQqpWbOmV9dr5c5LL70kDx8+lAULFkidOnUiZR8bNmyQI0eOhFpR5M1etXKpdu3aFn55Sz9TuHBhKVCggMdrtBpJw7N58+bZM6hcubLX6wMAAAAAAAAAAPhlmKSzjzSgadmypcSIESPUa7du3Wozko4dO2aVPNWqVbPPf/jhh85rbt68KXv27LFDHT9+3H4+deqUV4FOsWLFJG/evBHeq4ZRGzdu9Fi5pC36Fi1aFOS969evy/z58z1+ZsyYMbJr1y45dOiQjB071tr76UwkbccHAAAAAAAAAADwTIdJ2jJOg542bdqEONeqVSspV66c8/Xdu3eld+/ekjt3bqlXr55VJ23evDlIqLJjxw4pVKiQHapbt272c9++fZ3XaJu4jBkzBrmXzhXSKqfQqpJC26uDtslLmzatVKlSxe15bWWn93I1d+5ca7HXtGlTt5/Ztm2bVSHly5dPJk2aJBMnTpTOnTt73AMAAAAAAAAAAEBkCQjUFMNHlS1bVsqXL2/hT2TSyqKAgACZNm2aPC+0+ilhwoQWZDE/CQAAAAAA4PkSECA+yZt/mfTnvfv7/tl71Dx3X332/rx35btJiH/kBqH3lYtCuvmjR4/KsmXLInVdzc7Wr19vFU0AAAAAAAAAAAAQ/wyTNA07c+ZMpK+rFUknT56M9HUBAAAAAAAAAACeRVE6M0nnFmm4E/zo2LGjx8/Mnz9fcubMKXHixLEZQsuXLw9xzV9//SW1a9e2QCpevHhStGhRm3XkyTfffCOlS5eWxIkT21GpUiWbUxS8oknnLqVOnVrixo1r1xw+fDjINbt27bLZRjrDKWnSpNK+fXu5efNmqM9Az3fq1MnmLOm6Og9qwoQJQa7RuVHBn1GHDh1CXRcAAAAAAAAAAMDvw6Tt27fL+fPnnceqVavs/YYNG7q9/tdff5WmTZtK27ZtZffu3VK3bl079u3b57xGW+OVKlXKAidtZ/fHH39Inz59LHzyRK/TddetWye//fabpEuXTqpUqSJnz551XvP555/L119/bUHP1q1bLaSqWrWq3L17186fO3fOAqasWbPa+RUrVsj+/fulVatWoT6Dbt262bWzZs2yEKxLly4WLi1ZsiTIdW+99VaQZ6X7AQAAAAAAAAAAeNoCArXkxkdokLJ06VKr+NHqm+AaN24st27dsmscihcvLgULFnRW8zRp0kRixowpM2fOjPA+Hj16ZBVKY8aMkRYtWlhVUpo0aeSDDz6Q7t27O2c6pUyZUqZNm2b3nDRpkoVWGvREi/b/Mrq9e/dK/vz57ftoyORO3rx57XvpZx0KFy4s1atXl8GDBzsrk/Q7jho16j8ZpAUAAAAAAIBni5t/avMJ3vzLpD/v3d/3z96j5rn76rP3570r30lCfEd4coMorUxydf/+favOadOmjdsgSWnVkFb/uNLqIH1fPX78WJYtWybZs2e391OkSCHFihWTxYsXh2svt2/flgcPHkiSJEns9fHjx+XChQtB7q0PWNd23PvevXsSK1YsZ5CktG2d2rx5s8d7lSxZ0qqQtApKQyutjjp06JBVRrmaPXu2JEuWzMKnXr162R5Do/vRXwTXAwAAAAAAAAAAILx8JkzSwOfatWuhtoXTQEergVzpa31fXbp0yWYQffrpp1KtWjX5+eefpV69elK/fn3ZsGGD13v56KOPrBLJER451g/t3hUqVLCfhw8fbsHY1atXpWfPnnZOq5U8GT16tM1J0plJGkbpvseOHStlypRxXvPGG29Y0KZBkwZJWnX15ptvhvodhg0bZoGX49DWfQAAAAAAAIg4/e+fffEAAOBpiyE+YvLkydbaTUOciNLKJFWnTh3p2rWr/azt4XTWkrbBK1u2bJhraBA1d+5cm6MU2pyl4PLkySPTp0+3GUga+ESPHl06d+5sgZNrtZK7MGnLli1WnZQhQwbZuHGjdOzYMUiY1b59e+f1+fLlk9SpU0vFihVtPlSWLFncrqt70L04aGUSgRIAAAAAAAAAAPDLMOnkyZOyevVqWbhwYajXpUqVSi5evBjkPX2t7yttAxcjRgyr9HGVK1euUFvNOXzxxRcWJuledNaR630d99Igx/XeGla5VhDpoe/HixfP2vWNHDlSMmfO7PZ+d+7ckY8//lgWLVokNWvWtPf0vnv27LG9BG/p56Dt9dSRI0c8hkmxY8e2AwAAAAAAAAAAwO/b3E2dOtXmGzkCFU9KlCgha9asCfLeqlWr7H2lbeKKFi0qBw8eDHKNziDSqp/QfP755zJo0CBZsWKFFClSJMi5TJkyWaDkem+t9Nm6davz3q60Gil+/Pgyb948q26qXLmy23vqXCY9glcuaVWTo8rKHQ2blGuwBQAAAAAAAAAA8ExWJmloomFSy5YtraooNO+//761qhsxYoQFT9qObseOHTJp0iTnNT169JDGjRvbzKHy5ctbOPTjjz9a2zpPPvvsM+nbt6/MmTNHMmbM6JyDpIGQHlph1KVLFxk8eLBky5bNwqU+ffpYK7q6des61xkzZoyULFnSPqMhl+5FK50SJUrkvCZnzpw2z0hnOb344ov2ffS6uHHjWuCls51mzJhhFU1KW9npvmrUqCFJkyaVP/74w1r46fdzrZ4CAAAAAAAAAAB4GgICAwMDJQr9/PPPUrVqVasmyp49e5BzrVq1khMnTgQJgubPny+9e/e29zXY0YoiDVpcTZkyxQKbM2fOSI4cOWTAgAE2R8nTuhogaau94Pr16yf9+/e3n/Ux6WsNrq5duyalSpWScePGBdlzixYtZNmyZXLz5k0Ljbp37y7NmzcPsqYGUxqe6R6UBlc630ifwz///GOBks5I0sBIrz19+rS8+eabsm/fPrl165bNPdIgSp+BhlHe0kqqhAkTyr///huuzwEAAAAAAMDx7zq++SS8+dc99h41z51n/3Q867/zvrp/f967itokxDeFJzeI8jApNFq1o9VFjkDH19f1ZYRJAAAAAAAAT8af/4GUvUfNc+fZPx3P+u+8r+7fn/eufDcJ8Y/cIMrb3Hmim9cWb1rp4w/rAgAAAAAAAAAAPIuiiQ/R+UKO+USahmmbOp0/5KpcuXJ2TfBDZyipBw8eyEcffST58uWTePHi2VwjbT937tw5O+9pXW11527djh07Oq/RlnTati5VqlS29ssvvywLFiwIso62qmvWrJmleDorqW3bttb2Liy//fabVKhQwdbVz+pMpDt37jjPHzp0yFr1JUuWzM5rm71169ZF8EkDAAAAAAAAAAD4WZi0fft2mThxouTPnz/U6xYuXCjnz593HjpLKHr06NKwYUM7f/v2bdm1a5f06dPH/tTrdR5T7dq1w7y/67qrVq2y9x3rKg2ldK0lS5bI3r17pX79+tKoUSPZvXu38xoNkvbv32+fX7p0qWzcuNFmIIUVJFWrVk2qVKki27Zts7106tRJokX7v7+e1157TR4+fChr166VnTt3SoECBew9DbgAAAAAAAAAAACeFp+YmaSVO1rlM27cOBk8eLAULFhQRo0a5dVn9bq+fftaAKRVPe5oOPPKK6/IyZMnJX369F6tq9VRGgYdPnzYKpSUVjONHz/eqpMckiZNKp999pm0a9dO/vrrL8mdO7fdr0iRInZ+xYoVUqNGDauG0iopd4oXLy6VK1eWQYMGuT1/5coVSZ48uQVTpUuXtvdu3LhhFUoaWlWqVCnM78PMJAAAAAAAgCfjz3NA2HvUPHee/dPxrP/O++r+/XnvKuqTEN8TntzAJyqTtJWctqnzJhQJbvLkydKkSROPQZLSB6GBkLad88b9+/dl1qxZ0qZNG2eQpEqWLCnz5s2zVnaPHz+WuXPnyt27d631nqPCSO/hCJKUfietMNq6davbe126dMnOpUiRwtZPmTKllC1bVjZv3hwksMqRI4fMmDFDbt26ZRVKWsWlnylcuLDbde/du2e/CK4HAAAAAAAAAABAeMWQKKaBjLaj02qe8NKWcNrmTgMlTzTs0RlKTZs2DTNZc1i8eLFcu3ZNWrVqFeT97777Tho3bmzhTowYMeSFF16QRYsWSdasWe28tpzTgMeVXpckSRKP7eiOHTtmf/bv31+++OILq8rS0KhixYr23bJly2aB1urVq6Vu3bqSIEECC6f0Plr1lDhxYrfrDhs2TAYMGODV9wUAAAAAAPiv+OJ/sc5/rQ4AgPhuZdLp06fl/fffl9mzZ0ucOHHC/XkNkfLly2ct7Nx58OCBzTTSTn7ani4861avXj1EWzqdw6QhkwY7O3bskG7dutn6Oj8porTCSb399tvSunVrKVSokHz55ZdWiTRlyhQ7p/vX6i0NkDZt2mQhmgZLtWrVsvZ+7vTq1csqshyHPmsAAAAAAAAAAAC/qkzauXOntXnTeUkOjx49stlAY8aMsVZt0aNHd/tZbfemVU0DBw4MNUjSOUlr1671uipJr9ewaOHChUHeP3r0qO1Jq4Xy5Mlj7xUoUMDCnbFjx8qECRMkVapU9n1caUs6bYun59xJnTq1/amzllzlypVLTp06ZT/r/nV+09WrV53fQ+dL6byk6dOnS8+ePUOsGzt2bDsAAAAAAAAAAAD8tjJJW7lpVc+ePXuch84batasmf3sKUhS8+fPt7DpzTff9BgkHT582IIhbUvnralTp1oFkM5wcnX79m37U1vMudI9OqqLSpQoYZVLGpI5aBCk54sVK+b2fhkzZrQKqIMHDwZ5/9ChQ5IhQ4ZQ762vHfcGAAAAAAAAAAB45iqTdP5P3rx5g7wXL148C3+Cv++uFZ22egseFGmQ9Prrr9scJq3m0Uonx7winV0UK1Ysj2tqMKNhUsuWLW3WkaucOXPabCRtR6ezjfS+OltJq4P0Po5qomrVqslbb71llUq6l06dOkmTJk2cLfPOnj1rIZrORdL2fDoPqUePHtKvXz+rdNKZSVptdODAAfn++++dIZXORtJ99e3bV+LGjSvffPONHD9+PEToBQAAAAAAAAAA8MyESd5o1aqVnDhxQtavX+98T6t4Nm/eLD///HOI6zWsWbJkif2swYyrdevWSbly5exn/VOrgqZNm+Y8r1VM2lquTZs2IdaNGTOmLF++3FrK6ayimzdvWrikwU+NGjWc1+n8Jw2QNDDSyqEGDRrI119/7TyvAZPu31FtpLp06SJ3796Vrl27Wks8DZU0pMqSJYudT5YsmaxYsUI++eQTqVChgq2hrfZ++OEHuxYAAAAAAAAAAOBpCQgMDAwUH1a2bFkpX7689O/fP1LX1RZyAwYMsLDqeXD9+nVJmDCh/Pvvv17PjwIAAAAAAIhsAQG+90y9/dcxX9y7t/tn71Hz3Hn2T8ez/jvvq/v3570r305CfD838OnKJP0CR48elWXLlkXquvv377cH1KJFi0hdFwAAAAAAAAAA4Fnj85VJiBxUJgEAAAAAAF/gi//F+vPwX9uz96h57jz7p+NZ/5331f37894VSciT5QbRJAo9evRI+vTpI5kyZZK4cePajKBBgwZJWPnW2LFjJVeuXPaZHDlyyIwZM0JcM2rUKDun16RLl87mEelcIk+0jV5AQECII168eM5rFi5cKEWKFJFEiRLZ+zqTaebMmUHW0VlKOjMpbdq0du/cuXPLhAkTwqyU0tlKOsNJ76l7D82nn35q1+msJQAAAAAAAAAAgKcpStvcffbZZzJ+/HiZPn265MmTR3bs2CGtW7e2JKxz585uP6PX9+rVS7755hspWrSobNu2Td566y1JnDix1KpVy66ZM2eO9OzZU6ZMmSIlS5aUQ4cO2WwkDWBGjhzpdt3u3btLhw4dgrxXsWJFu4dDkiRJ5JNPPpGcOXNKrFixZOnSpbbfFClSSNWqVe2abt26ydq1a2XWrFkWDv3888/y7rvvSpo0aaR27dpu73379m3JnDmzNGzY0EKv0Gzfvl0mTpwo+fPnD+PpAgAAAAAAAAAA+HmY9Ouvv0qdOnWkZs2a9lrDl2+//dYCIk+0Eujtt9+Wxo0b22sNYTRg0WDKESbpuq+++qq88cYbznWbNm0qW7du9bhu/Pjx7XD4/fff5c8//wxSVVSuXLkgn3n//fctCNu8ebMzTNJ7t2zZ0nlt+/btLfzR7+QpTNLAyhFaaQjmiVY9NWvWzIK0wYMHe7wOAAAAAAAAAAAgskRpmzutGlqzZo1VDjkCHA1mqlev7vEz9+7dkzhx4gR5T9vJaVjz4MED57o7d+50hlLHjh2T5cuXS40aNbze2//+9z/Jnj27lC5d2u15bcWnez948KCUKVMmyHdasmSJnD171q5Zt26dfb8qVarIk+rYsaMFb5UqVQrzWn1O2u/Q9QAAAAAAAAAAAPCryiStwtGQQ9vGRY8e3WYoDRkyxKpvPNEKIA166tatKy+//LKFRvpag6QrV65I6tSprSJJfy5VqpQFOg8fPrQWdh9//LFX+9LZSrNnz3ZbJaSDqF566SULa3TP48aNk8qVKzvPjx492qqRdGZSjBgxJFq0aFZJ5Bo4RcTcuXNl165dVoXljWHDhsmAAQOe6J4AAAAAAMD3MNgcAAA8V5VJ3333nYU2OuNIgxJtGffFF1/Yn5706dPHKpeKFy8uMWPGtDZ52lZOaXCj1q9fL0OHDrWgR9dduHChLFu2TAYNGuTVvhYtWiQ3btxwrusqQYIEsmfPHgt1NPjSGUl6P9cwacuWLVadpEHXiBEjrKJo9erVElGnT5+2lnr6rIJXZXmic6U0+HIcugYAAAAAAAAAAEB4BQRq6U4USZcunVX/aNjioLOAZs2aJQcOHAj1s1qJdPHiRatEmjRpknz00Udy7do1C5S0NZ2GTcOHD3der2tqxZDOHXKETp5UrFhRXnzxRQuVwtKuXTsLalauXCl37tyRhAkT2uccc6Ac15w5c0ZWrFgR5no636lLly52OCxevFjq1atnlVAOWsUVEBBg38VRJRUarQDTvWmwpN8NAAAAAAD4J3+vTPLF/fvz3r3dP3uPmufOs386nvXfeV/dvz/vXUVdEuK7wpMbRGmbu9u3b4cIdjQUefz4cZif1aokbSXnaAH32muvOdfytK4KKzs7fvy4zTnSyiJv6F41zHEEXHpE9DuFFm7t3bs3yHutW7e29oAaooUVJAEAAAAAAAAAAERUlIZJtWrVslZx6dOnlzx58sju3btl5MiR0qZNG4+fOXTokGzbtk2KFSsmV69etev37dsXpDWerqvvFypUyK47cuSItcfT98MKXqZMmWLVTtpKz90coiJFikiWLFksQFq+fLnMnDlTxo8fb+c1uStbtqz06NFD4saNKxkyZJANGzbIjBkzbD8OLVq0sLlLup66f/++/Pnnn86fz549a6304sePL1mzZrXWennz5g2yl3jx4knSpElDvA8AAAAAAAAAAPDMhEk6X0hDnnfffVcuXbokadKkkbffflv69u3rvKZ///4ybdo0OXHihLO9m84hOnjwoFUnlS9fXn799VdrD+fQu3dvawGnf2owkzx5cmdw5aBranWPa6WSVg/p+61atXIbOt26dcv2qi3rNCzSyiBtn9e4cWPnNVolpfOKmjVrJv/8848FSnrfDh06OK85depUkOqlc+fOWfDloHOj9NBgynUeEwAAAAAAAAAAwHM1M8kbLVu2tGBIQ57I1K9fP6sael7CGmYmAQAAAADwbPD3WRS+uH9/3vvzMD/Gn/fu7/tn71Hz3H312fvz3pVvJyFRw29mJoVFcy4NezZv3hzpa//0008yZsyYSF8XAAAAAAAAAADgWeLTYZJWJJ08efKprK1zlwAAAAAAAAAAABC6/xvcEwXGjx8v+fPnt/IpPUqUKGEVQ5588803Urp0aUmcOLEdlSpVChEKaTWTzlxKnTq1zTXSaw4fPhzqPm7cuCFdunSx+Ub6mZIlS8r27duDXHPx4kWbpaRz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YdOyZcsEYxHhwBk/fryNbRRMpUqVbAyl/Pnz2/hGOLbq169v5U6TJk3YNHEeTZ482f8ZR5mjevXqNp6SF5xw5L1y5coRZRVCCCGEEEIIIYQQQgghhIhbZ9Ly5cvtyh2cQ8CqoBkzZphVq1aFvebVV1+1K5mee+45+7lkyZJ2G7znn38+wJmE8yhnzpxRy3LdddfZAx599NGw5x07dsw6iyZMmGCGDRt21u/333+//2/ywznly5c327dvtyuWwoHzKJy8l1xyScBvp06dMh9++KHp0aOHXZ0khBBCCCGEEEIIIYQQQghxQW5zx4obVtds3brVfv7222+tY6hhw4Zhr1mxYoWpV69ewHc4kfjey48//mhy585tVxvh/Pn111+TReZu3bpZ51ewDKE4fvy4XW2E8yt4q75g2Moue/bspnjx4ubBBx80v/32W9hz58yZY39nFVc4/vnnHxs8y3sIIYQQQgghhBBCCCGEEELE1cokVgDh5CCeEVvAEUPpqaeess6fcOzbt8/kyJEj4Ds+k85ff/1lYxVdf/31No4Sjhm2hxs8eLCpWbOm+e6770zmzJmTLO/MmTPNN998k2CcoldeecX07dvXOpOQYeHChXZ1UaQt7po3b26dTtu2bTOPPfaYdajhIAu1Nd7EiROtAy1v3rxh0xw+fLjNtxBChCJWFzX+X8g8IYQQQgghhBBCCCFEDJGizqRZs2bZuEfTp0+3MY7Wr19vevbsaVcUtW3bNsnpelc2EdcI51KBAgXs/Tp27JikNHfu3Gkefvhh6xjKkCFDxHNxht18883WkTVq1CjTqlUr89VXX4W97q677vL/XbZsWSszW+KxWqlu3boB5+7atcssWLDA5iUS/fv3N7179/Z/xtmW0OooIYQQQgghhBBCCCGEEEKImHImPfLII3Z1knOm4EjZsWOHXVUTzplE7KD9+/cHfMfnyy+/3K5KCsWVV15pihUrZn766acky7p27Vpz4MABU7FiRf93rKT68ssvzUsvvWS3lXOriK644gp7XHPNNaZq1aomS5YsZvbs2ebuu++O6l5szXf11VdbeYOdSWybd9VVV5nbbrstYhrEYOIQQgghhBBCCCGEEEIIIYSIW2fSiRMnTOrUgWGbcMicOXMm7DXVqlUzH3/8ccB3rBbi+3AcO3bMbh933333JVlWnDobN24M+I6YRWzR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hgwB57z//vumfv365qqrrrK/r1+/PlFyzZw5016HPIlNd9++fea+++4zOXPmNBkzZjQVK1Y07733XoL3JC7Tvffea9O+9NJLTdmyZc2aNWv8v7MlX3C+b7nllkTlSwghhBBCCCGEEEIIIYQQIq6cSV988YXp1q2b+frrr83ChQvNqVOnrLPm+PHjEa9j7769e/f6jx07dgT8zvU33HCDGTFiRKJl2r59u+nTp4+pWbPmWb9Fky7b5+EQmzNnjtm4caNp3ry5adWqlVm3bl3Ya44cOWJq1Khh0qVLZz755BPz/fffm+eee85kyZIl4DycR958z5gxI9H5E0IIIYQQQgghhBBCCCGEiJtt7ubPn3/WqiNWKK1du9bceOONYa9jVQ4rf8LByiDnGEoMp0+fNq1btzaDBw82S5cuNUePHk10usuXLzfjxo0zVapUsZ+feOIJ8/zzz9s8VahQIeQ1OKfy5ctnJk+e7P+uUKFCZ52XPn36iPkWQgghhBBCCCGEEEIIIYS4oGMm/f777/b/rFmzRjzv2LFjpkCBAubMmTN2G7mnn37axkI6V4YMGWKdWR07drTOpKRQvXp18/bbb5tGjRqZK6+80syaNcv8/fffpnbt2mGvYRVTgwYNTMuWLe1qrTx58piuXbuazp07B5y3ZMkSKx8rlm666SYzbNgwuy1eKP755x97BJftH3/8kaR8CZFY4lnVJLvKXnoTP8RzfY13+SW7yl56Ez/Ec32Nd/klu8peehM/xHN9jXf5JbvKXnoTP8Rzfb0Q5D8fOH+Bz+dL+GRfjHD69Glfo0aNfDVq1Ih43vLly31Tp071rVu3zrdkyRJf48aNfZdffrlv586dZ537yy+/UAL23IRYunSpL0+ePL6DBw/az23btvU1bdo05LmR0j1y5Iivfv369ve0adNa2RYsWBDx3unTp7dH//79fd98841v/PjxvgwZMvimTJniP2fGjBm+Dz/80Ldhwwbf7NmzfSVLlvRdd911vn///TdkmgMHDrQy6FAZSAekA9IB6YB0QDogHZAOSAekA9IB6YB0QDogHZAOSAekA9IB6YB0QDpgwpRBKP9KMDGzMonYSd99951ZtmxZxPOqVatmD+9KoJIlS5rx48eboUOHJunef/75p93CbsKECebqq68258KAAQPs9nifffaZTeuDDz6wMZNY6VS2bNmQ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",
      "text/plain": [
       "<Figure size 2000x500 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "#creating a line chart using the top30 data\n",
    "plt.figure(figsize=(20,5))\n",
    "plt.bar(just30['name'], just30['marketcap'],color='blue')\n",
    "plt.title('MarketCap of Tokens')\n",
    "plt.xlabel('Name of Tokens')\n",
    "plt.ylabel('MarketCap')\n",
    "plt.savefig('bar_chart.png')"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "c8361e8c-4e8f-49fd-b5cf-60c057383627",
   "metadata": {},
   "source": [
    "### Step 3 Pie Chart"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "id": "0500f9b3-d260-40fd-b06b-20f2cf24df91",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>name</th>\n",
       "      <th>price</th>\n",
       "      <th>volume24hrs</th>\n",
       "      <th>marketcap</th>\n",
       "      <th>circulatingsupply</th>\n",
       "      <th>maxsupply</th>\n",
       "      <th>totalsupply</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>5510</th>\n",
       "      <td>Axelar Wrapped wstETH</td>\n",
       "      <td>1.595659e+09</td>\n",
       "      <td>87345.60631</td>\n",
       "      <td>2,79,031.47</td>\n",
       "      <td>2.399138e+05</td>\n",
       "      <td>872648297.8</td>\n",
       "      <td>208556067.2</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>17483</th>\n",
       "      <td>Sex One</td>\n",
       "      <td>3.556377e+06</td>\n",
       "      <td>867177.86630</td>\n",
       "      <td>6,54,442.14</td>\n",
       "      <td>3.993443e+06</td>\n",
       "      <td>651573104.6</td>\n",
       "      <td>748713356.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>18763</th>\n",
       "      <td>Sushi Fighter</td>\n",
       "      <td>2.307439e+06</td>\n",
       "      <td>628814.05320</td>\n",
       "      <td>3,59,836.53</td>\n",
       "      <td>4.053118e+06</td>\n",
       "      <td>838728403.2</td>\n",
       "      <td>133760316.1</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>13329</th>\n",
       "      <td>Maya Preferred</td>\n",
       "      <td>4.846371e+05</td>\n",
       "      <td>677354.92920</td>\n",
       "      <td>6,09,317.76</td>\n",
       "      <td>5.543653e+05</td>\n",
       "      <td>875055029.8</td>\n",
       "      <td>409733170.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>15363</th>\n",
       "      <td>PaleBlueDot</td>\n",
       "      <td>4.586141e+05</td>\n",
       "      <td>948143.78130</td>\n",
       "      <td>4,71,202.06</td>\n",
       "      <td>3.959904e+06</td>\n",
       "      <td>392859399.6</td>\n",
       "      <td>969741491.7</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "                        name         price   volume24hrs    marketcap  \\\n",
       "5510   Axelar Wrapped wstETH  1.595659e+09   87345.60631  2,79,031.47   \n",
       "17483                Sex One  3.556377e+06  867177.86630  6,54,442.14   \n",
       "18763          Sushi Fighter  2.307439e+06  628814.05320  3,59,836.53   \n",
       "13329         Maya Preferred  4.846371e+05  677354.92920  6,09,317.76   \n",
       "15363            PaleBlueDot  4.586141e+05  948143.78130  4,71,202.06   \n",
       "\n",
       "       circulatingsupply    maxsupply  totalsupply  \n",
       "5510        2.399138e+05  872648297.8  208556067.2  \n",
       "17483       3.993443e+06  651573104.6  748713356.0  \n",
       "18763       4.053118e+06  838728403.2  133760316.1  \n",
       "13329       5.543653e+05  875055029.8  409733170.0  \n",
       "15363       3.959904e+06  392859399.6  969741491.7  "
      ]
     },
     "execution_count": 13,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#to get the desired beauty of piechart and the labels I decided to reduce the data to just 7 tokens\n",
    "sort = ncd.sort_values('price', ascending =False)\n",
    "piet = sort.head(7)\n",
    "piet.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "id": "7cf475b9-a995-4207-9160-d7aab2f2a015",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAAncAAAGrCAYAAACi3rGrAAAAOnRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjEwLjgsIGh0dHBzOi8vbWF0cGxvdGxpYi5vcmcvwVt1zgAAAAlwSFlzAAAPYQAAD2EBqD+naQAASBpJREFUeJzt3Qd81PX9x/HPZQ9CgIS991BwAG4R96x777216r9aW1s71NqqVeuoWq17z7oX4sDNcIACsjeEFUISsu7u/3h/k1+4hBCyb72ePO5x5Ob3vhn3vs93/HzBYDBoAAAAiAkJ4W4AAAAAWg7hDgAAIIYQ7gAAAGII4Q4AACCGEO4AAABiCOEOAAAghhDuAAAAYgjhDgAAIIYQ7gAAAGII4Q5AVDr77LOtX79+FqnmzJljBx10kGVnZ5vP57P//e9/rfp848ePt+23375VnwNAdCDcAWhzjz/+uAs83iktLc2GDBlil19+ua1atSomviNnnXWWTZ8+3W655RZ76qmnbMyYMXUGstB+2Nrpz3/+c1heA4DolBTuBgCIX3/961+tf//+VlJSYp9//rk98MAD9s4779iMGTMsIyOj3vs+/PDDFggELBJt2rTJvvrqK7vhhhtcYN0aXX/++edXfz158mS755577Pe//70NHz68+vJRo0a1epsBxA7CHYCwOfTQQ6srWgo5OTk5duedd9rrr79up5xySp33KSoqsszMTEtOTrZItXr1anfeoUOHem934IEH1vhaFUyFO12uqh4ANAXDsgAixn777efOFyxYUD2vrl27djZv3jw77LDDLCsry0477bStzrlTJe9f//qXjRw50gWlzp072yGHHGJTpkypcbunn37aRo8ebenp6dapUyc7+eSTbcmSJQ1q43fffedCafv27V3b9t9/f/v666+rr9cQat++fd3/r732Wjes2ty5gf/+979tu+22s9TUVOvRo4dddtlllp+fv837ffDBB64CqqBcUVHhLps1a5Ydf/zx7nWrjxSu33jjjTqHzb/44gu75pprXD8qUB9zzDHVwdWjvj344IMtNzfX9acqseeee26zXi+A5qFyByBiKMSJKngehRKFh7322svuuOOOeodrzzvvPBdMFL5UCdR9J02a5MKXVyHUHLg//vGPduKJJ7rbKKzce++9Nm7cOBfc6qu2/fTTT7b33nu7YHfddde56uFDDz3kqmyffvqp7brrrnbssce6x7j66qtdqFIoVQhsKoXFv/zlL3bAAQfYJZdcYrNnz3bD1xrCVfjaWgXzrbfeciHupJNOskcffdQSExNd+/fcc0/r2bOnXX/99S6wvfjii3b00UfbK6+84sJbqCuuuMI6duxof/rTn2zhwoV29913u2HmF154wV2fl5fnFo0o/Onx9Lp1u1dffbXJrxdACwgCQBt77LHHgvrzM2HChODq1auDS5YsCT7//PPBnJycYHp6enDp0qXudmeddZa73fXXX7/FY+i6vn37Vn89ceJEd9srr7xyi9sGAgF3vnDhwmBiYmLwlltuqXH99OnTg0lJSVtcXtvRRx8dTElJCc6bN6/6suXLlwezsrKC48aNq75swYIFri233357o/rlpZdecvf7+OOP3dd5eXnu+Q466KCg3++vvt19993nbvfoo49WX7bPPvsEt9tuO/f/V155JZicnBy84IILatxv//33D44cOTJYUlJSo2/22GOP4ODBg7f4/hxwwAHVfSdXX32167/8/Hz39WuvveZuN3ny5Ea9TgCti2FZAGGjapSqPr1793ZDo6pwvfbaa66yFEoVq21R5UlDiaoy1abLRRUlDd2qardmzZrqU7du3Wzw4MH28ccfb/Xx/X6/G+ZUlWvAgAHVl3fv3t1OPfVUtyCkoKDAWtKECROsrKzMrrrqKktI2Pzn+oILLnDVw7fffnuL+zz33HOuWnfRRRe5qqJ3v3Xr1tnEiRPda9+4cWP1a1+7dq2rjGrrlmXLltV4rAsvvLC670RVS/XDokWL3NdelVNVwvLy8hZ97QCajmFZAGFz//33uy1QkpKSrGvXrjZ06NAaIUZ0Xa9evRo0pKv5aJpLtjUKMMFg0AW5utS3SEPDt8XFxa6NtWllq0Kj5u1pblxL8UJU7edMSUlxAdO73qO5iqeffrqdcMIJbqg51Ny5c91r15C0TnXRMGtosO7Tp0+N6zVEK+vXr3fn++yzjx133HFu2Piuu+5yw9MKvwq7mh8IIDwIdwDCZpdddqlz/7dQCgm1A19TKYCpEvXuu++6OWi1NWduXCRQFVEnbSejhQ6hfettG/Ob3/zGVerqMmjQoBpf19VHopAo6suXX37ZzWl888037f3333eLKf75z3+6y6K9P4FoRbgDEBMGDhzowoWGH7dWvdNt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ajyfwuLll1/uTtnZ2Zabm2t//OMfLRjcPIFflambbrrJPZZenx7v/vvvr/E4+fn5dv7551vnzp2tffv2tt9++9kPP/xQ4zaqSHbt2tWysrLsvPPOcwG1PmPGjLE77rij+uujjz7aBVavX5cuXepe99y5c93X//73v23w4MHu9et5jj/+eHf52WefbZ9++qn961//qq66qc9Cg1y3bt1qnPQ8nTp1qv5ar6v2bXV9WyitiJ4JyJvmTbE1b91hWTseat3Pu9+FqY1TXreCqW9W32bjd+/Y+k+fsA57nWrdz/u3ddjzVFv34YNWPPebbT5+zmFXWa/Lnqo+ZQzZvfq6te/eY2l9R1n3s/9lgdJiK/jqxerrCr59zVJ7jSDYAWEW7sVh3ntxS4yseO+933//ffXj1kXv3bqd3ifRjHD34osv2rBhw2zo0KF2+umn26OPPlojrNxwww0usCiMiILKl19+aU888YSrpM2bN88OOeQQO+644+zHH390oUlhTwFoa3S/e+65x3766Sf3OBMnTrTrrruuxm2Ki4vtH//4hz3yyCPudl26dNnicRTWFF4mT57svp40aZINGTLEteWbb76pDkSq5uk16ORRte/Xv/61zZw50w4++GB329GjR9vbb79tM2bMsAsvvNAN43777bc1nlPtTUpKcpcrACmoqo2hbr/9dtthhx1c0PSe58MPP6y+/oQTTrC8vDx79913berUqbbzzjvb/vvvb+vWrav+nuiX6W9/+5tNmTLFDT8rjNVHQdULtPr+qS/0y6PvhSiwKWgOGjTIPaYCuIL77Nmz7b333rNx48a52+k17b777nbBBRfYihUr3EkBPFpEU+Wu8KePLWPwbpa102GW3KGbZQwca+13O8EKvnml+newaMZEF/4yh49zt1Hlrd0OB1vB169s8/ETUjMtsV3H6pMvaXP1tHztUsva4WBL7tTTPWb52iWVl+evtMIfP7AOezOFAa2rIn+lLbrjGFdlrjz9yopmf1H/fSoqbPFdJ4bc5wjLD/lgUrFhjS267cjq61a9+Kca919yz2nuOaOFvwXCnf7m154mo6KBCgItHaI0etOxY8caz6VRGxV/VKTR+8n2229f72Psscce7nYqoDQmVC6sNXVIr1EjRyoenXTSSa7A4IXLhtBt//e//1lbTn9q0XCnoViFOlFI27BhgwsCHs3F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",
      "text/plain": [
       "<Figure size 2000x500 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "#now we can proceed to create pie chart with piet dataframe\n",
    "\n",
    "#creating a line chart using the top30 data\n",
    "plt.figure(figsize=(20,5))\n",
    "plt.pie(piet['price'], labels= piet['name'],autopct='%5.1f%%')\n",
    "plt.title('Price of Tokens')\n",
    "plt.savefig('pie_chart.png')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "id": "dd56222c-0e46-4ea9-a086-54f725adc564",
   "metadata": {},
   "outputs": [],
   "source": [
    "#and thats the end of the assignment"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.14.3"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
