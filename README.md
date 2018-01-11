# Pandas-Homework
{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "import pandas as pd\n",
    "import os"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 323,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "academy_file = os.path.join(\"schools_complete.csv\")\n",
    "students_file = os.path.join(\"students_complete.csv\")\n",
    "academy_df = pd.read_csv(academy_file)\n",
    "students_df = pd.read_csv(students_file)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Student ID</th>\n",
       "      <th>name</th>\n",
       "      <th>gender</th>\n",
       "      <th>grade</th>\n",
       "      <th>school</th>\n",
       "      <th>reading_score</th>\n",
       "      <th>math_score</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>0</td>\n",
       "      <td>Paul Bradley</td>\n",
       "      <td>M</td>\n",
       "      <td>9th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>66</td>\n",
       "      <td>79</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>1</td>\n",
       "      <td>Victor Smith</td>\n",
       "      <td>M</td>\n",
       "      <td>12th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>94</td>\n",
       "      <td>61</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>2</td>\n",
       "      <td>Kevin Rodriguez</td>\n",
       "      <td>M</td>\n",
       "      <td>12th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>90</td>\n",
       "      <td>60</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>3</td>\n",
       "      <td>Dr. Richard Scott</td>\n",
       "      <td>M</td>\n",
       "      <td>12th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>67</td>\n",
       "      <td>58</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>4</td>\n",
       "      <td>Bonnie Ray</td>\n",
       "      <td>F</td>\n",
       "      <td>9th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>97</td>\n",
       "      <td>84</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   Student ID               name gender grade             school  \\\n",
       "0           0       Paul Bradley      M   9th  Huang High School   \n",
       "1           1       Victor Smith      M  12th  Huang High School   \n",
       "2           2    Kevin Rodriguez      M  12th  Huang High School   \n",
       "3           3  Dr. Richard Scott      M  12th  Huang High School   \n",
       "4           4         Bonnie Ray      F   9th  Huang High School   \n",
       "\n",
       "   reading_score  math_score  \n",
       "0             66          79  \n",
       "1             94          61  \n",
       "2             90          60  \n",
       "3             67          58  \n",
       "4             97          84  "
      ]
     },
     "execution_count": 6,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "students_df.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>School ID</th>\n",
       "      <th>name</th>\n",
       "      <th>type</th>\n",
       "      <th>size</th>\n",
       "      <th>budget</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>0</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>District</td>\n",
       "      <td>2917</td>\n",
       "      <td>1910635</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>1</td>\n",
       "      <td>Figueroa High School</td>\n",
       "      <td>District</td>\n",
       "      <td>2949</td>\n",
       "      <td>1884411</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>2</td>\n",
       "      <td>Shelton High School</td>\n",
       "      <td>Charter</td>\n",
       "      <td>1761</td>\n",
       "      <td>1056600</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>3</td>\n",
       "      <td>Hernandez High School</td>\n",
       "      <td>District</td>\n",
       "      <td>4635</td>\n",
       "      <td>3022020</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>4</td>\n",
       "      <td>Griffin High School</td>\n",
       "      <td>Charter</td>\n",
       "      <td>1468</td>\n",
       "      <td>917500</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   School ID                   name      type  size   budget\n",
       "0          0      Huang High School  District  2917  1910635\n",
       "1          1   Figueroa High School  District  2949  1884411\n",
       "2          2    Shelton High School   Charter  1761  1056600\n",
       "3          3  Hernandez High School  District  4635  3022020\n",
       "4          4    Griffin High School   Charter  1468   917500"
      ]
     },
     "execution_count": 7,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "academy_df.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "School ID     int64\n",
       "name         object\n",
       "type         object\n",
       "size          int64\n",
       "budget        int64\n",
       "dtype: object"
      ]
     },
     "execution_count": 8,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "academy_df.dtypes"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "<bound method NDFrame.describe of     School ID                   name      type  size   budget\n",
       "0           0      Huang High School  District  2917  1910635\n",
       "1           1   Figueroa High School  District  2949  1884411\n",
       "2           2    Shelton High School   Charter  1761  1056600\n",
       "3           3  Hernandez High School  District  4635  3022020\n",
       "4           4    Griffin High School   Charter  1468   917500\n",
       "5           5     Wilson High School   Charter  2283  1319574\n",
       "6           6    Cabrera High School   Charter  1858  1081356\n",
       "7           7     Bailey High School  District  4976  3124928\n",
       "8           8     Holden High School   Charter   427   248087\n",
       "9           9       Pena High School   Charter   962   585858\n",
       "10         10     Wright High School   Charter  1800  1049400\n",
       "11         11  Rodriguez High School  District  3999  2547363\n",
       "12         12    Johnson High School  District  4761  3094650\n",
       "13         13       Ford High School  District  2739  1763916\n",
       "14         14     Thomas High School   Charter  1635  1043130>"
      ]
     },
     "execution_count": 9,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "academy_df.describe"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Pena High School         1\n",
       "Shelton High School      1\n",
       "Huang High School        1\n",
       "Holden High School       1\n",
       "Ford High School         1\n",
       "Rodriguez High School    1\n",
       "Cabrera High School      1\n",
       "Wright High School       1\n",
       "Griffin High School      1\n",
       "Wilson High School       1\n",
       "Figueroa High School     1\n",
       "Johnson High School      1\n",
       "Hernandez High School    1\n",
       "Thomas High School       1\n",
       "Bailey High School       1\n",
       "Name: name, dtype: int64"
      ]
     },
     "execution_count": 10,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "academy_df[\"name\"].value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "15"
      ]
     },
     "execution_count": 11,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "total_schools = academy_df[\"name\"].count()\n",
    "total_schools"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 106,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Student ID        int64\n",
       "name             object\n",
       "gender           object\n",
       "grade            object\n",
       "school           object\n",
       "reading_score     int64\n",
       "math_score        int64\n",
       "dtype: object"
      ]
     },
     "execution_count": 106,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "students_df.dtypes"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Bailey High School       4976\n",
       "Johnson High School      4761\n",
       "Hernandez High School    4635\n",
       "Rodriguez High School    3999\n",
       "Figueroa High School     2949\n",
       "Huang High School        2917\n",
       "Ford High School         2739\n",
       "Wilson High School       2283\n",
       "Cabrera High School      1858\n",
       "Wright High School       1800\n",
       "Shelton High School      1761\n",
       "Thomas High School       1635\n",
       "Griffin High School      1468\n",
       "Pena High School          962\n",
       "Holden High School        427\n",
       "Name: school, dtype: int64"
      ]
     },
     "execution_count": 12,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "students_df[\"school\"].value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "39170"
      ]
     },
     "execution_count": 13,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "total_students = students_df[\"name\"].count()\n",
    "total_students"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "24649428"
      ]
     },
     "execution_count": 14,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "total_budget = academy_df[\"budget\"].sum()\n",
    "total_budget"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "3093857"
      ]
     },
     "execution_count": 15,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "total_math_score = students_df[\"math_score\"].sum()\n",
    "total_math_score"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "78.985371457748272"
      ]
     },
     "execution_count": 16,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "average_math_score = (total_math_score / total_students)\n",
    "average_math_score"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 17,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "3207155"
      ]
     },
     "execution_count": 17,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "total_reading_score = students_df[\"reading_score\"].sum()\n",
    "total_reading_score"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 18,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "81.877840183814143"
      ]
     },
     "execution_count": 18,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "average_reading_score = (total_reading_score / total_students)\n",
    "average_reading_score"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(39170, 7)"
      ]
     },
     "execution_count": 19,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "students_df.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "bool"
      ]
     },
     "execution_count": 20,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "type(False)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 21,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# Considering passing grade is >=70\n",
    "booleans = []\n",
    "for length in students_df.reading_score:\n",
    "    if length >= 70:\n",
    "        booleans.append(True)\n",
    "    else:\n",
    "        booleans.append(False)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 22,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "[False, True, True, False, True, True, True, True, True, True]"
      ]
     },
     "execution_count": 22,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "booleans[0:10]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 23,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "39170"
      ]
     },
     "execution_count": 23,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "len(booleans)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 24,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0    False\n",
       "1     True\n",
       "2     True\n",
       "3    False\n",
       "4     True\n",
       "dtype: bool"
      ]
     },
     "execution_count": 24,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "passed_fail_reading = pd.Series(booleans)\n",
    "passed_fail_reading.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 25,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Student ID</th>\n",
       "      <th>name</th>\n",
       "      <th>gender</th>\n",
       "      <th>grade</th>\n",
       "      <th>school</th>\n",
       "      <th>reading_score</th>\n",
       "      <th>math_score</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>1</td>\n",
       "      <td>Victor Smith</td>\n",
       "      <td>M</td>\n",
       "      <td>12th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>94</td>\n",
       "      <td>61</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>2</td>\n",
       "      <td>Kevin Rodriguez</td>\n",
       "      <td>M</td>\n",
       "      <td>12th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>90</td>\n",
       "      <td>60</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>4</td>\n",
       "      <td>Bonnie Ray</td>\n",
       "      <td>F</td>\n",
       "      <td>9th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>97</td>\n",
       "      <td>84</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>5</th>\n",
       "      <td>5</td>\n",
       "      <td>Bryan Miranda</td>\n",
       "      <td>M</td>\n",
       "      <td>9th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>94</td>\n",
       "      <td>94</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>6</th>\n",
       "      <td>6</td>\n",
       "      <td>Sheena Carter</td>\n",
       "      <td>F</td>\n",
       "      <td>11th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>82</td>\n",
       "      <td>80</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   Student ID             name gender grade             school  reading_score  \\\n",
       "1           1     Victor Smith      M  12th  Huang High School             94   \n",
       "2           2  Kevin Rodriguez      M  12th  Huang High School             90   \n",
       "4           4       Bonnie Ray      F   9th  Huang High School             97   \n",
       "5           5    Bryan Miranda      M   9th  Huang High School             94   \n",
       "6           6    Sheena Carter      F  11th  Huang High School             82   \n",
       "\n",
       "   math_score  \n",
       "1          61  \n",
       "2          60  \n",
       "4          84  \n",
       "5          94  \n",
       "6          80  "
      ]
     },
     "execution_count": 25,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "students_df[passed_fail_reading].head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 26,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0    False\n",
       "1     True\n",
       "2     True\n",
       "3    False\n",
       "4     True\n",
       "Name: reading_score, dtype: bool"
      ]
     },
     "execution_count": 26,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "passed_fail_reading = students_df.reading_score >= 70\n",
    "passed_fail_reading.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 27,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     33610\n",
       "False     5560\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 27,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "passed_fail_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 28,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# Considering passing grade is >=70\n",
    "booleans_2 = []\n",
    "for length in students_df.math_score:\n",
    "    if length >= 70:\n",
    "        booleans_2.append(True)\n",
    "    else:\n",
    "        booleans_2.append(False)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 29,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "[True, False, False, False, True, True, True, False, True, True]"
      ]
     },
     "execution_count": 29,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "booleans_2[0:10]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 30,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "39170"
      ]
     },
     "execution_count": 30,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "len(booleans_2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 31,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0     True\n",
       "1    False\n",
       "2    False\n",
       "3    False\n",
       "4     True\n",
       "dtype: bool"
      ]
     },
     "execution_count": 31,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "passed_fail_math = pd.Series(booleans_2)\n",
    "passed_fail_math.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 32,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0     True\n",
       "1    False\n",
       "2    False\n",
       "3    False\n",
       "4     True\n",
       "Name: math_score, dtype: bool"
      ]
     },
     "execution_count": 32,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "passed_fail_math = students_df.math_score >= 70\n",
    "passed_fail_math.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 33,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     29370\n",
       "False     9800\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 33,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "passed_fail_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 34,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "85.805463364820014"
      ]
     },
     "execution_count": 34,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "percentage_reading_pass = (33610 / total_students) * 100\n",
    "percentage_reading_pass"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 35,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "74.980852693387803"
      ]
     },
     "execution_count": 35,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "percentage_math_pass = (29370 / total_students) * 100\n",
    "percentage_math_pass"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 36,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "80.393158029103915"
      ]
     },
     "execution_count": 36,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "overall_rate = (percentage_reading_pass + percentage_math_pass) / 2\n",
    "overall_rate"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 37,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Total Schools</th>\n",
       "      <th>Total Students</th>\n",
       "      <th>Total Budget</th>\n",
       "      <th>Average Math Score</th>\n",
       "      <th>Average Reading Score</th>\n",
       "      <th>% Passing Math</th>\n",
       "      <th>% Passing Reading</th>\n",
       "      <th>Overall Passing Rate</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>15</td>\n",
       "      <td>39170</td>\n",
       "      <td>$24,649,428.00</td>\n",
       "      <td>78.985371</td>\n",
       "      <td>81.87784</td>\n",
       "      <td>74.980853</td>\n",
       "      <td>85.805463</td>\n",
       "      <td>80.393158</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   Total Schools  Total Students    Total Budget  Average Math Score  \\\n",
       "0             15           39170  $24,649,428.00           78.985371   \n",
       "\n",
       "   Average Reading Score  % Passing Math  % Passing Reading  \\\n",
       "0               81.87784       74.980853          85.805463   \n",
       "\n",
       "   Overall Passing Rate  \n",
       "0             80.393158  "
      ]
     },
     "execution_count": 37,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "district_summary = pd.DataFrame({\"Total Schools\" :[total_schools], \"Total Students\" :[total_students], \"Total Budget\" :[\"${:,.2f}\".format(total_budget)], \n",
    "                                 \"Average Math Score\" :[average_math_score],\n",
    "                                 \"Average Reading Score\" :[average_reading_score], \"% Passing Math\" :[percentage_math_pass],\n",
    "                                 \"% Passing Reading\" :[percentage_reading_pass], \"Overall Passing Rate\" :[overall_rate]},\n",
    "                                columns=[\"Total Schools\", \"Total Students\", \"Total Budget\", \"Average Math Score\", \"Average Reading Score\", \n",
    "                                 \"% Passing Math\", \"% Passing Reading\", \"Overall Passing Rate\"])\n",
    "district_summary"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 38,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "<bound method NDFrame.describe of     School ID                   name      type  size   budget\n",
       "0           0      Huang High School  District  2917  1910635\n",
       "1           1   Figueroa High School  District  2949  1884411\n",
       "2           2    Shelton High School   Charter  1761  1056600\n",
       "3           3  Hernandez High School  District  4635  3022020\n",
       "4           4    Griffin High School   Charter  1468   917500\n",
       "5           5     Wilson High School   Charter  2283  1319574\n",
       "6           6    Cabrera High School   Charter  1858  1081356\n",
       "7           7     Bailey High School  District  4976  3124928\n",
       "8           8     Holden High School   Charter   427   248087\n",
       "9           9       Pena High School   Charter   962   585858\n",
       "10         10     Wright High School   Charter  1800  1049400\n",
       "11         11  Rodriguez High School  District  3999  2547363\n",
       "12         12    Johnson High School  District  4761  3094650\n",
       "13         13       Ford High School  District  2739  1763916\n",
       "14         14     Thomas High School   Charter  1635  1043130>"
      ]
     },
     "execution_count": 38,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#School Summary - Huang High School(Detailed)\n",
    "academy_df.describe"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 39,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>School ID</th>\n",
       "      <th>name</th>\n",
       "      <th>type</th>\n",
       "      <th>size</th>\n",
       "      <th>budget</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>0</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>District</td>\n",
       "      <td>2917</td>\n",
       "      <td>1910635</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   School ID               name      type  size   budget\n",
       "0          0  Huang High School  District  2917  1910635"
      ]
     },
     "execution_count": 39,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_hs_academy = academy_df[academy_df[\"name\"] == \"Huang High School\"]\n",
    "huang_hs_academy"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 40,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "1910635"
      ]
     },
     "execution_count": 40,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_total_budget = huang_hs_academy[\"budget\"].sum()\n",
    "huang_total_budget"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 41,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'District'"
      ]
     },
     "execution_count": 41,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_school_type = huang_hs_academy[\"type\"].sum()\n",
    "huang_school_type"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 42,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Student ID</th>\n",
       "      <th>name</th>\n",
       "      <th>gender</th>\n",
       "      <th>grade</th>\n",
       "      <th>school</th>\n",
       "      <th>reading_score</th>\n",
       "      <th>math_score</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>0</td>\n",
       "      <td>Paul Bradley</td>\n",
       "      <td>M</td>\n",
       "      <td>9th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>66</td>\n",
       "      <td>79</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>1</td>\n",
       "      <td>Victor Smith</td>\n",
       "      <td>M</td>\n",
       "      <td>12th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>94</td>\n",
       "      <td>61</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>2</td>\n",
       "      <td>Kevin Rodriguez</td>\n",
       "      <td>M</td>\n",
       "      <td>12th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>90</td>\n",
       "      <td>60</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>3</td>\n",
       "      <td>Dr. Richard Scott</td>\n",
       "      <td>M</td>\n",
       "      <td>12th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>67</td>\n",
       "      <td>58</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>4</td>\n",
       "      <td>Bonnie Ray</td>\n",
       "      <td>F</td>\n",
       "      <td>9th</td>\n",
       "      <td>Huang High School</td>\n",
       "      <td>97</td>\n",
       "      <td>84</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   Student ID               name gender grade             school  \\\n",
       "0           0       Paul Bradley      M   9th  Huang High School   \n",
       "1           1       Victor Smith      M  12th  Huang High School   \n",
       "2           2    Kevin Rodriguez      M  12th  Huang High School   \n",
       "3           3  Dr. Richard Scott      M  12th  Huang High School   \n",
       "4           4         Bonnie Ray      F   9th  Huang High School   \n",
       "\n",
       "   reading_score  math_score  \n",
       "0             66          79  \n",
       "1             94          61  \n",
       "2             90          60  \n",
       "3             67          58  \n",
       "4             97          84  "
      ]
     },
     "execution_count": 42,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_hs_students = students_df[students_df[\"school\"] == \"Huang High School\"]\n",
    "huang_hs_students.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 43,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "2917"
      ]
     },
     "execution_count": 43,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_total_students = huang_hs_students[\"name\"].count()\n",
    "huang_total_students"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 44,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "1910635"
      ]
     },
     "execution_count": 44,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_total_budget"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 45,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0     True\n",
       "1    False\n",
       "2    False\n",
       "3    False\n",
       "4     True\n",
       "Name: math_score, dtype: bool"
      ]
     },
     "execution_count": 45,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_hs_students_math = huang_hs_students.math_score >= 70\n",
    "huang_hs_students_math.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 46,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     1916\n",
       "False    1001\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 46,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 47,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "223528"
      ]
     },
     "execution_count": 47,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_hs_students_totalmath = huang_hs_students[\"math_score\"].sum()\n",
    "huang_hs_students_totalmath"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 48,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0    False\n",
       "1     True\n",
       "2     True\n",
       "3    False\n",
       "4     True\n",
       "Name: reading_score, dtype: bool"
      ]
     },
     "execution_count": 48,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_hs_students_reading = huang_hs_students.reading_score >= 70\n",
    "huang_hs_students_reading.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 49,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     2372\n",
       "False     545\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 49,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 50,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "236810"
      ]
     },
     "execution_count": 50,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_hs_students_totalreading = huang_hs_students[\"reading_score\"].sum()\n",
    "huang_hs_students_totalreading "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 51,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "655.0"
      ]
     },
     "execution_count": 51,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "per_stu_budget = huang_total_budget / huang_total_students\n",
    "per_stu_budget"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 52,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "76.629413781282139"
      ]
     },
     "execution_count": 52,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_average_math_score = (huang_hs_students_totalmath / huang_total_students)\n",
    "huang_average_math_score"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 53,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "81.182721974631477"
      ]
     },
     "execution_count": 53,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_average_reading_score = (huang_hs_students_totalreading / huang_total_students)\n",
    "huang_average_reading_score"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 56,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "81.316420980459384"
      ]
     },
     "execution_count": 56,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "per_huang_pass_reading = (2372 / huang_total_students) * 100\n",
    "per_huang_pass_reading"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 57,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "65.683921837504286"
      ]
     },
     "execution_count": 57,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "per_huang_pass_math = (1916 / huang_total_students) * 100\n",
    "per_huang_pass_math"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 58,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "73.500171408981828"
      ]
     },
     "execution_count": 58,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "huang_overall = (per_huang_pass_math + per_huang_pass_reading) / 2\n",
    "huang_overall"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 78,
   "metadata": {},
   "outputs": [],
   "source": [
    "# School Summary - Figueroa High School \n",
    "figueroa_hs_academy = academy_df[academy_df[\"name\"] == \"Figueroa High School\"]\n",
    "figueroa_total_budget = figueroa_hs_academy[\"budget\"].sum()\n",
    "figueroa_school_type = figueroa_hs_academy[\"type\"].sum()\n",
    "figueroa_hs_students = students_df[students_df[\"school\"] == \"Figueroa High School\"]\n",
    "figueroa_total_students = figueroa_hs_students[\"name\"].count()\n",
    "figueroa_hs_students_math = figueroa_hs_students.math_score >= 70\n",
    "figueroa_hs_students_math.value_counts()\n",
    "figueroa_hs_students_totalmath = figueroa_hs_students[\"math_score\"].sum()\n",
    "figueroa_hs_students_reading = figueroa_hs_students.reading_score >= 70\n",
    "figueroa_hs_students_reading.value_counts()\n",
    "figueroa_hs_students_totalreading = figueroa_hs_students[\"reading_score\"].sum()\n",
    "per_fi_stu_budget = figueroa_total_budget / figueroa_total_students\n",
    "figueroa_average_math_score = (figueroa_hs_students_totalmath / figueroa_total_students)\n",
    "figueroa_average_reading_score = (figueroa_hs_students_totalreading / figueroa_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 79,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     1946\n",
       "False    1003\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 79,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "figueroa_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 80,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     2381\n",
       "False     568\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 80,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "figueroa_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 81,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_figueroa_pass_reading = (2381 / figueroa_total_students) * 100\n",
    "per_figueroa_pass_math = (1946 / figueroa_total_students) * 100\n",
    "figueroa_overall = (per_figueroa_pass_math + per_figueroa_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 82,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Shelton High School\n",
    "shelton_hs_academy = academy_df[academy_df[\"name\"] == \"Shelton High School\"]\n",
    "shelton_total_budget = shelton_hs_academy[\"budget\"].sum()\n",
    "shelton_school_type = shelton_hs_academy[\"type\"].sum()\n",
    "shelton_hs_students = students_df[students_df[\"school\"] == \"Shelton High School\"]\n",
    "shelton_total_students = shelton_hs_students[\"name\"].count()\n",
    "shelton_hs_students_math = shelton_hs_students.math_score >= 70\n",
    "shelton_hs_students_math.value_counts()\n",
    "shelton_hs_students_totalmath = shelton_hs_students[\"math_score\"].sum()\n",
    "shelton_hs_students_reading = shelton_hs_students.reading_score >= 70\n",
    "shelton_hs_students_reading.value_counts()\n",
    "shelton_hs_students_totalreading = shelton_hs_students[\"reading_score\"].sum()\n",
    "per_sh_stu_budget = shelton_total_budget / shelton_total_students\n",
    "shelton_average_math_score = (shelton_hs_students_totalmath / shelton_total_students)\n",
    "shelton_average_reading_score = (shelton_hs_students_totalreading / shelton_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 83,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     1653\n",
       "False     108\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 83,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "shelton_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 84,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     1688\n",
       "False      73\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 84,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "shelton_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 85,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_shelton_pass_reading = (1688 / shelton_total_students) * 100\n",
    "per_shelton_pass_math = (1653 / shelton_total_students) * 100\n",
    "shelton_overall = (per_shelton_pass_math + per_shelton_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 86,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Hernandez High School\n",
    "hernandez_hs_academy = academy_df[academy_df[\"name\"] == \"Hernandez High School\"]\n",
    "hernandez_total_budget = hernandez_hs_academy[\"budget\"].sum()\n",
    "hernandez_school_type = hernandez_hs_academy[\"type\"].sum()\n",
    "hernandez_hs_students = students_df[students_df[\"school\"] == \"Hernandez High School\"]\n",
    "hernandez_total_students = hernandez_hs_students[\"name\"].count()\n",
    "hernandez_hs_students_math = hernandez_hs_students.math_score >= 70\n",
    "hernandez_hs_students_math.value_counts()\n",
    "hernandez_hs_students_totalmath = hernandez_hs_students[\"math_score\"].sum()\n",
    "hernandez_hs_students_reading = hernandez_hs_students.reading_score >= 70\n",
    "hernandez_hs_students_reading.value_counts()\n",
    "hernandez_hs_students_totalreading = hernandez_hs_students[\"reading_score\"].sum()\n",
    "per_hz_stu_budget = hernandez_total_budget / hernandez_total_students\n",
    "hernandez_average_math_score = (hernandez_hs_students_totalmath / hernandez_total_students)\n",
    "hernandez_average_reading_score = (hernandez_hs_students_totalreading / hernandez_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 87,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     3094\n",
       "False    1541\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 87,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "hernandez_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 88,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     3748\n",
       "False     887\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 88,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "hernandez_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 89,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_hernandez_pass_reading = (3748 / hernandez_total_students) * 100\n",
    "per_hernandez_pass_math = (3094 / hernandez_total_students) * 100\n",
    "hernandez_overall = (per_hernandez_pass_math + per_hernandez_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 90,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Griffin High School\n",
    "griffin_hs_academy = academy_df[academy_df[\"name\"] == \"Griffin High School\"]\n",
    "griffin_total_budget = griffin_hs_academy[\"budget\"].sum()\n",
    "griffin_school_type = griffin_hs_academy[\"type\"].sum()\n",
    "griffin_hs_students = students_df[students_df[\"school\"] == \"Griffin High School\"]\n",
    "griffin_total_students = griffin_hs_students[\"name\"].count()\n",
    "griffin_hs_students_math = griffin_hs_students.math_score >= 70\n",
    "griffin_hs_students_math.value_counts()\n",
    "griffin_hs_students_totalmath = griffin_hs_students[\"math_score\"].sum()\n",
    "griffin_hs_students_reading = griffin_hs_students.reading_score >= 70\n",
    "griffin_hs_students_reading.value_counts()\n",
    "griffin_hs_students_totalreading = griffin_hs_students[\"reading_score\"].sum()\n",
    "per_gr_stu_budget = griffin_total_budget / griffin_total_students\n",
    "griffin_average_math_score = (griffin_hs_students_totalmath / griffin_total_students)\n",
    "griffin_average_reading_score = (griffin_hs_students_totalreading / griffin_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 91,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     1371\n",
       "False      97\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 91,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "griffin_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 92,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     1426\n",
       "False      42\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 92,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "griffin_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 93,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_griffin_pass_reading = (1426 / griffin_total_students) * 100\n",
    "per_griffin_pass_math = (1371 / griffin_total_students) * 100\n",
    "griffin_overall = (per_griffin_pass_math + per_griffin_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 94,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Wilson High School\n",
    "wilson_hs_academy = academy_df[academy_df[\"name\"] == \"Wilson High School\"]\n",
    "wilson_total_budget = wilson_hs_academy[\"budget\"].sum()\n",
    "wilson_school_type = wilson_hs_academy[\"type\"].sum()\n",
    "wilson_hs_students = students_df[students_df[\"school\"] == \"Wilson High School\"]\n",
    "wilson_total_students = wilson_hs_students[\"name\"].count()\n",
    "wilson_hs_students_math = wilson_hs_students.math_score >= 70\n",
    "wilson_hs_students_math.value_counts()\n",
    "wilson_hs_students_totalmath = wilson_hs_students[\"math_score\"].sum()\n",
    "wilson_hs_students_reading = wilson_hs_students.reading_score >= 70\n",
    "wilson_hs_students_reading.value_counts()\n",
    "wilson_hs_students_totalreading = wilson_hs_students[\"reading_score\"].sum()\n",
    "per_wil_stu_budget = wilson_total_budget / wilson_total_students\n",
    "wilson_average_math_score = (wilson_hs_students_totalmath / wilson_total_students)\n",
    "wilson_average_reading_score = (wilson_hs_students_totalreading / wilson_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 95,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     2143\n",
       "False     140\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 95,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "wilson_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 96,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     2204\n",
       "False      79\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 96,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "wilson_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 410,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_wilson_pass_reading = (2204 / wilson_total_students) * 100\n",
    "per_wilson_pass_math = (2143 / wilson_total_students) * 100\n",
    "wilson_overall = (per_wilson_pass_math + per_wilson_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 98,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Cabrera High School \n",
    "cabrera_hs_academy = academy_df[academy_df[\"name\"] == \"Cabrera High School\"]\n",
    "cabrera_total_budget = cabrera_hs_academy[\"budget\"].sum()\n",
    "cabrera_school_type = cabrera_hs_academy[\"type\"].sum()\n",
    "cabrera_hs_students = students_df[students_df[\"school\"] == \"Cabrera High School\"]\n",
    "cabrera_total_students = cabrera_hs_students[\"name\"].count()\n",
    "cabrera_hs_students_math = cabrera_hs_students.math_score >= 70\n",
    "cabrera_hs_students_math.value_counts()\n",
    "cabrera_hs_students_totalmath = cabrera_hs_students[\"math_score\"].sum()\n",
    "cabrera_hs_students_reading = cabrera_hs_students.reading_score >= 70\n",
    "cabrera_hs_students_reading.value_counts()\n",
    "cabrera_hs_students_totalreading = cabrera_hs_students[\"reading_score\"].sum()\n",
    "per_ca_stu_budget = cabrera_total_budget / cabrera_total_students\n",
    "cabrera_average_math_score = (cabrera_hs_students_totalmath / cabrera_total_students)\n",
    "cabrera_average_reading_score = (cabrera_hs_students_totalreading / cabrera_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 99,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     1749\n",
       "False     109\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 99,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cabrera_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 100,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     1803\n",
       "False      55\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 100,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cabrera_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 101,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_cabrera_pass_reading = (1803 / cabrera_total_students) * 100\n",
    "per_cabrera_pass_math = (1749 / cabrera_total_students) * 100\n",
    "cabrera_overall = (per_cabrera_pass_math + per_cabrera_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 102,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Bailey High School\n",
    "bailey_hs_academy = academy_df[academy_df[\"name\"] == \"Bailey High School\"]\n",
    "bailey_total_budget = bailey_hs_academy[\"budget\"].sum()\n",
    "bailey_school_type = bailey_hs_academy[\"type\"].sum()\n",
    "bailey_hs_students = students_df[students_df[\"school\"] == \"Bailey High School\"]\n",
    "bailey_total_students = bailey_hs_students[\"name\"].count()\n",
    "bailey_hs_students_math = bailey_hs_students.math_score >= 70\n",
    "bailey_hs_students_math.value_counts()\n",
    "bailey_hs_students_totalmath = bailey_hs_students[\"math_score\"].sum()\n",
    "bailey_hs_students_reading = bailey_hs_students.reading_score >= 70\n",
    "bailey_hs_students_reading.value_counts()\n",
    "bailey_hs_students_totalreading = bailey_hs_students[\"reading_score\"].sum()\n",
    "per_bay_stu_budget = bailey_total_budget / bailey_total_students\n",
    "bailey_average_math_score = (bailey_hs_students_totalmath / bailey_total_students)\n",
    "bailey_average_reading_score = (bailey_hs_students_totalreading / bailey_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 103,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     3318\n",
       "False    1658\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 103,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "bailey_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 104,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     4077\n",
       "False     899\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 104,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "bailey_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 105,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_bailey_pass_reading = (4077 / bailey_total_students) * 100\n",
    "per_bailey_pass_math = (3318 / bailey_total_students) * 100\n",
    "bailey_overall = (per_bailey_pass_math + per_bailey_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 106,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Holden High School\n",
    "holden_hs_academy = academy_df[academy_df[\"name\"] == \"Holden High School\"]\n",
    "holden_total_budget = holden_hs_academy[\"budget\"].sum()\n",
    "holden_school_type = holden_hs_academy[\"type\"].sum()\n",
    "holden_hs_students = students_df[students_df[\"school\"] == \"Holden High School\"]\n",
    "holden_total_students = holden_hs_students[\"name\"].count()\n",
    "holden_hs_students_math = holden_hs_students.math_score >= 70\n",
    "holden_hs_students_math.value_counts()\n",
    "holden_hs_students_totalmath = holden_hs_students[\"math_score\"].sum()\n",
    "holden_hs_students_reading = holden_hs_students.reading_score >= 70\n",
    "holden_hs_students_reading.value_counts()\n",
    "holden_hs_students_totalreading = holden_hs_students[\"reading_score\"].sum()\n",
    "per_hl_stu_budget = holden_total_budget / holden_total_students\n",
    "holden_average_math_score = (holden_hs_students_totalmath / holden_total_students)\n",
    "holden_average_reading_score = (holden_hs_students_totalreading / holden_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 107,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     395\n",
       "False     32\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 107,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "holden_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 108,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     411\n",
       "False     16\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 108,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "holden_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 109,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_holden_pass_reading = (411 / holden_total_students) * 100\n",
    "per_holden_pass_math = (395 / holden_total_students) * 100\n",
    "holden_overall = (per_holden_pass_math + per_holden_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 110,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Pena High School\n",
    "pena_hs_academy = academy_df[academy_df[\"name\"] == \"Pena High School\"]\n",
    "pena_total_budget = pena_hs_academy[\"budget\"].sum()\n",
    "pena_school_type = pena_hs_academy[\"type\"].sum()\n",
    "pena_hs_students = students_df[students_df[\"school\"] == \"Pena High School\"]\n",
    "pena_total_students = pena_hs_students[\"name\"].count()\n",
    "pena_hs_students_math = pena_hs_students.math_score >= 70\n",
    "pena_hs_students_math.value_counts()\n",
    "pena_hs_students_totalmath = pena_hs_students[\"math_score\"].sum()\n",
    "pena_hs_students_reading = pena_hs_students.reading_score >= 70\n",
    "pena_hs_students_reading.value_counts()\n",
    "pena_hs_students_totalreading = pena_hs_students[\"reading_score\"].sum()\n",
    "per_pe_stu_budget = pena_total_budget / pena_total_students\n",
    "pena_average_math_score = (pena_hs_students_totalmath / pena_total_students)\n",
    "pena_average_reading_score = (pena_hs_students_totalreading / pena_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 111,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     910\n",
       "False     52\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 111,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pena_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 112,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     923\n",
       "False     39\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 112,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pena_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 113,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_pena_pass_reading = (923 / pena_total_students) * 100\n",
    "per_pena_pass_math = (910 / pena_total_students) * 100\n",
    "pena_overall = (per_pena_pass_math + per_pena_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 114,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Wright High School\n",
    "wright_hs_academy = academy_df[academy_df[\"name\"] == \"Wright High School\"]\n",
    "wright_total_budget = wright_hs_academy[\"budget\"].sum()\n",
    "wright_school_type = wright_hs_academy[\"type\"].sum()\n",
    "wright_hs_students = students_df[students_df[\"school\"] == \"Wright High School\"]\n",
    "wright_total_students = wright_hs_students[\"name\"].count()\n",
    "wright_hs_students_math = wright_hs_students.math_score >= 70\n",
    "wright_hs_students_math.value_counts()\n",
    "wright_hs_students_totalmath = wright_hs_students[\"math_score\"].sum()\n",
    "wright_hs_students_reading = wright_hs_students.reading_score >= 70\n",
    "wright_hs_students_reading.value_counts()\n",
    "wright_hs_students_totalreading = wright_hs_students[\"reading_score\"].sum()\n",
    "per_wr_stu_budget = wright_total_budget / wright_total_students\n",
    "wright_average_math_score = (wright_hs_students_totalmath / wright_total_students)\n",
    "wright_average_reading_score = (wright_hs_students_totalreading / wright_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 115,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     1680\n",
       "False     120\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 115,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "wright_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 116,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     1739\n",
       "False      61\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 116,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "wright_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 117,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_wright_pass_reading = (1739 / wright_total_students) * 100\n",
    "per_wright_pass_math = (1680 / wright_total_students) * 100\n",
    "wright_overall = (per_wright_pass_math + per_wright_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 118,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Rodriguez High School\n",
    "rodriguez_hs_academy = academy_df[academy_df[\"name\"] == \"Rodriguez High School\"]\n",
    "rodriguez_total_budget = rodriguez_hs_academy[\"budget\"].sum()\n",
    "rodriguez_school_type = rodriguez_hs_academy[\"type\"].sum()\n",
    "rodriguez_hs_students = students_df[students_df[\"school\"] == \"Rodriguez High School\"]\n",
    "rodriguez_total_students = rodriguez_hs_students[\"name\"].count()\n",
    "rodriguez_hs_students_math = rodriguez_hs_students.math_score >= 70\n",
    "rodriguez_hs_students_math.value_counts()\n",
    "rodriguez_hs_students_totalmath = rodriguez_hs_students[\"math_score\"].sum()\n",
    "rodriguez_hs_students_reading = rodriguez_hs_students.reading_score >= 70\n",
    "rodriguez_hs_students_reading.value_counts()\n",
    "rodriguez_hs_students_totalreading = rodriguez_hs_students[\"reading_score\"].sum()\n",
    "per_ro_stu_budget = rodriguez_total_budget / rodriguez_total_students\n",
    "rodriguez_average_math_score = (rodriguez_hs_students_totalmath / rodriguez_total_students)\n",
    "rodriguez_average_reading_score = (rodriguez_hs_students_totalreading / rodriguez_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 119,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     2654\n",
       "False    1345\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 119,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "rodriguez_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 120,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     3208\n",
       "False     791\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 120,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "rodriguez_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 121,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_rodriguez_pass_reading = (3208 / rodriguez_total_students) * 100\n",
    "per_rodriguez_pass_math = (2654 / rodriguez_total_students) * 100\n",
    "rodriguez_overall = (per_rodriguez_pass_math + per_rodriguez_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 122,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Johnson High School\n",
    "johnson_hs_academy = academy_df[academy_df[\"name\"] == \"Johnson High School\"]\n",
    "johnson_total_budget = johnson_hs_academy[\"budget\"].sum()\n",
    "johnson_school_type = johnson_hs_academy[\"type\"].sum()\n",
    "johnson_hs_students = students_df[students_df[\"school\"] == \"Johnson High School\"]\n",
    "johnson_total_students = johnson_hs_students[\"name\"].count()\n",
    "johnson_hs_students_math = johnson_hs_students.math_score >= 70\n",
    "johnson_hs_students_math.value_counts()\n",
    "johnson_hs_students_totalmath = johnson_hs_students[\"math_score\"].sum()\n",
    "johnson_hs_students_reading = johnson_hs_students.reading_score >= 70\n",
    "johnson_hs_students_reading.value_counts()\n",
    "johnson_hs_students_totalreading = johnson_hs_students[\"reading_score\"].sum()\n",
    "per_joh_stu_budget = johnson_total_budget / johnson_total_students\n",
    "johnson_average_math_score = (johnson_hs_students_totalmath / johnson_total_students)\n",
    "johnson_average_reading_score = (johnson_hs_students_totalreading / johnson_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 123,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     3145\n",
       "False    1616\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 123,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "johnson_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 124,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     3867\n",
       "False     894\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 124,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "johnson_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 125,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_johnson_pass_reading = (3867 / johnson_total_students) * 100\n",
    "per_johnson_pass_math = (3145 / johnson_total_students) * 100\n",
    "johnson_overall = (per_johnson_pass_math + per_johnson_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 126,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Ford High School\n",
    "ford_hs_academy = academy_df[academy_df[\"name\"] == \"Ford High School\"]\n",
    "ford_total_budget = ford_hs_academy[\"budget\"].sum()\n",
    "ford_school_type = ford_hs_academy[\"type\"].sum()\n",
    "ford_hs_students = students_df[students_df[\"school\"] == \"Ford High School\"]\n",
    "ford_total_students = ford_hs_students[\"name\"].count()\n",
    "ford_hs_students_math = ford_hs_students.math_score >= 70\n",
    "ford_hs_students_math.value_counts()\n",
    "ford_hs_students_totalmath = ford_hs_students[\"math_score\"].sum()\n",
    "ford_hs_students_reading = ford_hs_students.reading_score >= 70\n",
    "ford_hs_students_reading.value_counts()\n",
    "ford_hs_students_totalreading = ford_hs_students[\"reading_score\"].sum()\n",
    "per_fd_stu_budget = ford_total_budget / ford_total_students\n",
    "ford_average_math_score = (ford_hs_students_totalmath / ford_total_students)\n",
    "ford_average_reading_score = (ford_hs_students_totalreading / ford_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 127,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     1871\n",
       "False     868\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 127,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "ford_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 128,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     2172\n",
       "False     567\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 128,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "ford_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 129,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_ford_pass_reading = (2172 / ford_total_students) * 100\n",
    "per_ford_pass_math = (1871 / ford_total_students) * 100\n",
    "ford_overall = (per_ford_pass_math + per_ford_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 130,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Thomas High School\n",
    "thomas_hs_academy = academy_df[academy_df[\"name\"] == \"Thomas High School\"]\n",
    "thomas_total_budget = thomas_hs_academy[\"budget\"].sum()\n",
    "thomas_school_type = thomas_hs_academy[\"type\"].sum()\n",
    "thomas_hs_students = students_df[students_df[\"school\"] == \"Thomas High School\"]\n",
    "thomas_total_students = thomas_hs_students[\"name\"].count()\n",
    "thomas_hs_students_math = thomas_hs_students.math_score >= 70\n",
    "thomas_hs_students_math.value_counts()\n",
    "thomas_hs_students_totalmath = thomas_hs_students[\"math_score\"].sum()\n",
    "thomas_hs_students_reading = thomas_hs_students.reading_score >= 70\n",
    "thomas_hs_students_reading.value_counts()\n",
    "thomas_hs_students_totalreading = thomas_hs_students[\"reading_score\"].sum()\n",
    "per_tho_stu_budget = thomas_total_budget / thomas_total_students\n",
    "thomas_average_math_score = (thomas_hs_students_totalmath / thomas_total_students)\n",
    "thomas_average_reading_score = (thomas_hs_students_totalreading / thomas_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 131,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     1525\n",
       "False     110\n",
       "Name: math_score, dtype: int64"
      ]
     },
     "execution_count": 131,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "thomas_hs_students_math.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 132,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "True     1591\n",
       "False      44\n",
       "Name: reading_score, dtype: int64"
      ]
     },
     "execution_count": 132,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "thomas_hs_students_reading.value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 133,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "per_thomas_pass_reading = (1591 / thomas_total_students) * 100\n",
    "per_thomas_pass_math = (1525 / thomas_total_students) * 100\n",
    "thomas_overall = (per_thomas_pass_math + per_thomas_pass_reading) / 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 432,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>School Type</th>\n",
       "      <th>Total Students</th>\n",
       "      <th>Total School Budget</th>\n",
       "      <th>Per Student Budget</th>\n",
       "      <th>Average Math Score</th>\n",
       "      <th>Average Reading Score</th>\n",
       "      <th>% Passing Math</th>\n",
       "      <th>% Passing Reading</th>\n",
       "      <th>% Overall Passing Rate</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Huang High School</th>\n",
       "      <td>District</td>\n",
       "      <td>2917</td>\n",
       "      <td>$1,910,635.00</td>\n",
       "      <td>$655.00</td>\n",
       "      <td>76.629414</td>\n",
       "      <td>81.182722</td>\n",
       "      <td>65.683922</td>\n",
       "      <td>81.316421</td>\n",
       "      <td>73.500171</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Figueroa High School</th>\n",
       "      <td>District</td>\n",
       "      <td>2949</td>\n",
       "      <td>$1,884,411.00</td>\n",
       "      <td>$639.00</td>\n",
       "      <td>76.711767</td>\n",
       "      <td>81.158020</td>\n",
       "      <td>65.988471</td>\n",
       "      <td>80.739234</td>\n",
       "      <td>73.363852</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Shelton High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>1761</td>\n",
       "      <td>$1,056,600.00</td>\n",
       "      <td>$600.00</td>\n",
       "      <td>83.359455</td>\n",
       "      <td>83.725724</td>\n",
       "      <td>93.867121</td>\n",
       "      <td>95.854628</td>\n",
       "      <td>94.860875</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Hernandez High School</th>\n",
       "      <td>District</td>\n",
       "      <td>4635</td>\n",
       "      <td>$3,022,020.00</td>\n",
       "      <td>$652.00</td>\n",
       "      <td>77.289752</td>\n",
       "      <td>80.934412</td>\n",
       "      <td>66.752967</td>\n",
       "      <td>80.862999</td>\n",
       "      <td>73.807983</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Griffin High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>1468</td>\n",
       "      <td>$917,500.00</td>\n",
       "      <td>$625.00</td>\n",
       "      <td>83.351499</td>\n",
       "      <td>83.816757</td>\n",
       "      <td>93.392371</td>\n",
       "      <td>97.138965</td>\n",
       "      <td>95.265668</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Wilson High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>2283</td>\n",
       "      <td>$1,319,574.00</td>\n",
       "      <td>$578.00</td>\n",
       "      <td>83.274201</td>\n",
       "      <td>83.989488</td>\n",
       "      <td>93.867718</td>\n",
       "      <td>96.539641</td>\n",
       "      <td>95.203679</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Cabrera High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>1858</td>\n",
       "      <td>$1,081,356.00</td>\n",
       "      <td>$582.00</td>\n",
       "      <td>83.061895</td>\n",
       "      <td>83.975780</td>\n",
       "      <td>94.133477</td>\n",
       "      <td>97.039828</td>\n",
       "      <td>95.586652</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Bailey High School</th>\n",
       "      <td>District</td>\n",
       "      <td>4976</td>\n",
       "      <td>$3,124,928.00</td>\n",
       "      <td>$628.00</td>\n",
       "      <td>77.048432</td>\n",
       "      <td>81.033963</td>\n",
       "      <td>66.680064</td>\n",
       "      <td>81.933280</td>\n",
       "      <td>74.306672</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Holden High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>427</td>\n",
       "      <td>$248,087.00</td>\n",
       "      <td>$581.00</td>\n",
       "      <td>83.803279</td>\n",
       "      <td>83.814988</td>\n",
       "      <td>92.505855</td>\n",
       "      <td>96.252927</td>\n",
       "      <td>94.379391</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Pena High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>962</td>\n",
       "      <td>$585,858.00</td>\n",
       "      <td>$609.00</td>\n",
       "      <td>83.839917</td>\n",
       "      <td>84.044699</td>\n",
       "      <td>94.594595</td>\n",
       "      <td>95.945946</td>\n",
       "      <td>95.270270</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Wright High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>1800</td>\n",
       "      <td>$1,049,400.00</td>\n",
       "      <td>$583.00</td>\n",
       "      <td>83.682222</td>\n",
       "      <td>83.955000</td>\n",
       "      <td>93.333333</td>\n",
       "      <td>96.611111</td>\n",
       "      <td>94.972222</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Rodriguez High School</th>\n",
       "      <td>District</td>\n",
       "      <td>3999</td>\n",
       "      <td>$2,547,363.00</td>\n",
       "      <td>$637.00</td>\n",
       "      <td>76.842711</td>\n",
       "      <td>80.744686</td>\n",
       "      <td>66.366592</td>\n",
       "      <td>80.220055</td>\n",
       "      <td>73.293323</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Johnson High School</th>\n",
       "      <td>District</td>\n",
       "      <td>4761</td>\n",
       "      <td>$3,094,650.00</td>\n",
       "      <td>$650.00</td>\n",
       "      <td>77.072464</td>\n",
       "      <td>80.966394</td>\n",
       "      <td>66.057551</td>\n",
       "      <td>81.222432</td>\n",
       "      <td>73.639992</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Ford High School</th>\n",
       "      <td>District</td>\n",
       "      <td>2739</td>\n",
       "      <td>$2,739.00</td>\n",
       "      <td>$644.00</td>\n",
       "      <td>77.102592</td>\n",
       "      <td>80.746258</td>\n",
       "      <td>68.309602</td>\n",
       "      <td>79.299014</td>\n",
       "      <td>73.804308</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Thomas High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>1635</td>\n",
       "      <td>$1,043,130.00</td>\n",
       "      <td>$638.00</td>\n",
       "      <td>83.418349</td>\n",
       "      <td>83.848930</td>\n",
       "      <td>93.272171</td>\n",
       "      <td>97.308869</td>\n",
       "      <td>95.290520</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "                      School Type  Total Students Total School Budget  \\\n",
       "Huang High School        District            2917       $1,910,635.00   \n",
       "Figueroa High School     District            2949       $1,884,411.00   \n",
       "Shelton High School       Charter            1761       $1,056,600.00   \n",
       "Hernandez High School    District            4635       $3,022,020.00   \n",
       "Griffin High School       Charter            1468         $917,500.00   \n",
       "Wilson High School        Charter            2283       $1,319,574.00   \n",
       "Cabrera High School       Charter            1858       $1,081,356.00   \n",
       "Bailey High School       District            4976       $3,124,928.00   \n",
       "Holden High School        Charter             427         $248,087.00   \n",
       "Pena High School          Charter             962         $585,858.00   \n",
       "Wright High School        Charter            1800       $1,049,400.00   \n",
       "Rodriguez High School    District            3999       $2,547,363.00   \n",
       "Johnson High School      District            4761       $3,094,650.00   \n",
       "Ford High School         District            2739           $2,739.00   \n",
       "Thomas High School        Charter            1635       $1,043,130.00   \n",
       "\n",
       "                      Per Student Budget  Average Math Score  \\\n",
       "Huang High School                $655.00           76.629414   \n",
       "Figueroa High School             $639.00           76.711767   \n",
       "Shelton High School              $600.00           83.359455   \n",
       "Hernandez High School            $652.00           77.289752   \n",
       "Griffin High School              $625.00           83.351499   \n",
       "Wilson High School               $578.00           83.274201   \n",
       "Cabrera High School              $582.00           83.061895   \n",
       "Bailey High School               $628.00           77.048432   \n",
       "Holden High School               $581.00           83.803279   \n",
       "Pena High School                 $609.00           83.839917   \n",
       "Wright High School               $583.00           83.682222   \n",
       "Rodriguez High School            $637.00           76.842711   \n",
       "Johnson High School              $650.00           77.072464   \n",
       "Ford High School                 $644.00           77.102592   \n",
       "Thomas High School               $638.00           83.418349   \n",
       "\n",
       "                       Average Reading Score  % Passing Math  \\\n",
       "Huang High School                  81.182722       65.683922   \n",
       "Figueroa High School               81.158020       65.988471   \n",
       "Shelton High School                83.725724       93.867121   \n",
       "Hernandez High School              80.934412       66.752967   \n",
       "Griffin High School                83.816757       93.392371   \n",
       "Wilson High School                 83.989488       93.867718   \n",
       "Cabrera High School                83.975780       94.133477   \n",
       "Bailey High School                 81.033963       66.680064   \n",
       "Holden High School                 83.814988       92.505855   \n",
       "Pena High School                   84.044699       94.594595   \n",
       "Wright High School                 83.955000       93.333333   \n",
       "Rodriguez High School              80.744686       66.366592   \n",
       "Johnson High School                80.966394       66.057551   \n",
       "Ford High School                   80.746258       68.309602   \n",
       "Thomas High School                 83.848930       93.272171   \n",
       "\n",
       "                       % Passing Reading  % Overall Passing Rate  \n",
       "Huang High School              81.316421               73.500171  \n",
       "Figueroa High School           80.739234               73.363852  \n",
       "Shelton High School            95.854628               94.860875  \n",
       "Hernandez High School          80.862999               73.807983  \n",
       "Griffin High School            97.138965               95.265668  \n",
       "Wilson High School             96.539641               95.203679  \n",
       "Cabrera High School            97.039828               95.586652  \n",
       "Bailey High School             81.933280               74.306672  \n",
       "Holden High School             96.252927               94.379391  \n",
       "Pena High School               95.945946               95.270270  \n",
       "Wright High School             96.611111               94.972222  \n",
       "Rodriguez High School          80.220055               73.293323  \n",
       "Johnson High School            81.222432               73.639992  \n",
       "Ford High School               79.299014               73.804308  \n",
       "Thomas High School             97.308869               95.290520  "
      ]
     },
     "execution_count": 432,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "school_summary = pd.DataFrame({\"School Type\" :[huang_school_type, figueroa_school_type, shelton_school_type, hernandez_school_type, griffin_school_type, wilson_school_type, cabrera_school_type, bailey_school_type, holden_school_type, pena_school_type, wright_school_type, rodriguez_school_type, johnson_school_type, ford_school_type, thomas_school_type], \n",
    "                               \"Total Students\" :[huang_total_students, figueroa_total_students, shelton_total_students, hernandez_total_students, griffin_total_students, wilson_total_students, cabrera_total_students, bailey_total_students, holden_total_students, pena_total_students, wright_total_students, rodriguez_total_students, johnson_total_students, ford_total_students, thomas_total_students], \n",
    "                               \"Total School Budget\" :[\"${:,.2f}\".format(huang_total_budget),\"${:,.2f}\".format(figueroa_total_budget),\"${:,.2f}\".format(shelton_total_budget),\"${:,.2f}\".format(hernandez_total_budget), \"${:,.2f}\".format(griffin_total_budget),\"${:,.2f}\".format(wilson_total_budget),\"${:,.2f}\".format(cabrera_total_budget),\"${:,.2f}\".format(bailey_total_budget),\n",
    "                                                       \"${:,.2f}\".format(holden_total_budget),\"${:,.2f}\".format(pena_total_budget),\"${:,.2f}\".format(wright_total_budget),\"${:,.2f}\".format(rodriguez_total_budget),\"${:,.2f}\".format(johnson_total_budget),\"${:,.2f}\".format(ford_total_students),\"${:,.2f}\".format(thomas_total_budget)], \n",
    "                                 \"Per Student Budget\" :[\"${:,.2f}\".format(per_stu_budget),\"${:,.2f}\".format(per_fi_stu_budget),\"${:,.2f}\".format(per_sh_stu_budget),\"${:,.2f}\".format(per_hz_stu_budget),\"${:,.2f}\".format(per_gr_stu_budget),\"${:,.2f}\".format(per_wil_stu_budget),\"${:,.2f}\".format(per_ca_stu_budget),\"${:,.2f}\".format(per_bay_stu_budget),\"${:,.2f}\".format(per_hl_stu_budget),\"${:,.2f}\".format(per_pe_stu_budget),\n",
    "                                                        \"${:,.2f}\".format(per_wr_stu_budget),\"${:,.2f}\".format(per_ro_stu_budget),\"${:,.2f}\".format(per_joh_stu_budget),\"${:,.2f}\".format(per_fd_stu_budget),\"${:,.2f}\".format(per_tho_stu_budget)], \n",
    "                               \"Average Math Score\" :[huang_average_math_score, figueroa_average_math_score, shelton_average_math_score, hernandez_average_math_score, griffin_average_math_score, wilson_average_math_score, cabrera_average_math_score, \n",
    "                                                      bailey_average_math_score, holden_average_math_score, pena_average_math_score, wright_average_math_score, rodriguez_average_math_score, johnson_average_math_score, ford_average_math_score, thomas_average_math_score],\n",
    "                                 \"Average Reading Score\" :[huang_average_reading_score, figueroa_average_reading_score, shelton_average_reading_score, hernandez_average_reading_score, griffin_average_reading_score, wilson_average_reading_score, cabrera_average_reading_score, \n",
    "                                                        bailey_average_reading_score, holden_average_reading_score, pena_average_reading_score, wright_average_reading_score, rodriguez_average_reading_score, johnson_average_reading_score, ford_average_reading_score, thomas_average_reading_score], \n",
    "                               \"% Passing Math\" :[per_huang_pass_math, per_figueroa_pass_math, per_shelton_pass_math, per_hernandez_pass_math, per_griffin_pass_math, per_wilson_pass_math, per_cabrera_pass_math, per_bailey_pass_math, per_holden_pass_math, per_pena_pass_math, per_wright_pass_math, per_rodriguez_pass_math, per_johnson_pass_math, per_ford_pass_math, per_thomas_pass_math],\n",
    "                                 \"% Passing Reading\" :[per_huang_pass_reading, per_figueroa_pass_reading, per_shelton_pass_reading, per_hernandez_pass_reading, per_griffin_pass_reading, per_wilson_pass_reading, per_cabrera_pass_reading, per_bailey_pass_reading, per_holden_pass_reading, per_pena_pass_reading, per_wright_pass_reading, per_rodriguez_pass_reading, per_johnson_pass_reading, per_ford_pass_reading, per_thomas_pass_reading], \n",
    "                               \"% Overall Passing Rate\" :[huang_overall, figueroa_overall, shelton_overall, hernandez_overall, griffin_overall, wilson_overall, cabrera_overall, bailey_overall, holden_overall, pena_overall, wright_overall, rodriguez_overall, johnson_overall, ford_overall, thomas_overall]},\n",
    "                                columns=[\"School Type\", \"Total Students\", \"Total School Budget\", \"Per Student Budget\", \"Average Math Score\", \"Average Reading Score\", \n",
    "                                 \"% Passing Math\", \"% Passing Reading\", \"% Overall Passing Rate\"], index=[\"Huang High School\", \"Figueroa High School\", \"Shelton High School\", \"Hernandez High School\", \"Griffin High School\",\n",
    "                                                                                                       \"Wilson High School\", \"Cabrera High School\", \"Bailey High School\", \"Holden High School\", \"Pena High School\", \"Wright High School\", \n",
    "                                                                                                        \"Rodriguez High School\", \"Johnson High School\", \"Ford High School\", \"Thomas High School\"])\n",
    "school_summary"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 148,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Cabrera High School      95.586652\n",
       "Thomas High School       95.290520\n",
       "Pena High School         95.270270\n",
       "Griffin High School      95.265668\n",
       "Wright High School       94.972222\n",
       "Shelton High School      94.860875\n",
       "Holden High School       94.379391\n",
       "Bailey High School       74.306672\n",
       "Hernandez High School    73.807983\n",
       "Ford High School         73.804308\n",
       "Johnson High School      73.639992\n",
       "Huang High School        73.500171\n",
       "Figueroa High School     73.363852\n",
       "Rodriguez High School    73.293323\n",
       "Wilson High School       71.687066\n",
       "Name: % Overall Passing Rate, dtype: float64"
      ]
     },
     "execution_count": 148,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Top Performing Schools (By Passing Rate)\n",
    "school_summary[\"% Overall Passing Rate\"].sort_values(ascending=False)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 151,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>School Type</th>\n",
       "      <th>Total Students</th>\n",
       "      <th>Total School Budget</th>\n",
       "      <th>Per Student Budget</th>\n",
       "      <th>Average Math Score</th>\n",
       "      <th>Average Reading Score</th>\n",
       "      <th>% Passing Math</th>\n",
       "      <th>% Passing Reading</th>\n",
       "      <th>% Overall Passing Rate</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Cabrera High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>1858</td>\n",
       "      <td>$1,081,356.00</td>\n",
       "      <td>$582.00</td>\n",
       "      <td>83.061895</td>\n",
       "      <td>83.975780</td>\n",
       "      <td>94.133477</td>\n",
       "      <td>97.039828</td>\n",
       "      <td>95.586652</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Thomas High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>1635</td>\n",
       "      <td>$1,043,130.00</td>\n",
       "      <td>$638.00</td>\n",
       "      <td>83.418349</td>\n",
       "      <td>83.848930</td>\n",
       "      <td>93.272171</td>\n",
       "      <td>97.308869</td>\n",
       "      <td>95.290520</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Pena High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>962</td>\n",
       "      <td>$585,858.00</td>\n",
       "      <td>$609.00</td>\n",
       "      <td>83.839917</td>\n",
       "      <td>84.044699</td>\n",
       "      <td>94.594595</td>\n",
       "      <td>95.945946</td>\n",
       "      <td>95.270270</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Griffin High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>1468</td>\n",
       "      <td>$917,500.00</td>\n",
       "      <td>$625.00</td>\n",
       "      <td>83.351499</td>\n",
       "      <td>83.816757</td>\n",
       "      <td>93.392371</td>\n",
       "      <td>97.138965</td>\n",
       "      <td>95.265668</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Wright High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>1800</td>\n",
       "      <td>$1,049,400.00</td>\n",
       "      <td>$583.00</td>\n",
       "      <td>83.682222</td>\n",
       "      <td>83.955000</td>\n",
       "      <td>93.333333</td>\n",
       "      <td>96.611111</td>\n",
       "      <td>94.972222</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "                    School Type  Total Students Total School Budget  \\\n",
       "Cabrera High School     Charter            1858       $1,081,356.00   \n",
       "Thomas High School      Charter            1635       $1,043,130.00   \n",
       "Pena High School        Charter             962         $585,858.00   \n",
       "Griffin High School     Charter            1468         $917,500.00   \n",
       "Wright High School      Charter            1800       $1,049,400.00   \n",
       "\n",
       "                    Per Student Budget  Average Math Score  \\\n",
       "Cabrera High School            $582.00           83.061895   \n",
       "Thomas High School             $638.00           83.418349   \n",
       "Pena High School               $609.00           83.839917   \n",
       "Griffin High School            $625.00           83.351499   \n",
       "Wright High School             $583.00           83.682222   \n",
       "\n",
       "                     Average Reading Score  % Passing Math  % Passing Reading  \\\n",
       "Cabrera High School              83.975780       94.133477          97.039828   \n",
       "Thomas High School               83.848930       93.272171          97.308869   \n",
       "Pena High School                 84.044699       94.594595          95.945946   \n",
       "Griffin High School              83.816757       93.392371          97.138965   \n",
       "Wright High School               83.955000       93.333333          96.611111   \n",
       "\n",
       "                     % Overall Passing Rate  \n",
       "Cabrera High School               95.586652  \n",
       "Thomas High School                95.290520  \n",
       "Pena High School                  95.270270  \n",
       "Griffin High School               95.265668  \n",
       "Wright High School                94.972222  "
      ]
     },
     "execution_count": 151,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "top_performing_schools = school_summary.sort_values(\"% Overall Passing Rate\", ascending=False)\n",
    "top_performing_schools.head(5)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 142,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Wilson High School       71.687066\n",
       "Rodriguez High School    73.293323\n",
       "Figueroa High School     73.363852\n",
       "Huang High School        73.500171\n",
       "Johnson High School      73.639992\n",
       "Ford High School         73.804308\n",
       "Hernandez High School    73.807983\n",
       "Bailey High School       74.306672\n",
       "Holden High School       94.379391\n",
       "Shelton High School      94.860875\n",
       "Wright High School       94.972222\n",
       "Griffin High School      95.265668\n",
       "Pena High School         95.270270\n",
       "Thomas High School       95.290520\n",
       "Cabrera High School      95.586652\n",
       "Name: % Overall Passing Rate, dtype: float64"
      ]
     },
     "execution_count": 142,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Bottom Performing Schools (By Passing Rate)\n",
    "school_summary[\"% Overall Passing Rate\"].sort_values()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 147,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>School Type</th>\n",
       "      <th>Total Students</th>\n",
       "      <th>Total School Budget</th>\n",
       "      <th>Per Student Budget</th>\n",
       "      <th>Average Math Score</th>\n",
       "      <th>Average Reading Score</th>\n",
       "      <th>% Passing Math</th>\n",
       "      <th>% Passing Reading</th>\n",
       "      <th>% Overall Passing Rate</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Wilson High School</th>\n",
       "      <td>Charter</td>\n",
       "      <td>2283</td>\n",
       "      <td>$1,319,574.00</td>\n",
       "      <td>$578.00</td>\n",
       "      <td>83.274201</td>\n",
       "      <td>83.989488</td>\n",
       "      <td>46.235167</td>\n",
       "      <td>97.138965</td>\n",
       "      <td>71.687066</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Rodriguez High School</th>\n",
       "      <td>District</td>\n",
       "      <td>3999</td>\n",
       "      <td>$2,547,363.00</td>\n",
       "      <td>$637.00</td>\n",
       "      <td>76.842711</td>\n",
       "      <td>80.744686</td>\n",
       "      <td>66.366592</td>\n",
       "      <td>80.220055</td>\n",
       "      <td>73.293323</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Figueroa High School</th>\n",
       "      <td>District</td>\n",
       "      <td>2949</td>\n",
       "      <td>$1,884,411.00</td>\n",
       "      <td>$639.00</td>\n",
       "      <td>76.711767</td>\n",
       "      <td>81.158020</td>\n",
       "      <td>65.988471</td>\n",
       "      <td>80.739234</td>\n",
       "      <td>73.363852</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Huang High School</th>\n",
       "      <td>District</td>\n",
       "      <td>2917</td>\n",
       "      <td>$1,910,635.00</td>\n",
       "      <td>$655.00</td>\n",
       "      <td>76.629414</td>\n",
       "      <td>81.182722</td>\n",
       "      <td>65.683922</td>\n",
       "      <td>81.316421</td>\n",
       "      <td>73.500171</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Johnson High School</th>\n",
       "      <td>District</td>\n",
       "      <td>4761</td>\n",
       "      <td>$3,094,650.00</td>\n",
       "      <td>$650.00</td>\n",
       "      <td>77.072464</td>\n",
       "      <td>80.966394</td>\n",
       "      <td>66.057551</td>\n",
       "      <td>81.222432</td>\n",
       "      <td>73.639992</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "                      School Type  Total Students Total School Budget  \\\n",
       "Wilson High School        Charter            2283       $1,319,574.00   \n",
       "Rodriguez High School    District            3999       $2,547,363.00   \n",
       "Figueroa High School     District            2949       $1,884,411.00   \n",
       "Huang High School        District            2917       $1,910,635.00   \n",
       "Johnson High School      District            4761       $3,094,650.00   \n",
       "\n",
       "                      Per Student Budget  Average Math Score  \\\n",
       "Wilson High School               $578.00           83.274201   \n",
       "Rodriguez High School            $637.00           76.842711   \n",
       "Figueroa High School             $639.00           76.711767   \n",
       "Huang High School                $655.00           76.629414   \n",
       "Johnson High School              $650.00           77.072464   \n",
       "\n",
       "                       Average Reading Score  % Passing Math  \\\n",
       "Wilson High School                 83.989488       46.235167   \n",
       "Rodriguez High School              80.744686       66.366592   \n",
       "Figueroa High School               81.158020       65.988471   \n",
       "Huang High School                  81.182722       65.683922   \n",
       "Johnson High School                80.966394       66.057551   \n",
       "\n",
       "                       % Passing Reading  % Overall Passing Rate  \n",
       "Wilson High School             97.138965               71.687066  \n",
       "Rodriguez High School          80.220055               73.293323  \n",
       "Figueroa High School           80.739234               73.363852  \n",
       "Huang High School              81.316421               73.500171  \n",
       "Johnson High School            81.222432               73.639992  "
      ]
     },
     "execution_count": 147,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "bottom_performing_schools = school_summary.sort_values(\"% Overall Passing Rate\")\n",
    "bottom_performing_schools.head(5)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 271,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Math Scores by Grade\n",
    "# Thomas High School\n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "# del students_df[\"Student ID, name, gender, reading_score\"]\n",
    "thomas_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Thomas High School\"]\n",
    "grade_sorted = math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "thomas_grade9_total_students = grade_sorted[grade_sorted[\"grade\"] == \"9th\"]\n",
    "thomas_grade9th_total_students = thomas_grade9_total_students.grade.count()\n",
    "thomas_grade10_total_students = grade_sorted[grade_sorted[\"grade\"] == \"10th\"]\n",
    "thomas_grade10th_total_students = thomas_grade10_total_students.grade.count()\n",
    "thomas_grade11_total_students = grade_sorted[grade_sorted[\"grade\"] == \"11th\"]\n",
    "thomas_grade11th_total_students = thomas_grade11_total_students.grade.count()\n",
    "thomas_grade12_total_students = grade_sorted[grade_sorted[\"grade\"] == \"12th\"]\n",
    "thomas_grade12th_total_students = thomas_grade12_total_students.grade.count()\n",
    "thomas_total9_math_score = thomas_grade9_total_students[\"math_score\"].sum()\n",
    "thomas_total10_math_score = thomas_grade10_total_students[\"math_score\"].sum()\n",
    "thomas_total11_math_score = thomas_grade11_total_students[\"math_score\"].sum()\n",
    "thomas_total12_math_score = thomas_grade12_total_students[\"math_score\"].sum()\n",
    "thomas_average9_math_score = (thomas_total9_math_score / thomas_grade9th_total_students)\n",
    "thomas_average10_math_score = (thomas_total10_math_score / thomas_grade10th_total_students)\n",
    "thomas_average11_math_score = (thomas_total11_math_score / thomas_grade11th_total_students)\n",
    "thomas_average12_math_score = (thomas_total12_math_score / thomas_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 276,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Huang High School\n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "huang_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Huang High School\"]\n",
    "huang_grade_sorted = huang_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "huang_grade9_total_students = huang_grade_sorted[huang_grade_sorted[\"grade\"] == \"9th\"]\n",
    "huang_grade9th_total_students = huang_grade9_total_students.grade.count()\n",
    "huang_grade10_total_students = huang_grade_sorted[huang_grade_sorted[\"grade\"] == \"10th\"]\n",
    "huang_grade10th_total_students = huang_grade10_total_students.grade.count()\n",
    "huang_grade11_total_students = huang_grade_sorted[huang_grade_sorted[\"grade\"] == \"11th\"]\n",
    "huang_grade11th_total_students = huang_grade11_total_students.grade.count()\n",
    "huang_grade12_total_students = huang_grade_sorted[huang_grade_sorted[\"grade\"] == \"12th\"]\n",
    "huang_grade12th_total_students = huang_grade12_total_students.grade.count()\n",
    "huang_total9_math_score = huang_grade9_total_students[\"math_score\"].sum()\n",
    "huang_total10_math_score = huang_grade10_total_students[\"math_score\"].sum()\n",
    "huang_total11_math_score = huang_grade11_total_students[\"math_score\"].sum()\n",
    "huang_total12_math_score = huang_grade12_total_students[\"math_score\"].sum()\n",
    "huang_average9_math_score = (huang_total9_math_score / huang_grade9th_total_students)\n",
    "huang_average10_math_score = (huang_total10_math_score / huang_grade10th_total_students)\n",
    "huang_average11_math_score = (huang_total11_math_score / huang_grade11th_total_students)\n",
    "huang_average12_math_score = (huang_total12_math_score / huang_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 278,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# Figueroa High School\n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "figueroa_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Figueroa High School\"]\n",
    "figueroa_grade_sorted = figueroa_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "figueroa_grade9_total_students = figueroa_grade_sorted[figueroa_grade_sorted[\"grade\"] == \"9th\"]\n",
    "figueroa_grade9th_total_students = figueroa_grade9_total_students.grade.count()\n",
    "figueroa_grade10_total_students = figueroa_grade_sorted[figueroa_grade_sorted[\"grade\"] == \"10th\"]\n",
    "figueroa_grade10th_total_students = figueroa_grade10_total_students.grade.count()\n",
    "figueroa_grade11_total_students = figueroa_grade_sorted[figueroa_grade_sorted[\"grade\"] == \"11th\"]\n",
    "figueroa_grade11th_total_students = figueroa_grade11_total_students.grade.count()\n",
    "figueroa_grade12_total_students = figueroa_grade_sorted[figueroa_grade_sorted[\"grade\"] == \"12th\"]\n",
    "figueroa_grade12th_total_students = figueroa_grade12_total_students.grade.count()\n",
    "figueroa_total9_math_score = figueroa_grade9_total_students[\"math_score\"].sum()\n",
    "figueroa_total10_math_score = figueroa_grade10_total_students[\"math_score\"].sum()\n",
    "figueroa_total11_math_score = figueroa_grade11_total_students[\"math_score\"].sum()\n",
    "figueroa_total12_math_score = figueroa_grade12_total_students[\"math_score\"].sum()\n",
    "figueroa_average9_math_score = (figueroa_total9_math_score / figueroa_grade9th_total_students)\n",
    "figueroa_average10_math_score = (figueroa_total10_math_score / figueroa_grade10th_total_students)\n",
    "figueroa_average11_math_score = (figueroa_total11_math_score / figueroa_grade11th_total_students)\n",
    "figueroa_average12_math_score = (figueroa_total12_math_score / figueroa_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 280,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# Shelton High School\n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "shelton_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Shelton High School\"]\n",
    "shelton_grade_sorted = shelton_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "shelton_grade9_total_students = shelton_grade_sorted[shelton_grade_sorted[\"grade\"] == \"9th\"]\n",
    "shelton_grade9th_total_students = shelton_grade9_total_students.grade.count()\n",
    "shelton_grade10_total_students = shelton_grade_sorted[shelton_grade_sorted[\"grade\"] == \"10th\"]\n",
    "shelton_grade10th_total_students = shelton_grade10_total_students.grade.count()\n",
    "shelton_grade11_total_students = shelton_grade_sorted[shelton_grade_sorted[\"grade\"] == \"11th\"]\n",
    "shelton_grade11th_total_students = shelton_grade11_total_students.grade.count()\n",
    "shelton_grade12_total_students = shelton_grade_sorted[shelton_grade_sorted[\"grade\"] == \"12th\"]\n",
    "shelton_grade12th_total_students = shelton_grade12_total_students.grade.count()\n",
    "shelton_total9_math_score = shelton_grade9_total_students[\"math_score\"].sum()\n",
    "shelton_total10_math_score = shelton_grade10_total_students[\"math_score\"].sum()\n",
    "shelton_total11_math_score = shelton_grade11_total_students[\"math_score\"].sum()\n",
    "shelton_total12_math_score = shelton_grade12_total_students[\"math_score\"].sum()\n",
    "shelton_average9_math_score = (shelton_total9_math_score / shelton_grade9th_total_students)\n",
    "shelton_average10_math_score = (shelton_total10_math_score / shelton_grade10th_total_students)\n",
    "shelton_average11_math_score = (shelton_total11_math_score / shelton_grade11th_total_students)\n",
    "shelton_average12_math_score = (shelton_total12_math_score / shelton_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 282,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Hernandez High School\n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "her_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Hernandez High School\"]\n",
    "her_grade_sorted = her_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "her_grade9_total_students = her_grade_sorted[her_grade_sorted[\"grade\"] == \"9th\"]\n",
    "her_grade9th_total_students = her_grade9_total_students.grade.count()\n",
    "her_grade10_total_students = her_grade_sorted[her_grade_sorted[\"grade\"] == \"10th\"]\n",
    "her_grade10th_total_students = her_grade10_total_students.grade.count()\n",
    "her_grade11_total_students = her_grade_sorted[her_grade_sorted[\"grade\"] == \"11th\"]\n",
    "her_grade11th_total_students = her_grade11_total_students.grade.count()\n",
    "her_grade12_total_students = her_grade_sorted[her_grade_sorted[\"grade\"] == \"12th\"]\n",
    "her_grade12th_total_students = her_grade12_total_students.grade.count()\n",
    "her_total9_math_score = her_grade9_total_students[\"math_score\"].sum()\n",
    "her_total10_math_score = her_grade10_total_students[\"math_score\"].sum()\n",
    "her_total11_math_score = her_grade11_total_students[\"math_score\"].sum()\n",
    "her_total12_math_score = her_grade12_total_students[\"math_score\"].sum()\n",
    "her_average9_math_score = (her_total9_math_score / her_grade9th_total_students)\n",
    "her_average10_math_score = (her_total10_math_score / her_grade10th_total_students)\n",
    "her_average11_math_score = (her_total11_math_score / her_grade11th_total_students)\n",
    "her_average12_math_score = (her_total12_math_score / her_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 286,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Griffin High School\n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "griffin_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Griffin High School\"]\n",
    "griffin_grade_sorted = griffin_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "griffin_grade9_total_students = griffin_grade_sorted[griffin_grade_sorted[\"grade\"] == \"9th\"]\n",
    "griffin_grade9th_total_students = griffin_grade9_total_students.grade.count()\n",
    "griffin_grade10_total_students = griffin_grade_sorted[griffin_grade_sorted[\"grade\"] == \"10th\"]\n",
    "griffin_grade10th_total_students = griffin_grade10_total_students.grade.count()\n",
    "griffin_grade11_total_students = griffin_grade_sorted[griffin_grade_sorted[\"grade\"] == \"11th\"]\n",
    "griffin_grade11th_total_students = griffin_grade11_total_students.grade.count()\n",
    "griffin_grade12_total_students = griffin_grade_sorted[griffin_grade_sorted[\"grade\"] == \"12th\"]\n",
    "griffin_grade12th_total_students = griffin_grade12_total_students.grade.count()\n",
    "griffin_total9_math_score = griffin_grade9_total_students[\"math_score\"].sum()\n",
    "griffin_total10_math_score = griffin_grade10_total_students[\"math_score\"].sum()\n",
    "griffin_total11_math_score = griffin_grade11_total_students[\"math_score\"].sum()\n",
    "griffin_total12_math_score = griffin_grade12_total_students[\"math_score\"].sum()\n",
    "griffin_average9_math_score = (griffin_total9_math_score / griffin_grade9th_total_students)\n",
    "griffin_average10_math_score = (griffin_total10_math_score / griffin_grade10th_total_students)\n",
    "griffin_average11_math_score = (griffin_total11_math_score / griffin_grade11th_total_students)\n",
    "griffin_average12_math_score = (griffin_total12_math_score / griffin_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 291,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Wilson High School\n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "wilson_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Wilson High School\"]\n",
    "wilson_grade_sorted = wilson_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "wilson_grade9_total_students = wilson_grade_sorted[wilson_grade_sorted[\"grade\"] == \"9th\"]\n",
    "wilson_grade9th_total_students = wilson_grade9_total_students.grade.count()\n",
    "wilson_grade10_total_students = wilson_grade_sorted[wilson_grade_sorted[\"grade\"] == \"10th\"]\n",
    "wilson_grade10th_total_students = wilson_grade10_total_students.grade.count()\n",
    "wilson_grade11_total_students = wilson_grade_sorted[wilson_grade_sorted[\"grade\"] == \"11th\"]\n",
    "wilson_grade11th_total_students = wilson_grade11_total_students.grade.count()\n",
    "wilson_grade12_total_students = wilson_grade_sorted[wilson_grade_sorted[\"grade\"] == \"12th\"]\n",
    "wilson_grade12th_total_students = wilson_grade12_total_students.grade.count()\n",
    "wilson_total9_math_score = wilson_grade9_total_students[\"math_score\"].sum()\n",
    "wilson_total10_math_score = wilson_grade10_total_students[\"math_score\"].sum()\n",
    "wilson_total11_math_score = wilson_grade11_total_students[\"math_score\"].sum()\n",
    "wilson_total12_math_score = wilson_grade12_total_students[\"math_score\"].sum()\n",
    "wilson_average9_math_score = (wilson_total9_math_score / wilson_grade9th_total_students)\n",
    "wilson_average10_math_score = (wilson_total10_math_score / wilson_grade10th_total_students)\n",
    "wilson_average11_math_score = (wilson_total11_math_score / wilson_grade11th_total_students)\n",
    "wilson_average12_math_score = (wilson_total12_math_score / wilson_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 293,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Cabrera High School \n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "cabrera_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Cabrera High School\"]\n",
    "cabrera_grade_sorted = cabrera_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "cabrera_grade9_total_students = cabrera_grade_sorted[cabrera_grade_sorted[\"grade\"] == \"9th\"]\n",
    "cabrera_grade9th_total_students = cabrera_grade9_total_students.grade.count()\n",
    "cabrera_grade10_total_students = cabrera_grade_sorted[cabrera_grade_sorted[\"grade\"] == \"10th\"]\n",
    "cabrera_grade10th_total_students = cabrera_grade10_total_students.grade.count()\n",
    "cabrera_grade11_total_students = cabrera_grade_sorted[cabrera_grade_sorted[\"grade\"] == \"11th\"]\n",
    "cabrera_grade11th_total_students = cabrera_grade11_total_students.grade.count()\n",
    "cabrera_grade12_total_students = cabrera_grade_sorted[cabrera_grade_sorted[\"grade\"] == \"12th\"]\n",
    "cabrera_grade12th_total_students = cabrera_grade12_total_students.grade.count()\n",
    "cabrera_total9_math_score = cabrera_grade9_total_students[\"math_score\"].sum()\n",
    "cabrera_total10_math_score = cabrera_grade10_total_students[\"math_score\"].sum()\n",
    "cabrera_total11_math_score = cabrera_grade11_total_students[\"math_score\"].sum()\n",
    "cabrera_total12_math_score = cabrera_grade12_total_students[\"math_score\"].sum()\n",
    "cabrera_average9_math_score = (cabrera_total9_math_score / cabrera_grade9th_total_students)\n",
    "cabrera_average10_math_score = (cabrera_total10_math_score / cabrera_grade10th_total_students)\n",
    "cabrera_average11_math_score = (cabrera_total11_math_score / cabrera_grade11th_total_students)\n",
    "cabrera_average12_math_score = (cabrera_total12_math_score / cabrera_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 296,
   "metadata": {},
   "outputs": [],
   "source": [
    "# School Summary - Bailey High School \n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "bailey_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Bailey High School\"]\n",
    "bailey_grade_sorted = bailey_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "bailey_grade9_total_students = bailey_grade_sorted[bailey_grade_sorted[\"grade\"] == \"9th\"]\n",
    "bailey_grade9th_total_students = bailey_grade9_total_students.grade.count()\n",
    "bailey_grade10_total_students = bailey_grade_sorted[bailey_grade_sorted[\"grade\"] == \"10th\"]\n",
    "bailey_grade10th_total_students = bailey_grade10_total_students.grade.count()\n",
    "bailey_grade11_total_students = bailey_grade_sorted[bailey_grade_sorted[\"grade\"] == \"11th\"]\n",
    "bailey_grade11th_total_students = bailey_grade11_total_students.grade.count()\n",
    "bailey_grade12_total_students = bailey_grade_sorted[bailey_grade_sorted[\"grade\"] == \"12th\"]\n",
    "bailey_grade12th_total_students = bailey_grade12_total_students.grade.count()\n",
    "bailey_total9_math_score = bailey_grade9_total_students[\"math_score\"].sum()\n",
    "bailey_total10_math_score = bailey_grade10_total_students[\"math_score\"].sum()\n",
    "bailey_total11_math_score = bailey_grade11_total_students[\"math_score\"].sum()\n",
    "bailey_total12_math_score = bailey_grade12_total_students[\"math_score\"].sum()\n",
    "bailey_average9_math_score = (bailey_total9_math_score / bailey_grade9th_total_students)\n",
    "bailey_average10_math_score = (bailey_total10_math_score / bailey_grade10th_total_students)\n",
    "bailey_average11_math_score = (bailey_total11_math_score / bailey_grade11th_total_students)\n",
    "bailey_average12_math_score = (bailey_total12_math_score / bailey_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 300,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Holden High School \n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "holden_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Holden High School\"]\n",
    "holden_grade_sorted = holden_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "holden_grade9_total_students = holden_grade_sorted[holden_grade_sorted[\"grade\"] == \"9th\"]\n",
    "holden_grade9th_total_students = holden_grade9_total_students.grade.count()\n",
    "holden_grade10_total_students = holden_grade_sorted[holden_grade_sorted[\"grade\"] == \"10th\"]\n",
    "holden_grade10th_total_students = holden_grade10_total_students.grade.count()\n",
    "holden_grade11_total_students = holden_grade_sorted[holden_grade_sorted[\"grade\"] == \"11th\"]\n",
    "holden_grade11th_total_students = holden_grade11_total_students.grade.count()\n",
    "holden_grade12_total_students = holden_grade_sorted[holden_grade_sorted[\"grade\"] == \"12th\"]\n",
    "holden_grade12th_total_students = holden_grade12_total_students.grade.count()\n",
    "holden_total9_math_score = holden_grade9_total_students[\"math_score\"].sum()\n",
    "holden_total10_math_score = holden_grade10_total_students[\"math_score\"].sum()\n",
    "holden_total11_math_score = holden_grade11_total_students[\"math_score\"].sum()\n",
    "holden_total12_math_score = holden_grade12_total_students[\"math_score\"].sum()\n",
    "holden_average9_math_score = (holden_total9_math_score / holden_grade9th_total_students)\n",
    "holden_average10_math_score = (holden_total10_math_score / holden_grade10th_total_students)\n",
    "holden_average11_math_score = (holden_total11_math_score / holden_grade11th_total_students)\n",
    "holden_average12_math_score = (holden_total12_math_score / holden_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 298,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Pena High School \n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "pena_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Pena High School\"]\n",
    "pena_grade_sorted = pena_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "pena_grade9_total_students = pena_grade_sorted[pena_grade_sorted[\"grade\"] == \"9th\"]\n",
    "pena_grade9th_total_students = pena_grade9_total_students.grade.count()\n",
    "pena_grade10_total_students = pena_grade_sorted[pena_grade_sorted[\"grade\"] == \"10th\"]\n",
    "pena_grade10th_total_students = pena_grade10_total_students.grade.count()\n",
    "pena_grade11_total_students = pena_grade_sorted[pena_grade_sorted[\"grade\"] == \"11th\"]\n",
    "pena_grade11th_total_students = pena_grade11_total_students.grade.count()\n",
    "pena_grade12_total_students = pena_grade_sorted[pena_grade_sorted[\"grade\"] == \"12th\"]\n",
    "pena_grade12th_total_students = pena_grade12_total_students.grade.count()\n",
    "pena_total9_math_score = pena_grade9_total_students[\"math_score\"].sum()\n",
    "pena_total10_math_score = pena_grade10_total_students[\"math_score\"].sum()\n",
    "pena_total11_math_score = pena_grade11_total_students[\"math_score\"].sum()\n",
    "pena_total12_math_score = pena_grade12_total_students[\"math_score\"].sum()\n",
    "pena_average9_math_score = (pena_total9_math_score / pena_grade9th_total_students)\n",
    "pena_average10_math_score = (pena_total10_math_score / pena_grade10th_total_students)\n",
    "pena_average11_math_score = (pena_total11_math_score / pena_grade11th_total_students)\n",
    "pena_average12_math_score = (pena_total12_math_score / pena_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 302,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Wright High School \n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "wright_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Wright High School\"]\n",
    "wright_grade_sorted = wright_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "wright_grade9_total_students = wright_grade_sorted[wright_grade_sorted[\"grade\"] == \"9th\"]\n",
    "wright_grade9th_total_students = wright_grade9_total_students.grade.count()\n",
    "wright_grade10_total_students = wright_grade_sorted[wright_grade_sorted[\"grade\"] == \"10th\"]\n",
    "wright_grade10th_total_students = wright_grade10_total_students.grade.count()\n",
    "wright_grade11_total_students = wright_grade_sorted[wright_grade_sorted[\"grade\"] == \"11th\"]\n",
    "wright_grade11th_total_students = wright_grade11_total_students.grade.count()\n",
    "wright_grade12_total_students = wright_grade_sorted[wright_grade_sorted[\"grade\"] == \"12th\"]\n",
    "wright_grade12th_total_students = wright_grade12_total_students.grade.count()\n",
    "wright_total9_math_score = wright_grade9_total_students[\"math_score\"].sum()\n",
    "wright_total10_math_score = wright_grade10_total_students[\"math_score\"].sum()\n",
    "wright_total11_math_score = wright_grade11_total_students[\"math_score\"].sum()\n",
    "wright_total12_math_score = wright_grade12_total_students[\"math_score\"].sum()\n",
    "wright_average9_math_score = (wright_total9_math_score / wright_grade9th_total_students)\n",
    "wright_average10_math_score = (wright_total10_math_score / wright_grade10th_total_students)\n",
    "wright_average11_math_score = (wright_total11_math_score / wright_grade11th_total_students)\n",
    "wright_average12_math_score = (wright_total12_math_score / wright_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 304,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Rodriguez High School \n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "rod_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Wright High School\"]\n",
    "rod_grade_sorted = rod_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "rod_grade9_total_students = rod_grade_sorted[rod_grade_sorted[\"grade\"] == \"9th\"]\n",
    "rod_grade9th_total_students = rod_grade9_total_students.grade.count()\n",
    "rod_grade10_total_students = rod_grade_sorted[rod_grade_sorted[\"grade\"] == \"10th\"]\n",
    "rod_grade10th_total_students = rod_grade10_total_students.grade.count()\n",
    "rod_grade11_total_students = rod_grade_sorted[rod_grade_sorted[\"grade\"] == \"11th\"]\n",
    "rod_grade11th_total_students = rod_grade11_total_students.grade.count()\n",
    "rod_grade12_total_students = rod_grade_sorted[rod_grade_sorted[\"grade\"] == \"12th\"]\n",
    "rod_grade12th_total_students = rod_grade12_total_students.grade.count()\n",
    "rod_total9_math_score = rod_grade9_total_students[\"math_score\"].sum()\n",
    "rod_total10_math_score = rod_grade10_total_students[\"math_score\"].sum()\n",
    "rod_total11_math_score = rod_grade11_total_students[\"math_score\"].sum()\n",
    "rod_total12_math_score = rod_grade12_total_students[\"math_score\"].sum()\n",
    "rod_average9_math_score = (rod_total9_math_score / rod_grade9th_total_students)\n",
    "rod_average10_math_score = (rod_total10_math_score / rod_grade10th_total_students)\n",
    "rod_average11_math_score = (rod_total11_math_score / rod_grade11th_total_students)\n",
    "rod_average12_math_score = (rod_total12_math_score / rod_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 306,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Johnson High School \n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "johnson_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Wright High School\"]\n",
    "johnson_grade_sorted = johnson_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "johnson_grade9_total_students = johnson_grade_sorted[johnson_grade_sorted[\"grade\"] == \"9th\"]\n",
    "johnson_grade9th_total_students = johnson_grade9_total_students.grade.count()\n",
    "johnson_grade10_total_students = johnson_grade_sorted[johnson_grade_sorted[\"grade\"] == \"10th\"]\n",
    "johnson_grade10th_total_students = johnson_grade10_total_students.grade.count()\n",
    "johnson_grade11_total_students = johnson_grade_sorted[johnson_grade_sorted[\"grade\"] == \"11th\"]\n",
    "johnson_grade11th_total_students = johnson_grade11_total_students.grade.count()\n",
    "johnson_grade12_total_students = johnson_grade_sorted[johnson_grade_sorted[\"grade\"] == \"12th\"]\n",
    "johnson_grade12th_total_students = johnson_grade12_total_students.grade.count()\n",
    "johnson_total9_math_score = johnson_grade9_total_students[\"math_score\"].sum()\n",
    "johnson_total10_math_score = johnson_grade10_total_students[\"math_score\"].sum()\n",
    "johnson_total11_math_score = johnson_grade11_total_students[\"math_score\"].sum()\n",
    "johnson_total12_math_score = johnson_grade12_total_students[\"math_score\"].sum()\n",
    "johnson_average9_math_score = (johnson_total9_math_score / johnson_grade9th_total_students)\n",
    "johnson_average10_math_score = (johnson_total10_math_score / johnson_grade10th_total_students)\n",
    "johnson_average11_math_score = (johnson_total11_math_score / johnson_grade11th_total_students)\n",
    "johnson_average12_math_score = (johnson_total12_math_score / johnson_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 308,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Ford High School \n",
    "math_by_grade_pd = students_df.sort_values(\"grade\" and \"math_score\")\n",
    "ford_math_by_grade = math_by_grade_pd[math_by_grade_pd[\"school\"] == \"Wright High School\"]\n",
    "ford_grade_sorted = ford_math_by_grade.sort_values(\"grade\", ascending=False)\n",
    "ford_grade9_total_students = ford_grade_sorted[ford_grade_sorted[\"grade\"] == \"9th\"]\n",
    "ford_grade9th_total_students = ford_grade9_total_students.grade.count()\n",
    "ford_grade10_total_students = ford_grade_sorted[ford_grade_sorted[\"grade\"] == \"10th\"]\n",
    "ford_grade10th_total_students = ford_grade10_total_students.grade.count()\n",
    "ford_grade11_total_students = ford_grade_sorted[ford_grade_sorted[\"grade\"] == \"11th\"]\n",
    "ford_grade11th_total_students = ford_grade11_total_students.grade.count()\n",
    "ford_grade12_total_students = ford_grade_sorted[ford_grade_sorted[\"grade\"] == \"12th\"]\n",
    "ford_grade12th_total_students = ford_grade12_total_students.grade.count()\n",
    "ford_total9_math_score = ford_grade9_total_students[\"math_score\"].sum()\n",
    "ford_total10_math_score = ford_grade10_total_students[\"math_score\"].sum()\n",
    "ford_total11_math_score = ford_grade11_total_students[\"math_score\"].sum()\n",
    "ford_total12_math_score = ford_grade12_total_students[\"math_score\"].sum()\n",
    "ford_average9_math_score = (ford_total9_math_score / ford_grade9th_total_students)\n",
    "ford_average10_math_score = (ford_total10_math_score / ford_grade10th_total_students)\n",
    "ford_average11_math_score = (ford_total11_math_score / ford_grade11th_total_students)\n",
    "ford_average12_math_score = (ford_total12_math_score / ford_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 309,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>9th</th>\n",
       "      <th>10th</th>\n",
       "      <th>11th</th>\n",
       "      <th>12th</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Huang High School</th>\n",
       "      <td>77.027251</td>\n",
       "      <td>75.908735</td>\n",
       "      <td>76.446602</td>\n",
       "      <td>77.225641</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Figueroa High School</th>\n",
       "      <td>76.403037</td>\n",
       "      <td>76.539974</td>\n",
       "      <td>76.884344</td>\n",
       "      <td>77.151369</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Shelton High School</th>\n",
       "      <td>83.420755</td>\n",
       "      <td>82.917411</td>\n",
       "      <td>83.383495</td>\n",
       "      <td>83.778976</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Hernandez High School</th>\n",
       "      <td>77.438495</td>\n",
       "      <td>77.337408</td>\n",
       "      <td>77.136029</td>\n",
       "      <td>77.186567</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Griffin High School</th>\n",
       "      <td>82.044010</td>\n",
       "      <td>84.229064</td>\n",
       "      <td>83.842105</td>\n",
       "      <td>83.356164</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Wilson High School</th>\n",
       "      <td>83.085578</td>\n",
       "      <td>83.724422</td>\n",
       "      <td>83.195326</td>\n",
       "      <td>83.035794</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Cabrera High School</th>\n",
       "      <td>83.094697</td>\n",
       "      <td>83.154506</td>\n",
       "      <td>82.765560</td>\n",
       "      <td>83.277487</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Bailey High School</th>\n",
       "      <td>77.083676</td>\n",
       "      <td>76.996772</td>\n",
       "      <td>77.515588</td>\n",
       "      <td>76.492218</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Holden High School</th>\n",
       "      <td>83.787402</td>\n",
       "      <td>83.429825</td>\n",
       "      <td>85.000000</td>\n",
       "      <td>82.855422</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Pena High School</th>\n",
       "      <td>83.625455</td>\n",
       "      <td>83.372000</td>\n",
       "      <td>84.328125</td>\n",
       "      <td>84.121547</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Wright High School</th>\n",
       "      <td>83.264706</td>\n",
       "      <td>83.836782</td>\n",
       "      <td>83.836782</td>\n",
       "      <td>83.644986</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Rodriguez High School</th>\n",
       "      <td>83.264706</td>\n",
       "      <td>84.010288</td>\n",
       "      <td>83.836782</td>\n",
       "      <td>83.644986</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Johnson High School</th>\n",
       "      <td>83.264706</td>\n",
       "      <td>84.010288</td>\n",
       "      <td>83.836782</td>\n",
       "      <td>83.644986</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Ford High School</th>\n",
       "      <td>83.264706</td>\n",
       "      <td>84.010288</td>\n",
       "      <td>83.836782</td>\n",
       "      <td>83.644986</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Thomas High School</th>\n",
       "      <td>83.590022</td>\n",
       "      <td>83.087886</td>\n",
       "      <td>83.498795</td>\n",
       "      <td>83.497041</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "                             9th       10th       11th       12th\n",
       "Huang High School      77.027251  75.908735  76.446602  77.225641\n",
       "Figueroa High School   76.403037  76.539974  76.884344  77.151369\n",
       "Shelton High School    83.420755  82.917411  83.383495  83.778976\n",
       "Hernandez High School  77.438495  77.337408  77.136029  77.186567\n",
       "Griffin High School    82.044010  84.229064  83.842105  83.356164\n",
       "Wilson High School     83.085578  83.724422  83.195326  83.035794\n",
       "Cabrera High School    83.094697  83.154506  82.765560  83.277487\n",
       "Bailey High School     77.083676  76.996772  77.515588  76.492218\n",
       "Holden High School     83.787402  83.429825  85.000000  82.855422\n",
       "Pena High School       83.625455  83.372000  84.328125  84.121547\n",
       "Wright High School     83.264706  83.836782  83.836782  83.644986\n",
       "Rodriguez High School  83.264706  84.010288  83.836782  83.644986\n",
       "Johnson High School    83.264706  84.010288  83.836782  83.644986\n",
       "Ford High School       83.264706  84.010288  83.836782  83.644986\n",
       "Thomas High School     83.590022  83.087886  83.498795  83.497041"
      ]
     },
     "execution_count": 309,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "scores_by_grade = pd.DataFrame({\"9th\" :[huang_average9_math_score, figueroa_average9_math_score, shelton_average9_math_score, her_average9_math_score, griffin_average9_math_score, wilson_average9_math_score, cabrera_average9_math_score, bailey_average9_math_score, \n",
    "                                        holden_average9_math_score, pena_average9_math_score, wright_average9_math_score, rod_average9_math_score, johnson_average9_math_score , ford_average9_math_score, thomas_average9_math_score], \n",
    "                                \"10th\" :[huang_average10_math_score, figueroa_average10_math_score, shelton_average10_math_score, her_average10_math_score, griffin_average10_math_score, wilson_average10_math_score, cabrera_average10_math_score, bailey_average10_math_score, \n",
    "                                         holden_average10_math_score, pena_average10_math_score, wright_average11_math_score, rod_average10_math_score, johnson_average10_math_score , ford_average10_math_score, thomas_average10_math_score], \n",
    "                                \"11th\" :[huang_average11_math_score, figueroa_average11_math_score, shelton_average11_math_score, her_average11_math_score, griffin_average11_math_score, wilson_average11_math_score, cabrera_average11_math_score, bailey_average11_math_score, \n",
    "                                         holden_average11_math_score, pena_average11_math_score, wright_average11_math_score, rod_average11_math_score, johnson_average11_math_score , ford_average11_math_score, thomas_average11_math_score], \n",
    "                                \"12th\" :[huang_average12_math_score, figueroa_average12_math_score, shelton_average12_math_score, her_average12_math_score, griffin_average12_math_score, wilson_average12_math_score, cabrera_average12_math_score, bailey_average12_math_score, \n",
    "                                         holden_average12_math_score, pena_average12_math_score, wright_average12_math_score, rod_average12_math_score, johnson_average12_math_score , ford_average12_math_score, thomas_average12_math_score]}, \n",
    "                               columns=[\"9th\", \"10th\", \"11th\", \"12th\"], \n",
    "                               index=[\"Huang High School\", \"Figueroa High School\", \"Shelton High School\", \"Hernandez High School\", \"Griffin High School\", \"Wilson High School\", \"Cabrera High School\", \n",
    "                                      \"Bailey High School\", \"Holden High School\", \"Pena High School\", \"Wright High School\", \"Rodriguez High School\", \"Johnson High School\", \"Ford High School\", \"Thomas High School\"]) \n",
    "scores_by_grade"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 345,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Reading Scores by Grade \n",
    "# Huang High School\n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "# del students_df[\"Student ID, name, gender, math_score\"]\n",
    "huang_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Huang High School\"]\n",
    "huang_grade_sorted = huang_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "huang_grade9_total_students = huang_grade_sorted[huang_grade_sorted[\"grade\"] == \"9th\"]\n",
    "huang_grade9th_total_students = huang_grade9_total_students.grade.count()\n",
    "huang_grade10_total_students = huang_grade_sorted[huang_grade_sorted[\"grade\"] == \"10th\"]\n",
    "huang_grade10th_total_students = huang_grade10_total_students.grade.count()\n",
    "huang_grade11_total_students = huang_grade_sorted[huang_grade_sorted[\"grade\"] == \"11th\"]\n",
    "huang_grade11th_total_students = huang_grade11_total_students.grade.count()\n",
    "huang_grade12_total_students = huang_grade_sorted[huang_grade_sorted[\"grade\"] == \"12th\"]\n",
    "huang_grade12th_total_students = huang_grade12_total_students.grade.count()\n",
    "huang_total9_reading_score = huang_grade9_total_students[\"reading_score\"].sum()\n",
    "huang_total10_reading_score = huang_grade10_total_students[\"reading_score\"].sum()\n",
    "huang_total11_reading_score = huang_grade11_total_students[\"reading_score\"].sum()\n",
    "huang_total12_reading_score = huang_grade12_total_students[\"reading_score\"].sum()\n",
    "huang_average9_reading_score = (huang_total9_reading_score / huang_grade9th_total_students)\n",
    "huang_average10_reading_score = (huang_total10_reading_score / huang_grade10th_total_students)\n",
    "huang_average11_reading_score = (huang_total11_reading_score / huang_grade11th_total_students)\n",
    "huang_average12_reading_score = (huang_total12_reading_score / huang_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 357,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Figueroa High School\n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "figueroa_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Figueroa High School\"]\n",
    "figueroa_grade_sorted = figueroa_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "figueroa_grade9_total_students = figueroa_grade_sorted[figueroa_grade_sorted[\"grade\"] == \"9th\"]\n",
    "figueroa_grade9th_total_students = figueroa_grade9_total_students.grade.count()\n",
    "figueroa_grade10_total_students = figueroa_grade_sorted[figueroa_grade_sorted[\"grade\"] == \"10th\"]\n",
    "figueroa_grade10th_total_students = figueroa_grade10_total_students.grade.count()\n",
    "figueroa_grade11_total_students = figueroa_grade_sorted[figueroa_grade_sorted[\"grade\"] == \"11th\"]\n",
    "figueroa_grade11th_total_students = figueroa_grade11_total_students.grade.count()\n",
    "figueroa_grade12_total_students = figueroa_grade_sorted[figueroa_grade_sorted[\"grade\"] == \"12th\"]\n",
    "figueroa_grade12th_total_students = figueroa_grade12_total_students.grade.count()\n",
    "figueroa_total9_reading_score = figueroa_grade9_total_students[\"reading_score\"].sum()\n",
    "figueroa_total10_reading_score = figueroa_grade10_total_students[\"reading_score\"].sum()\n",
    "figueroa_total11_reading_score = figueroa_grade11_total_students[\"reading_score\"].sum()\n",
    "figueroa_total12_reading_score = figueroa_grade12_total_students[\"reading_score\"].sum()\n",
    "figueroa_average9_reading_score = (figueroa_total9_reading_score / figueroa_grade9th_total_students)\n",
    "figueroa_average10_reading_score = (figueroa_total10_reading_score / figueroa_grade10th_total_students)\n",
    "figueroa_average11_reading_score = (figueroa_total11_reading_score / figueroa_grade11th_total_students)\n",
    "figueroa_average12_reading_score = (figueroa_total12_reading_score / figueroa_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 358,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Shelton High School\n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "shelton_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Shelton High School\"]\n",
    "shelton_grade_sorted = shelton_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "shelton_grade9_total_students = shelton_grade_sorted[shelton_grade_sorted[\"grade\"] == \"9th\"]\n",
    "shelton_grade9th_total_students = shelton_grade9_total_students.grade.count()\n",
    "shelton_grade10_total_students = shelton_grade_sorted[shelton_grade_sorted[\"grade\"] == \"10th\"]\n",
    "shelton_grade10th_total_students = shelton_grade10_total_students.grade.count()\n",
    "shelton_grade11_total_students = shelton_grade_sorted[shelton_grade_sorted[\"grade\"] == \"11th\"]\n",
    "shelton_grade11th_total_students = shelton_grade11_total_students.grade.count()\n",
    "shelton_grade12_total_students = shelton_grade_sorted[shelton_grade_sorted[\"grade\"] == \"12th\"]\n",
    "shelton_grade12th_total_students = shelton_grade12_total_students.grade.count()\n",
    "shelton_total9_reading_score = shelton_grade9_total_students[\"reading_score\"].sum()\n",
    "shelton_total10_reading_score = shelton_grade10_total_students[\"reading_score\"].sum()\n",
    "shelton_total11_reading_score = shelton_grade11_total_students[\"reading_score\"].sum()\n",
    "shelton_total12_reading_score = shelton_grade12_total_students[\"reading_score\"].sum()\n",
    "shelton_average9_reading_score = (shelton_total9_reading_score / shelton_grade9th_total_students)\n",
    "shelton_average10_reading_score = (shelton_total10_reading_score / shelton_grade10th_total_students)\n",
    "shelton_average11_reading_score = (shelton_total11_reading_score / shelton_grade11th_total_students)\n",
    "shelton_average12_reading_score = (shelton_total12_reading_score / shelton_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 360,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Hernandez High School\n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "her_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Hernandez High School\"]\n",
    "her_grade_sorted = her_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "her_grade9_total_students = her_grade_sorted[her_grade_sorted[\"grade\"] == \"9th\"]\n",
    "her_grade9th_total_students = her_grade9_total_students.grade.count()\n",
    "her_grade10_total_students = her_grade_sorted[her_grade_sorted[\"grade\"] == \"10th\"]\n",
    "her_grade10th_total_students = her_grade10_total_students.grade.count()\n",
    "her_grade11_total_students = her_grade_sorted[her_grade_sorted[\"grade\"] == \"11th\"]\n",
    "her_grade11th_total_students = her_grade11_total_students.grade.count()\n",
    "her_grade12_total_students = her_grade_sorted[her_grade_sorted[\"grade\"] == \"12th\"]\n",
    "her_grade12th_total_students = her_grade12_total_students.grade.count()\n",
    "her_total9_reading_score = her_grade9_total_students[\"reading_score\"].sum()\n",
    "her_total10_reading_score = her_grade10_total_students[\"reading_score\"].sum()\n",
    "her_total11_reading_score = her_grade11_total_students[\"reading_score\"].sum()\n",
    "her_total12_reading_score = her_grade12_total_students[\"reading_score\"].sum()\n",
    "her_average9_reading_score = (her_total9_reading_score / her_grade9th_total_students)\n",
    "her_average10_reading_score = (her_total10_reading_score / her_grade10th_total_students)\n",
    "her_average11_reading_score = (her_total11_reading_score / her_grade11th_total_students)\n",
    "her_average12_reading_score = (her_total12_reading_score / her_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 363,
   "metadata": {},
   "outputs": [],
   "source": [
    "# School Summary - Griffin High School\n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "griffin_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Griffin High School\"]\n",
    "griffin_grade_sorted = griffin_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "griffin_grade9_total_students = griffin_grade_sorted[griffin_grade_sorted[\"grade\"] == \"9th\"]\n",
    "griffin_grade9th_total_students = griffin_grade9_total_students.grade.count()\n",
    "griffin_grade10_total_students = griffin_grade_sorted[griffin_grade_sorted[\"grade\"] == \"10th\"]\n",
    "griffin_grade10th_total_students = griffin_grade10_total_students.grade.count()\n",
    "griffin_grade11_total_students = griffin_grade_sorted[griffin_grade_sorted[\"grade\"] == \"11th\"]\n",
    "griffin_grade11th_total_students = griffin_grade11_total_students.grade.count()\n",
    "griffin_grade12_total_students = griffin_grade_sorted[griffin_grade_sorted[\"grade\"] == \"12th\"]\n",
    "griffin_grade12th_total_students = griffin_grade12_total_students.grade.count()\n",
    "griffin_total9_reading_score = griffin_grade9_total_students[\"reading_score\"].sum()\n",
    "griffin_total10_reading_score = griffin_grade10_total_students[\"reading_score\"].sum()\n",
    "griffin_total11_reading_score = griffin_grade11_total_students[\"reading_score\"].sum()\n",
    "griffin_total12_reading_score = griffin_grade12_total_students[\"reading_score\"].sum()\n",
    "griffin_average9_reading_score = (griffin_total9_reading_score / griffin_grade9th_total_students)\n",
    "griffin_average10_reading_score = (griffin_total10_reading_score / griffin_grade10th_total_students)\n",
    "griffin_average11_reading_score = (griffin_total11_reading_score / griffin_grade11th_total_students)\n",
    "griffin_average12_reading_score = (griffin_total12_reading_score / griffin_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 366,
   "metadata": {},
   "outputs": [],
   "source": [
    "# School Summary - Wilson High School\n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "wilson_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Wilson High School\"]\n",
    "wilson_grade_sorted = wilson_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "wilson_grade9_total_students = wilson_grade_sorted[wilson_grade_sorted[\"grade\"] == \"9th\"]\n",
    "wilson_grade9th_total_students = wilson_grade9_total_students.grade.count()\n",
    "wilson_grade10_total_students = wilson_grade_sorted[wilson_grade_sorted[\"grade\"] == \"10th\"]\n",
    "wilson_grade10th_total_students = wilson_grade10_total_students.grade.count()\n",
    "wilson_grade11_total_students = wilson_grade_sorted[wilson_grade_sorted[\"grade\"] == \"11th\"]\n",
    "wilson_grade11th_total_students = wilson_grade11_total_students.grade.count()\n",
    "wilson_grade12_total_students = wilson_grade_sorted[wilson_grade_sorted[\"grade\"] == \"12th\"]\n",
    "wilson_grade12th_total_students = wilson_grade12_total_students.grade.count()\n",
    "wilson_total9_reading_score = wilson_grade9_total_students[\"reading_score\"].sum()\n",
    "wilson_total10_reading_score = wilson_grade10_total_students[\"reading_score\"].sum()\n",
    "wilson_total11_reading_score = wilson_grade11_total_students[\"reading_score\"].sum()\n",
    "wilson_total12_reading_score = wilson_grade12_total_students[\"reading_score\"].sum()\n",
    "wilson_average9_reading_score = (wilson_total9_reading_score / wilson_grade9th_total_students)\n",
    "wilson_average10_reading_score = (wilson_total10_reading_score / wilson_grade10th_total_students)\n",
    "wilson_average11_reading_score = (wilson_total11_reading_score / wilson_grade11th_total_students)\n",
    "wilson_average12_reading_score = (wilson_total12_reading_score / wilson_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 368,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Cabrera High School \n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "cabrera_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Cabrera High School\"]\n",
    "cabrera_grade_sorted = cabrera_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "cabrera_grade9_total_students = cabrera_grade_sorted[cabrera_grade_sorted[\"grade\"] == \"9th\"]\n",
    "cabrera_grade9th_total_students = cabrera_grade9_total_students.grade.count()\n",
    "cabrera_grade10_total_students = cabrera_grade_sorted[cabrera_grade_sorted[\"grade\"] == \"10th\"]\n",
    "cabrera_grade10th_total_students = cabrera_grade10_total_students.grade.count()\n",
    "cabrera_grade11_total_students = cabrera_grade_sorted[cabrera_grade_sorted[\"grade\"] == \"11th\"]\n",
    "cabrera_grade11th_total_students = cabrera_grade11_total_students.grade.count()\n",
    "cabrera_grade12_total_students = cabrera_grade_sorted[cabrera_grade_sorted[\"grade\"] == \"12th\"]\n",
    "cabrera_grade12th_total_students = cabrera_grade12_total_students.grade.count()\n",
    "cabrera_total9_reading_score = cabrera_grade9_total_students[\"reading_score\"].sum()\n",
    "cabrera_total10_reading_score = cabrera_grade10_total_students[\"reading_score\"].sum()\n",
    "cabrera_total11_reading_score = cabrera_grade11_total_students[\"reading_score\"].sum()\n",
    "cabrera_total12_reading_score = cabrera_grade12_total_students[\"reading_score\"].sum()\n",
    "cabrera_average9_reading_score = (cabrera_total9_reading_score / cabrera_grade9th_total_students)\n",
    "cabrera_average10_reading_score = (cabrera_total10_reading_score / cabrera_grade10th_total_students)\n",
    "cabrera_average11_reading_score = (cabrera_total11_reading_score / cabrera_grade11th_total_students)\n",
    "cabrera_average12_reading_score = (cabrera_total12_reading_score / cabrera_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 370,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Bailey High School \n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "bailey_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Bailey High School\"]\n",
    "bailey_grade_sorted = bailey_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "bailey_grade9_total_students = bailey_grade_sorted[bailey_grade_sorted[\"grade\"] == \"9th\"]\n",
    "bailey_grade9th_total_students = bailey_grade9_total_students.grade.count()\n",
    "bailey_grade10_total_students = bailey_grade_sorted[bailey_grade_sorted[\"grade\"] == \"10th\"]\n",
    "bailey_grade10th_total_students = bailey_grade10_total_students.grade.count()\n",
    "bailey_grade11_total_students = bailey_grade_sorted[bailey_grade_sorted[\"grade\"] == \"11th\"]\n",
    "bailey_grade11th_total_students = bailey_grade11_total_students.grade.count()\n",
    "bailey_grade12_total_students = bailey_grade_sorted[bailey_grade_sorted[\"grade\"] == \"12th\"]\n",
    "bailey_grade12th_total_students = bailey_grade12_total_students.grade.count()\n",
    "bailey_total9_reading_score = bailey_grade9_total_students[\"reading_score\"].sum()\n",
    "bailey_total10_reading_score = bailey_grade10_total_students[\"reading_score\"].sum()\n",
    "bailey_total11_reading_score = bailey_grade11_total_students[\"reading_score\"].sum()\n",
    "bailey_total12_reading_score = bailey_grade12_total_students[\"reading_score\"].sum()\n",
    "bailey_average9_reading_score = (bailey_total9_reading_score / bailey_grade9th_total_students)\n",
    "bailey_average10_reading_score = (bailey_total10_reading_score / bailey_grade10th_total_students)\n",
    "bailey_average11_reading_score = (bailey_total11_reading_score / bailey_grade11th_total_students)\n",
    "bailey_average12_reading_score = (bailey_total12_reading_score / bailey_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 372,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Holden High School \n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "holden_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Holden High School\"]\n",
    "holden_grade_sorted = holden_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "holden_grade9_total_students = holden_grade_sorted[holden_grade_sorted[\"grade\"] == \"9th\"]\n",
    "holden_grade9th_total_students = holden_grade9_total_students.grade.count()\n",
    "holden_grade10_total_students = holden_grade_sorted[holden_grade_sorted[\"grade\"] == \"10th\"]\n",
    "holden_grade10th_total_students = holden_grade10_total_students.grade.count()\n",
    "holden_grade11_total_students = holden_grade_sorted[holden_grade_sorted[\"grade\"] == \"11th\"]\n",
    "holden_grade11th_total_students = holden_grade11_total_students.grade.count()\n",
    "holden_grade12_total_students = holden_grade_sorted[holden_grade_sorted[\"grade\"] == \"12th\"]\n",
    "holden_grade12th_total_students = holden_grade12_total_students.grade.count()\n",
    "holden_total9_reading_score = holden_grade9_total_students[\"reading_score\"].sum()\n",
    "holden_total10_reading_score = holden_grade10_total_students[\"reading_score\"].sum()\n",
    "holden_total11_reading_score = holden_grade11_total_students[\"reading_score\"].sum()\n",
    "holden_total12_reading_score = holden_grade12_total_students[\"reading_score\"].sum()\n",
    "holden_average9_reading_score = (holden_total9_reading_score / holden_grade9th_total_students)\n",
    "holden_average10_reading_score = (holden_total10_reading_score / holden_grade10th_total_students)\n",
    "holden_average11_reading_score = (holden_total11_reading_score / holden_grade11th_total_students)\n",
    "holden_average12_reading_score = (holden_total12_reading_score / holden_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 376,
   "metadata": {},
   "outputs": [],
   "source": [
    "# School Summary - Pena High School \n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "pena_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Pena High School\"]\n",
    "pena_grade_sorted = pena_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "pena_grade9_total_students = pena_grade_sorted[pena_grade_sorted[\"grade\"] == \"9th\"]\n",
    "pena_grade9th_total_students = pena_grade9_total_students.grade.count()\n",
    "pena_grade10_total_students = pena_grade_sorted[pena_grade_sorted[\"grade\"] == \"10th\"]\n",
    "pena_grade10th_total_students = pena_grade10_total_students.grade.count()\n",
    "pena_grade11_total_students = pena_grade_sorted[pena_grade_sorted[\"grade\"] == \"11th\"]\n",
    "pena_grade11th_total_students = pena_grade11_total_students.grade.count()\n",
    "pena_grade12_total_students = pena_grade_sorted[pena_grade_sorted[\"grade\"] == \"12th\"]\n",
    "pena_grade12th_total_students = pena_grade12_total_students.grade.count()\n",
    "pena_total9_reading_score = pena_grade9_total_students[\"reading_score\"].sum()\n",
    "pena_total10_reading_score = pena_grade10_total_students[\"reading_score\"].sum()\n",
    "pena_total11_reading_score = pena_grade11_total_students[\"reading_score\"].sum()\n",
    "pena_total12_reading_score = pena_grade12_total_students[\"reading_score\"].sum()\n",
    "pena_average9_reading_score = (pena_total9_reading_score / pena_grade9th_total_students)\n",
    "pena_average10_reading_score = (pena_total10_reading_score / pena_grade10th_total_students)\n",
    "pena_average11_reading_score = (pena_total11_reading_score / pena_grade11th_total_students)\n",
    "pena_average12_reading_score = (pena_total12_reading_score / pena_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 378,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Wright High School \n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "wright_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Wright High School\"]\n",
    "wright_grade_sorted = wright_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "wright_grade9_total_students = wright_grade_sorted[wright_grade_sorted[\"grade\"] == \"9th\"]\n",
    "wright_grade9th_total_students = wright_grade9_total_students.grade.count()\n",
    "wright_grade10_total_students = wright_grade_sorted[wright_grade_sorted[\"grade\"] == \"10th\"]\n",
    "wright_grade10th_total_students = wright_grade10_total_students.grade.count()\n",
    "wright_grade11_total_students = wright_grade_sorted[wright_grade_sorted[\"grade\"] == \"11th\"]\n",
    "wright_grade11th_total_students = wright_grade11_total_students.grade.count()\n",
    "wright_grade12_total_students = wright_grade_sorted[wright_grade_sorted[\"grade\"] == \"12th\"]\n",
    "wright_grade12th_total_students = wright_grade12_total_students.grade.count()\n",
    "wright_total9_reading_score = wright_grade9_total_students[\"reading_score\"].sum()\n",
    "wright_total10_reading_score = wright_grade10_total_students[\"reading_score\"].sum()\n",
    "wright_total11_reading_score = wright_grade11_total_students[\"reading_score\"].sum()\n",
    "wright_total12_reading_score = wright_grade12_total_students[\"reading_score\"].sum()\n",
    "wright_average9_reading_score = (wright_total9_reading_score / wright_grade9th_total_students)\n",
    "wright_average10_reading_score = (wright_total10_reading_score / wright_grade10th_total_students)\n",
    "wright_average11_reading_score = (wright_total11_reading_score / wright_grade11th_total_students)\n",
    "wright_average12_reading_score = (wright_total12_reading_score / wright_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 380,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Rodriguez High School \n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "rod_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Wright High School\"]\n",
    "rod_grade_sorted = rod_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "rod_grade9_total_students = rod_grade_sorted[rod_grade_sorted[\"grade\"] == \"9th\"]\n",
    "rod_grade9th_total_students = rod_grade9_total_students.grade.count()\n",
    "rod_grade10_total_students = rod_grade_sorted[rod_grade_sorted[\"grade\"] == \"10th\"]\n",
    "rod_grade10th_total_students = rod_grade10_total_students.grade.count()\n",
    "rod_grade11_total_students = rod_grade_sorted[rod_grade_sorted[\"grade\"] == \"11th\"]\n",
    "rod_grade11th_total_students = rod_grade11_total_students.grade.count()\n",
    "rod_grade12_total_students = rod_grade_sorted[rod_grade_sorted[\"grade\"] == \"12th\"]\n",
    "rod_grade12th_total_students = rod_grade12_total_students.grade.count()\n",
    "rod_total9_reading_score = rod_grade9_total_students[\"reading_score\"].sum()\n",
    "rod_total10_reading_score = rod_grade10_total_students[\"reading_score\"].sum()\n",
    "rod_total11_reading_score = rod_grade11_total_students[\"reading_score\"].sum()\n",
    "rod_total12_reading_score = rod_grade12_total_students[\"reading_score\"].sum()\n",
    "rod_average9_reading_score = (rod_total9_reading_score / rod_grade9th_total_students)\n",
    "rod_average10_reading_score = (rod_total10_reading_score / rod_grade10th_total_students)\n",
    "rod_average11_reading_score = (rod_total11_reading_score / rod_grade11th_total_students)\n",
    "rod_average12_reading_score = (rod_total12_reading_score / rod_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 382,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Johnson High School \n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "johnson_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Wright High School\"]\n",
    "johnson_grade_sorted = johnson_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "johnson_grade9_total_students = johnson_grade_sorted[johnson_grade_sorted[\"grade\"] == \"9th\"]\n",
    "johnson_grade9th_total_students = johnson_grade9_total_students.grade.count()\n",
    "johnson_grade10_total_students = johnson_grade_sorted[johnson_grade_sorted[\"grade\"] == \"10th\"]\n",
    "johnson_grade10th_total_students = johnson_grade10_total_students.grade.count()\n",
    "johnson_grade11_total_students = johnson_grade_sorted[johnson_grade_sorted[\"grade\"] == \"11th\"]\n",
    "johnson_grade11th_total_students = johnson_grade11_total_students.grade.count()\n",
    "johnson_grade12_total_students = johnson_grade_sorted[johnson_grade_sorted[\"grade\"] == \"12th\"]\n",
    "johnson_grade12th_total_students = johnson_grade12_total_students.grade.count()\n",
    "johnson_total9_reading_score = johnson_grade9_total_students[\"reading_score\"].sum()\n",
    "johnson_total10_reading_score = johnson_grade10_total_students[\"reading_score\"].sum()\n",
    "johnson_total11_reading_score = johnson_grade11_total_students[\"reading_score\"].sum()\n",
    "johnson_total12_reading_score = johnson_grade12_total_students[\"reading_score\"].sum()\n",
    "johnson_average9_reading_score = (johnson_total9_reading_score / johnson_grade9th_total_students)\n",
    "johnson_average10_reading_score = (johnson_total10_reading_score / johnson_grade10th_total_students)\n",
    "johnson_average11_reading_score = (johnson_total11_reading_score / johnson_grade11th_total_students)\n",
    "johnson_average12_reading_score = (johnson_total12_reading_score / johnson_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 385,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# School Summary - Ford High School \n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "ford_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Wright High School\"]\n",
    "ford_grade_sorted = ford_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "ford_grade9_total_students = ford_grade_sorted[ford_grade_sorted[\"grade\"] == \"9th\"]\n",
    "ford_grade9th_total_students = ford_grade9_total_students.grade.count()\n",
    "ford_grade10_total_students = ford_grade_sorted[ford_grade_sorted[\"grade\"] == \"10th\"]\n",
    "ford_grade10th_total_students = ford_grade10_total_students.grade.count()\n",
    "ford_grade11_total_students = ford_grade_sorted[ford_grade_sorted[\"grade\"] == \"11th\"]\n",
    "ford_grade11th_total_students = ford_grade11_total_students.grade.count()\n",
    "ford_grade12_total_students = ford_grade_sorted[ford_grade_sorted[\"grade\"] == \"12th\"]\n",
    "ford_grade12th_total_students = ford_grade12_total_students.grade.count()\n",
    "ford_total9_reading_score = ford_grade9_total_students[\"reading_score\"].sum()\n",
    "ford_total10_reading_score = ford_grade10_total_students[\"reading_score\"].sum()\n",
    "ford_total11_reading_score = ford_grade11_total_students[\"reading_score\"].sum()\n",
    "ford_total12_reading_score = ford_grade12_total_students[\"reading_score\"].sum()\n",
    "ford_average9_reading_score = (ford_total9_reading_score / ford_grade9th_total_students)\n",
    "ford_average10_reading_score = (ford_total10_reading_score / ford_grade10th_total_students)\n",
    "ford_average11_reading_score = (ford_total11_reading_score / ford_grade11th_total_students)\n",
    "ford_average12_reading_score = (ford_total12_reading_score / ford_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 388,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Thomas High School\n",
    "reading_by_grade_pd = students_df.sort_values(\"grade\" and \"reading_score\")\n",
    "thomas_reading_by_grade = reading_by_grade_pd[reading_by_grade_pd[\"school\"] == \"Thomas High School\"]\n",
    "grade_sorted = thomas_reading_by_grade.sort_values(\"grade\", ascending=False)\n",
    "thomas_grade9_total_students = grade_sorted[grade_sorted[\"grade\"] == \"9th\"]\n",
    "thomas_grade9th_total_students = thomas_grade9_total_students.grade.count()\n",
    "thomas_grade10_total_students = grade_sorted[grade_sorted[\"grade\"] == \"10th\"]\n",
    "thomas_grade10th_total_students = thomas_grade10_total_students.grade.count()\n",
    "thomas_grade11_total_students = grade_sorted[grade_sorted[\"grade\"] == \"11th\"]\n",
    "thomas_grade11th_total_students = thomas_grade11_total_students.grade.count()\n",
    "thomas_grade12_total_students = grade_sorted[grade_sorted[\"grade\"] == \"12th\"]\n",
    "thomas_grade12th_total_students = thomas_grade12_total_students.grade.count()\n",
    "thomas_total9_reading_score = thomas_grade9_total_students[\"reading_score\"].sum()\n",
    "thomas_total10_reading_score = thomas_grade10_total_students[\"reading_score\"].sum()\n",
    "thomas_total11_reading_score = thomas_grade11_total_students[\"reading_score\"].sum()\n",
    "thomas_total12_reading_score = thomas_grade12_total_students[\"reading_score\"].sum()\n",
    "thomas_average9_reading_score = (thomas_total9_reading_score / thomas_grade9th_total_students)\n",
    "thomas_average10_reading_score = (thomas_total10_reading_score / thomas_grade10th_total_students)\n",
    "thomas_average11_reading_score = (thomas_total11_reading_score / thomas_grade11th_total_students)\n",
    "thomas_average12_reading_score = (thomas_total12_reading_score / thomas_grade12th_total_students)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 389,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>9th</th>\n",
       "      <th>10th</th>\n",
       "      <th>11th</th>\n",
       "      <th>12th</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Huang High School</th>\n",
       "      <td>81.290284</td>\n",
       "      <td>81.512386</td>\n",
       "      <td>81.417476</td>\n",
       "      <td>80.305983</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Figueroa High School</th>\n",
       "      <td>81.198598</td>\n",
       "      <td>81.408912</td>\n",
       "      <td>80.640339</td>\n",
       "      <td>81.384863</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Shelton High School</th>\n",
       "      <td>84.122642</td>\n",
       "      <td>83.441964</td>\n",
       "      <td>84.373786</td>\n",
       "      <td>82.781671</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Hernandez High School</th>\n",
       "      <td>80.866860</td>\n",
       "      <td>80.660147</td>\n",
       "      <td>81.396140</td>\n",
       "      <td>80.857143</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Griffin High School</th>\n",
       "      <td>83.369193</td>\n",
       "      <td>83.706897</td>\n",
       "      <td>84.288089</td>\n",
       "      <td>84.013699</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Wilson High School</th>\n",
       "      <td>83.939778</td>\n",
       "      <td>84.021452</td>\n",
       "      <td>83.764608</td>\n",
       "      <td>84.317673</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Cabrera High School</th>\n",
       "      <td>83.676136</td>\n",
       "      <td>84.253219</td>\n",
       "      <td>83.788382</td>\n",
       "      <td>84.287958</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Bailey High School</th>\n",
       "      <td>81.303155</td>\n",
       "      <td>80.907183</td>\n",
       "      <td>80.945643</td>\n",
       "      <td>80.912451</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Holden High School</th>\n",
       "      <td>83.677165</td>\n",
       "      <td>83.324561</td>\n",
       "      <td>83.815534</td>\n",
       "      <td>84.698795</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Pena High School</th>\n",
       "      <td>83.807273</td>\n",
       "      <td>83.612000</td>\n",
       "      <td>84.335938</td>\n",
       "      <td>84.591160</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Wright High School</th>\n",
       "      <td>83.833333</td>\n",
       "      <td>83.812757</td>\n",
       "      <td>84.156322</td>\n",
       "      <td>84.073171</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Rodriguez High School</th>\n",
       "      <td>83.833333</td>\n",
       "      <td>83.812757</td>\n",
       "      <td>84.156322</td>\n",
       "      <td>84.073171</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Johnson High School</th>\n",
       "      <td>83.833333</td>\n",
       "      <td>83.812757</td>\n",
       "      <td>84.156322</td>\n",
       "      <td>84.073171</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Ford High School</th>\n",
       "      <td>83.833333</td>\n",
       "      <td>83.812757</td>\n",
       "      <td>84.156322</td>\n",
       "      <td>84.073171</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Thomas High School</th>\n",
       "      <td>83.728850</td>\n",
       "      <td>84.254157</td>\n",
       "      <td>83.585542</td>\n",
       "      <td>83.831361</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "                             9th       10th       11th       12th\n",
       "Huang High School      81.290284  81.512386  81.417476  80.305983\n",
       "Figueroa High School   81.198598  81.408912  80.640339  81.384863\n",
       "Shelton High School    84.122642  83.441964  84.373786  82.781671\n",
       "Hernandez High School  80.866860  80.660147  81.396140  80.857143\n",
       "Griffin High School    83.369193  83.706897  84.288089  84.013699\n",
       "Wilson High School     83.939778  84.021452  83.764608  84.317673\n",
       "Cabrera High School    83.676136  84.253219  83.788382  84.287958\n",
       "Bailey High School     81.303155  80.907183  80.945643  80.912451\n",
       "Holden High School     83.677165  83.324561  83.815534  84.698795\n",
       "Pena High School       83.807273  83.612000  84.335938  84.591160\n",
       "Wright High School     83.833333  83.812757  84.156322  84.073171\n",
       "Rodriguez High School  83.833333  83.812757  84.156322  84.073171\n",
       "Johnson High School    83.833333  83.812757  84.156322  84.073171\n",
       "Ford High School       83.833333  83.812757  84.156322  84.073171\n",
       "Thomas High School     83.728850  84.254157  83.585542  83.831361"
      ]
     },
     "execution_count": 389,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "reading_scores_by_grade = pd.DataFrame({\"9th\" :[huang_average9_reading_score, figueroa_average9_reading_score, shelton_average9_reading_score, her_average9_reading_score, \n",
    "                                                griffin_average9_reading_score, wilson_average9_reading_score, cabrera_average9_reading_score, bailey_average9_reading_score, \n",
    "                                                holden_average9_reading_score, pena_average9_reading_score, wright_average9_reading_score, rod_average9_reading_score, \n",
    "                                                johnson_average9_reading_score, ford_average9_reading_score, thomas_average9_reading_score], \n",
    "                                        \"10th\" :[huang_average10_reading_score, figueroa_average10_reading_score, shelton_average10_reading_score, her_average10_reading_score, \n",
    "                                                 griffin_average10_reading_score, wilson_average10_reading_score, cabrera_average10_reading_score, bailey_average10_reading_score, \n",
    "                                                 holden_average10_reading_score, pena_average10_reading_score, wright_average10_reading_score, rod_average10_reading_score, \n",
    "                                                 johnson_average10_reading_score, ford_average10_reading_score, thomas_average10_reading_score], \n",
    "                                        \"11th\" :[huang_average11_reading_score, figueroa_average11_reading_score, shelton_average11_reading_score, her_average11_reading_score, \n",
    "                                                 griffin_average11_reading_score, wilson_average11_reading_score, cabrera_average11_reading_score, bailey_average11_reading_score, \n",
    "                                                 holden_average11_reading_score, pena_average11_reading_score, wright_average11_reading_score, rod_average11_reading_score, \n",
    "                                                 johnson_average11_reading_score, ford_average11_reading_score, thomas_average11_reading_score], \n",
    "                                        \"12th\" :[huang_average12_reading_score, figueroa_average12_reading_score, shelton_average12_reading_score, her_average12_reading_score, \n",
    "                                                 griffin_average12_reading_score, wilson_average12_reading_score, cabrera_average12_reading_score, bailey_average12_reading_score, \n",
    "                                                 holden_average12_reading_score, pena_average12_reading_score, wright_average12_reading_score, rod_average12_reading_score, \n",
    "                                                 johnson_average12_reading_score, ford_average12_reading_score, thomas_average12_reading_score]}, \n",
    "                                       columns=[\"9th\", \"10th\", \"11th\", \"12th\"], \n",
    "                                       index=[\"Huang High School\", \"Figueroa High School\", \"Shelton High School\", \"Hernandez High School\", \"Griffin High School\", \"Wilson High School\", \n",
    "                                      \"Cabrera High School\", \"Bailey High School\", \"Holden High School\", \"Pena High School\", \"Wright High School\", \"Rodriguez High School\", \n",
    "                                              \"Johnson High School\", \"Ford High School\", \"Thomas High School\"]) \n",
    "reading_scores_by_grade"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 431,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Average Math Score</th>\n",
       "      <th>Average Reading Score</th>\n",
       "      <th>% Passing Math</th>\n",
       "      <th>% Passing Reading</th>\n",
       "      <th>% Overall Passing Rate</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Per Student Budget</th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>$578.00</th>\n",
       "      <td>83.274201</td>\n",
       "      <td>83.989488</td>\n",
       "      <td>93.867718</td>\n",
       "      <td>96.539641</td>\n",
       "      <td>95.203679</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>$581.00</th>\n",
       "      <td>83.803279</td>\n",
       "      <td>83.814988</td>\n",
       "      <td>92.505855</td>\n",
       "      <td>96.252927</td>\n",
       "      <td>94.379391</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>$582.00</th>\n",
       "      <td>83.061895</td>\n",
       "      <td>83.975780</td>\n",
       "      <td>94.133477</td>\n",
       "      <td>97.039828</td>\n",
       "      <td>95.586652</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>$583.00</th>\n",
       "      <td>83.682222</td>\n",
       "      <td>83.955000</td>\n",
       "      <td>93.333333</td>\n",
       "      <td>96.611111</td>\n",
       "      <td>94.972222</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>$600.00</th>\n",
       "      <td>83.359455</td>\n",
       "      <td>83.725724</td>\n",
       "      <td>93.867121</td>\n",
       "      <td>95.854628</td>\n",
       "      <td>94.860875</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "                    Average Math Score  Average Reading Score  % Passing Math  \\\n",
       "Per Student Budget                                                              \n",
       "$578.00                      83.274201              83.989488       93.867718   \n",
       "$581.00                      83.803279              83.814988       92.505855   \n",
       "$582.00                      83.061895              83.975780       94.133477   \n",
       "$583.00                      83.682222              83.955000       93.333333   \n",
       "$600.00                      83.359455              83.725724       93.867121   \n",
       "\n",
       "                    % Passing Reading  % Overall Passing Rate  \n",
       "Per Student Budget                                             \n",
       "$578.00                     96.539641               95.203679  \n",
       "$581.00                     96.252927               94.379391  \n",
       "$582.00                     97.039828               95.586652  \n",
       "$583.00                     96.611111               94.972222  \n",
       "$600.00                     95.854628               94.860875  "
      ]
     },
     "execution_count": 431,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "scores_by_spending = school_summary.sort_values(\"Per Student Budget\", ascending=False)\n",
    "del scores_by_spending[\"Total Students\"]\n",
    "scores_mean = scores_by_spending.groupby(\"Per Student Budget\").mean()\n",
    "scores_mean.head(5)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 437,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Average Math Score</th>\n",
       "      <th>Average Reading Score</th>\n",
       "      <th>% Passing Math</th>\n",
       "      <th>% Passing Reading</th>\n",
       "      <th>% Overall Passing Rate</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Total Students</th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>427</th>\n",
       "      <td>83.803279</td>\n",
       "      <td>83.814988</td>\n",
       "      <td>92.505855</td>\n",
       "      <td>96.252927</td>\n",
       "      <td>94.379391</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>962</th>\n",
       "      <td>83.839917</td>\n",
       "      <td>84.044699</td>\n",
       "      <td>94.594595</td>\n",
       "      <td>95.945946</td>\n",
       "      <td>95.270270</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1468</th>\n",
       "      <td>83.351499</td>\n",
       "      <td>83.816757</td>\n",
       "      <td>93.392371</td>\n",
       "      <td>97.138965</td>\n",
       "      <td>95.265668</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1635</th>\n",
       "      <td>83.418349</td>\n",
       "      <td>83.848930</td>\n",
       "      <td>93.272171</td>\n",
       "      <td>97.308869</td>\n",
       "      <td>95.290520</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1761</th>\n",
       "      <td>83.359455</td>\n",
       "      <td>83.725724</td>\n",
       "      <td>93.867121</td>\n",
       "      <td>95.854628</td>\n",
       "      <td>94.860875</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "                Average Math Score  Average Reading Score  % Passing Math  \\\n",
       "Total Students                                                              \n",
       "427                      83.803279              83.814988       92.505855   \n",
       "962                      83.839917              84.044699       94.594595   \n",
       "1468                     83.351499              83.816757       93.392371   \n",
       "1635                     83.418349              83.848930       93.272171   \n",
       "1761                     83.359455              83.725724       93.867121   \n",
       "\n",
       "                % Passing Reading  % Overall Passing Rate  \n",
       "Total Students                                             \n",
       "427                     96.252927               94.379391  \n",
       "962                     95.945946               95.270270  \n",
       "1468                    97.138965               95.265668  \n",
       "1635                    97.308869               95.290520  \n",
       "1761                    95.854628               94.860875  "
      ]
     },
     "execution_count": 437,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "scores_by_size = school_summary.sort_values(\"Total Students\", ascending=False)\n",
    "del scores_by_size[\"Per Student Budget\"]\n",
    "size_mean = scores_by_size.groupby(\"Total Students\").mean()\n",
    "size_mean.head(5)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 448,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style>\n",
       "    .dataframe thead tr:only-child th {\n",
       "        text-align: right;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: left;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Average Math Score</th>\n",
       "      <th>Average Reading Score</th>\n",
       "      <th>% Passing Math</th>\n",
       "      <th>% Passing Reading</th>\n",
       "      <th>% Overall Passing Rate</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>School Type</th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Charter</th>\n",
       "      <td>83.473852</td>\n",
       "      <td>83.896421</td>\n",
       "      <td>93.620830</td>\n",
       "      <td>96.586489</td>\n",
       "      <td>95.103660</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>District</th>\n",
       "      <td>76.956733</td>\n",
       "      <td>80.966636</td>\n",
       "      <td>66.548453</td>\n",
       "      <td>80.799062</td>\n",
       "      <td>73.673757</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "             Average Math Score  Average Reading Score  % Passing Math  \\\n",
       "School Type                                                              \n",
       "Charter               83.473852              83.896421       93.620830   \n",
       "District              76.956733              80.966636       66.548453   \n",
       "\n",
       "             % Passing Reading  % Overall Passing Rate  \n",
       "School Type                                             \n",
       "Charter              96.586489               95.103660  \n",
       "District             80.799062               73.673757  "
      ]
     },
     "execution_count": 448,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "scores_by_type = school_summary.sort_values(\"School Type\", ascending=False)\n",
    "del scores_by_type[\"Per Student Budget\"]\n",
    "del scores_by_type[\"Total Students\"]\n",
    "type_mean = scores_by_type.groupby(\"School Type\").mean()\n",
    "type_mean.head(5)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": []
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
   "version": "3.5.4"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
