# Lab 13

## Basic C# 

The following tasks should be completeed using Visual Studio C# IDE.  Start a new project every time you start a new task. Every time you cerate a new project, you should use the option for Windows Application Project.

## Task 1

Write a program that creates a GUI with a text box for a number between 1 and 9 and a button.  When you click on the button, the program should display the name of the number (i.e. one, two, three, etc.) by using if statement.  

--------------------------

## Task 2 

Add error checking for the input data to the above program.  When the number is less than 1 or bigger than 9, this is not a valid number input, use a message box to display an appropriate message.

Message boxes are often used to display some information to the user.  A simple way to use the message box is as follows:

```c#
MessageBox.Show(“Hello World!”); or 
MessageBox.Show(myName); where myName is a string variable.
```

------------

## Task 3

Rewrite the above program (by starting a new project) using a switch statement.

-----------------

## Task 4

Write a program that creates a GUI with a text box for the number of the month (from 1 to 12) and a button.  The program should display the name of the season (winter, spring, summer, autumn).  Use a switch statement. Include error checking code for the month.  

----

## HERE BE A SOLUTUON

<details>

<summary>Click if you have given up</summary>

```c#
public partial class Form1 : Form
{
    // Declare an array of numbered words
    public string[] units = { "One", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine" };
    public string[] months = { "Winter", "Spring", "Summmer", "Autumn" };

    public Form1()
    {
        InitializeComponent();
        number_rtb.Text = "";
        month_rtb.Text = "";
    }

    private void button1_Click(object sender, EventArgs e)
    {
        // try to convert the text from the tb to an int, if failure call messagebox and clear tb 
        // else we are then going to check if the number is less than 1 or greater than 9, if true then throw a messagebox
        // else convert the number to text
        try
        {
            int number = Convert.ToInt32(number_rtb.Text);

            if (number < 1 || number > 9)
            {
                MessageBox.Show("Please input a number between 1 and 9", "Number Input", MessageBoxButtons.OK, MessageBoxIcon.Error);
            }
            else
            {
                //number_lb.Text = numifconversion(number);
                number_lb.Text = numswitchconversion(number);
            }
        }
        catch (Exception)
        {
            MessageBox.Show("Please input a number only", "Number Input", MessageBoxButtons.OK, MessageBoxIcon.Error);
            number_rtb.Text = "";
        }
    }

    /// <summary>
    /// Takes an int and converts to a word using a switch statement
    /// </summary>
    /// <param name="num"></param>
    /// <returns></returns>
    public string numswitchconversion(int num)
    {
        switch (num)
        {
            case (1):
                return units[0];
            case (2):
                return units[1];
            case (3):
                return units[2];
            case (4):
                return units[3];
            case (5):
                return units[4];
            case (6):
                return units[5];
            case (7):
                return units[6];
            case (8):
                return units[7];
            default:
                return units[8];
        }
    }


    /// <summary>
    /// Takes an int and converts to a word using an if statement
    /// </summary>
    /// <param name="num"></param>
    /// <returns></returns>
    public string numifconversion(int num)
    {
        if (num == 1)
        {
            return units[0];
        }
        else if (num == 2)
        {
            return units[1];
        }
        else if (num == 3)
        {
            return units[2];
        }
        else if (num == 4)
        {
            return units[3];
        }
        else if (num == 5)
        {
            return units[4];
        }
        else if (num == 6)
        {
            return units[5];
        }
        else if (num == 7)
        {
            return units[6];
        }
        else if (num == 8)
        {
            return units[7];
        }
        else 
        {
            return units[8];
        }
    }

    private void button2_Click(object sender, EventArgs e)
    {
        // try to convert the text from the tb to an int, if failure call messagebox and clear tb 
        // else we are then going to check if the number is less than 1 or greater than 12, if true then throw a messagebox
        // else convert the number to text
        try
        {
            int number = Convert.ToInt32(month_rtb.Text);

            if (number < 1 || number > 12)
            {
                MessageBox.Show("Please input a number between 1 and 12", "Number Input", MessageBoxButtons.OK, MessageBoxIcon.Error);
            }
            else
            {
                //number_lb.Text = ifconversion(number);
                month_lb.Text = monthswitchconversion(number);
            }
        }
        catch (Exception)
        {
            MessageBox.Show("Please input a number only", "Number Input", MessageBoxButtons.OK, MessageBoxIcon.Error);
            month_rtb.Text = "";
        }
    }

    /// <summary>
    /// Takes an int and converts to a month using a switch statement
    /// </summary>
    /// <param name="num"></param>
    /// <returns></returns>
    public string monthswitchconversion(int num)
    {
        // winter =[0] spring =[1] summer=[2] autumn =[3]
        switch (num)
        {
            case (1):
                return months[0];
            case (2):
                return months[0];
            case (3):
                return months[1];
            case (4):
                return months[1];
            case (5):
                return months[1];
            case (6):
                return months[2];
            case (7):
                return months[2];
            case (8):
                return months[2];
            case (9):
                return months[3];
            case (10):
                return months[3];
            case (11):
                return months[3];
            default:
                return months[0];
        }
    }
}
```

</details>