## optimization-purchase
### I'll commit the first release as soon as possible (Probably on 19/07)
# Description
This is a code written in MATLAB language which I wrote after my studies of Operations Research during the 2nd year of my Bachelor Degree. It's a simple scalable code that focuses on optimizing the purchase of a given set of items.</br></br>
It can optimize the total spending for anything that has to be bought, the main goal is to help the decision-making process of choosing where to buy partial or complete sets of items from, given every shop with its prices and shipping costs.</br></br>
p.s. I wrote this code for my own needs, because I had to buy a complete collection of books.
# How to use
<ol>
<li><h3> Execute through executable file</h3>
  Just unpack the zip anywhere, fill the csv files inside the data folder and run the .exe
</li>
<li><h3> Run the code itself (Useful to add improvements or make the code fits your own needs)</h3>
<strong>Read Carefully</strong> To run the code, your MATLAB enviroment <strong>has</strong> to include the following toolboxes:
<ul><li><strong>Optimization Toolbox</strong></li> <li><strong>Global Optimization Toolbox</strong></li></ul>
The main function takes as input a String containing the name of a data folder located in the same path of the executable function. This folder <strong>has to contain 3 or 4 csv files</strong> called "shipping.csv", "demand.csv", "shoprice.csv" and if needed "discount.csv".</br></br>
(If no string is given as parameter to the function, it will use as <strong>default folder "data"</strong>)</li></ol>
<h2> How to format csv files </h2>
<h3> No entry can be missing otherwise code won't run </h3>
<ul>
  <li><strong>shipping.csv</strong> This csv file has to cointain in its rows the following entries:</li>
    <strong>[ shop_name, shipping_cost1, shipping_cost2, max_items1, max_items2, min_items2, min_total, vat_value ]</strong>
    <ul style="list-style-type:square;">
      <li><strong>shop_name</strong>: quite self-explanatory lmao</li>
      <li><strong>shipping_cost1</strong>: Standard shipping cost to buy from the shop</li>
      <li><strong>shipping_cost2</strong>: Shipping cost achievable through spending enough money or buying enough items</li>
      <li><strong>max_items1</strong>: Maximum number of items that can be bought at shipping_cost1</li>
      <li><strong>max_items2</strong>: Maximum number of items that can be bought at shipping_cost2</li>
      <li><strong>min_items2</strong>: Minimum quantity of items that have to be bought to get access to the shipping_cost2</li>
      <li><strong>min_total</strong>: Minimum value that has to be spent to get access to the shipping_cost2</li>
      <li><strong>vat_value</strong>: If not already included in the provided prices set this as the value of the VAT percentage (Example 0.04)</li>
    </ul></br>

  <li><strong>demand.csv</strong> This csv file has to cointain in its rows the following entries:</li>
    <strong>[ quantity ]</strong>
    <ul style="list-style-type:square;">
      <li><strong>quantity</strong>: this value indicate the amount of item referring to the row number needed</li>
    </ul></br>

  <li><strong>shoprice.csv</strong> This csv file has to cointain in its rows the following entries:</li>
    <strong>[ id_shop, id_item, price_value ]</strong>
    <ul style="list-style-type:square;">
      <li><strong>id_shop</strong>: This is the id reffering to the row of shipping.csv containing the shop that has the item</li>
      <li><strong>id_item</strong>: This value refers to the row of demand.csv cointaining the items availabe at the shop id_shop</li>
      <li><strong>price_value</strong>: Price of the item id_item availabe at the shop id_shop</li>
    </ul><strong>If an item is not available from a particular shop just don't insert the entry</strong></br></br>
    
  <li><strong>discount.csv (Not Necessary)</strong> This csv file has to cointain in its rows the following entries:</li>
    <strong>[ id_shop, discount_percentage, discount_float, min_spending , min_quantity]</strong>
    <ul style="list-style-type:square;">
      <li><strong>id_shop</strong>: Set this entry as the number referring to the row of the shop in shipping.csv you have a discount for</li>
      <li><strong>discount_percentage</strong>: If your discount is a percentage over the total one, set this as the percentage of the discount you have got (Example 0.20)</li>
      <li><strong>discount_float</strong>: If your discount is an amount to be decreased, set this entry as the float amount corresponding to the discount you have got (Example 4.50)</li>
      <li><strong>min_spending</strong>: Set this value as the minimum amount that has to be spent to get access to the discount</li>
      <li><strong>min_quantity</strong>: Set this value as the minimum quantity of items that have to be bought to get access to the discount</li>

### Assign to every void value zero
  </ul>
</ul>



# Work in progress
