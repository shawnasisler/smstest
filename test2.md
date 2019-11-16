 "cells": [
  {
   "cell_type": "code",
   "execution_count": 7,
   "metadata": {},
   "outputs": [],
   "source": [
    "def add(x, y):\n",
    "    \"\"\"Add Function\"\"\"\n",
    "    return x + y\n",
    "\n",
    "def subtract(x, y):\n",
    "    \"\"\"Subtract Function\"\"\"\n",
    "    return x - y\n",
    "\n",
    "def multiply(x, y):\n",
    "    \"\"\"Multiply Functions\"\"\"\n",
    "    return x * y\n",
    "\n",
    "def divide(x, y):\n",
    "    \"\"\"Divide Function\"\"\"\n",
    "    if y == 0:\n",
    "        raise ValueError('Can not divide by zero!')\n",
    "    return x/y"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "metadata": {},
   "outputs": [],
   "source": [
    "import unittest\n",
    "\n",
    "class TestCalc(unittest.TestCase):\n",
    "    \n",
    "    def test_add(self):\n",
    "        result = add(10,5)\n",
    "        self.assertEqual(result, 15)\n",
    "\n",
    "    def test_subtract(self):\n",
    "        result = subtract(10,5)\n",
    "        self.assertEqual(result, 5)\n",
    "\n",
    "    def test_multiply(self):\n",
    "        result = multiply(10,5)\n",
    "        self.assertEqual(result, 50)\n",
    "\n",
    "    def test_divide(self):\n",
    "        result = divide(10,5)\n",
    "        self.assertEqual(result, 2)\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "metadata": {},
   "outputs": [
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "test_add (__main__.TestCalc) ... ok\n",
      "test_divide (__main__.TestCalc) ... ok\n",
      "test_multiply (__main__.TestCalc) ... ok\n",
      "test_subtract (__main__.TestCalc) ... ok\n",
      "\n",
      "----------------------------------------------------------------------\n",
      "Ran 4 tests in 0.004s\n",
      "\n",
      "OK\n"
     ]
    },
    {
     "data": {
      "text/plain": [
       "<unittest.main.TestProgram at 0x11041269630>"
      ]
     },
     "execution_count": 11,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "unittest.main(argv=[''], verbosity=2, exit=False)"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
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
   "version": "3.7.3"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}