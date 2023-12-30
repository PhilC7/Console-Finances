# Console-Finances

For this exercise i was given a data set of a company's financial records.

I had to work out the following:

- The total number of months included in the dataset.

- The net total amount of Profit/Losses over the entire period.

- The average of the **changes** in Profit/Losses over the entire period.

  - I needed to track what the total change in Profit/Losses are from month to month and then find the average.
  - (`Total/(Number of months - 1)`)

- The greatest increase in Profit/Losses (date and difference in the amounts) over the entire period.

- The greatest decrease in Profit/Losses (date and difference in the amounts) over the entire period.

When opening the code in the browser the resulting analysis should look similar to the following:

```text
Financial Analysis
----------------
Total Months: 86
Total: $38382578
Average Change: -2315.12
Greatest Increase in Profits/Losses: Feb-2012 ($1926159)
Greatest Decrease in Profits/Losses: Sep-2013 ($-2196167)
```

# Useage

The website can be accessed [here](https://philc7.github.io/Console-Finances/)

To view the results you have to:

- Open the link up in the browser.
- Right click in the browser and select **_inspect_**.
- Select **_console_** and then you should see the output of the financial analysis.

### This is how the page should look.

![Alt text](<Screenshot 2023-12-30 at 11.48.25.png>)

# Credits

### Here are a few references that helped me to further understand basic Javascript.

#### Books

- Eloquent Javascript (Third Edition, 2019), Marijn Haverbeke
  - Page 69 (Array Loops).

#### Websites

- To set the decimal place of the average changes to 2 places. https://www.w3schools.com/jsref/jsref_tofixed.asp

- How to initialise a variable then use that to add up as I loop through an array.

  _For example here is a snippet of my code:_

        ```
        var difference = 0; //Initialise variable to be 0.

        for (let i = 0; i < finances.length; i++) {
        var balance = finances[i][1]; // Initialise balance to get current month's value.

        // Use a for loop to go through the array, missing the first month out.
        if (i > 0) {
            var previousBalance = finances[i - 1][1]; // Set variable to target the previous month
            var monthlyDifference = balance - previousBalance; // Set variable to calculate the current balance - previous months balance.
            difference += monthlyDifference; // Add the differences to the difference variable after each loop.
        }
        }
        ```

  https://www.freecodecamp.org/news/how-to-add-numbers-in-javascript-arrays/

# License

Please refer to the LICENSE in the repo.
