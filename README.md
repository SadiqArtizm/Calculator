
# TypeScript Code

import inquirer from 'inquirer';

const questions = [
  {
    type: 'number',
    name: 'num1',
    message: 'Please Enter Your First Number',
  },
  {
    type: 'number',
    name: 'num2',
    message: 'Please Enter Your Second Number',
  },
  {
    type: 'list',
    name: 'operator',
    choices: ['add(+)', 'multiply(*)', 'divide(/)', 'subtract(-)'],
    message: 'Select Your Operator',
  },
];

const { num1, num2, operator }: { num1: number; num2: number; operator: string } = await inquirer.prompt(questions);

let result: number | undefined;

if (operator === 'add(+)') {
  result = num1 + num2;
} else if (operator === 'multiply(*)') {
  result = num1 * num2;
} else if (operator === 'divide(/)') {
  if (num2 !== 0) {
    result = num1 / num2;
  } else {
    console.error('Error: Cannot divide by zero');
    process.exit(1);
  }
} else if (operator === 'subtract(-)') {
  result = num1 - num2;
} else {
  console.error('Error: Invalid operator');
  process.exit(1);
}


if (result !== undefined) {
  console.log(`Result: ${result}`);
}
# Java ScriptCode

import inquirer from 'inquirer';
const questions = [
    {
        type: 'number',
        name: 'num1',
        message: 'Please Enter Your First Number',
    },
    {
        type: 'number',
        name: 'num2',
        message: 'Please Enter Your Second Number',
    },
    {
        type: 'list',
        name: 'operator',
        choices: ['add(+)', 'multiply(*)', 'divide(/)', 'subtract(-)'],
        message: 'Select Your Operator',
    },
];
const { num1, num2, operator } = await inquirer.prompt(questions);
let result;
if (operator === 'add(+)') {
    result = num1 + num2;
}
else if (operator === 'multiply(*)') {
    result = num1 * num2;
}
else if (operator === 'divide(/)') {
    if (num2 !== 0) {
        result = num1 / num2;
    }
    else {
        console.error('Error: Cannot divide by zero');
        process.exit(1);
    }
}
else if (operator === 'subtract(-)') {
    result = num1 - num2;
}
else {
    console.error('Error: Invalid operator');
    process.exit(1);
}
if (result !== undefined) {
    console.log(`Result: ${result}`);
}

