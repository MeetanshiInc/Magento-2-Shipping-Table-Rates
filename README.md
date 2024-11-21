# **Magento 2 Shipping Table Rates**

Shipping costs are an integral part of an eCommerce store's pricing structure, and offering flexibility in shipping options can significantly enhance the customer experience. The **Magento 2 Shipping Table Rates** extension is designed to help merchants customize their shipping costs based on various parameters, such as destination, weight, and price, offering a more tailored experience for both the store owner and the customer.

In this article, we will delve into the features and functionality of the **Magento 2 Shipping Table Rates** extension, outlining how it can help merchants optimize their shipping strategies.

## **How It Works**

The **Magento 2 Shipping Table Rates** extension allows store owners to create shipping rules based on a range of conditions. These conditions can include shipping destination, weight of the product, cart total, or even the number of items in the cart. Store owners can upload CSV files to define custom shipping rates, which will automatically apply to orders during checkout.

The extension’s flexibility makes it suitable for various shipping scenarios, from local to international shipping, and helps merchants control costs based on specific rules.

## **Key Features**

* Customizable shipping rates based on conditions.  
* CSV import/export for easy rate management.  
* Real-time responsive shipping cost calculation.

## Custom Shipping Table Rates

The Magento 2 Shipping Table Rates extension allows store owners to define custom shipping rates for various shipping methods. By uploading a CSV file, merchants can set rates based on various criteria, including the weight of the items, cart value, or number of items in the cart. This flexibility ensures that the shipping costs are calculated accurately based on the customer’s specific order details.

## Easy CSV Import/Export

Store owners can import and export shipping table rates easily using CSV files. This feature simplifies the management of multiple shipping options and makes it easy to update rates in bulk.

## Multiple Shipping Methods

Magento 2 Shipping Table Rates supports multiple shipping methods, giving customers a variety of shipping options during checkout. These methods can include flat rate shipping, weight-based shipping, and price-based shipping. Store owners can choose which methods to offer based on customer location, cart contents, or other relevant conditions.

## Advanced Condition Settings

This extension enables store owners to set specific conditions for shipping rates based on various factors. You can apply conditions based on shipping destination, cart value, product weight, or even custom conditions.

## Real-Time Shipping Calculation

Once configured, the extension calculates shipping rates in real time based on the current cart and destination details. This ensures that customers always see accurate shipping costs before they complete their checkout process.

## **Extension Installation**

To install the Magento 2 Shipping Table Rates extension, follow these simple steps:

### **Step 1:**

Extract the zip folder and upload our extension to the root of your Magento 2 directory via FTP.

### **Step 2:**

Login to your SSH and run below commands step by step:

* php bin/magento setup:upgrade  
* For Magento version 2.0.x to 2.1.x \- php bin/magento setup:static-content:deploy  
* For Magento version 2.2.x & above \- php bin/magento setup:static-content:deploy –f  
* php bin/magento cache:flush

## **How to Configure Magento 2 Shipping Table Rates Extension**

### **Step 1: Add a Method to Import Shipping Table Rates**

To import Shipping Table Rates, navigate to **Sales \> Shipping Methods \> Shipping Table Rates** in your Magento admin panel. Click on the **Add Method** button to create a new method. All previously added and saved shipping table rate methods will be listed here for easy reference.

![Add a Method to Import Shipping Table Rates](https://github.com/user-attachments/assets/9d298433-6b3c-469c-b241-d3545e46b10f)

Follow these steps to configure the general settings for adding a new shipping table rate method:

* **Name**: Provide a name for the shipping table rate method. Use the variable `{day}` to display the estimated delivery days alongside the rates. The `{day}` variable will only show if the delivery days are specified in the shipping rates CSV.  
* **Status**: Set the status of the shipping table rate method to **Active** to enable it.  
* **Priority**: Define the priority for the method to determine its execution order.

#### **Handling Products with Different Shipping Types:**

* **Sum Up Rates**: Combine the rates for products with different shipping types in the cart.  
* **Select Maximal Rate**: Use the highest rate among the shipping types.  
* **Select Minimal Rate**: Use the lowest rate among the shipping types.  
* **Stores**: Choose the store views to which the shipping table rates will apply.  
* **Customer Groups**: Select the customer groups eligible for these shipping table rates.

![Handling Products with Different Shipping Types](https://github.com/user-attachments/assets/4c323d95-aa7e-48c9-88bc-d26b8dd2e4a3)

### **Import Shipping Table Rates**

To import Shipping Table Rates, follow these steps:

* **Navigate to the Import Tab**: Go to the **Import** tab to upload your Shipping Table Rates using a CSV file.  
* **Download the Sample CSV**: Download the sample CSV file to ensure your shipping rates CSV matches the required format.  
* **Delete Existing Rates**: When importing or saving changes, all existing rates will be removed. Ensure you have a backup if needed.  
* **Upload CSV File**: Upload the properly formatted CSV file containing your Shipping Table Rates.  
* **Save Changes**: Click **Save** or **Save and Continue Edit** to apply the imported Shipping Table Rates.

![Import Shipping Table Rates](https://github.com/user-attachments/assets/4b4c0880-9129-444c-8e17-b473476e8c6a)

### **Methods and Rates**

To view the imported Shipping Table Rates, navigate to the **Methods and Rates** tab. Below is an explanation of each grid column:

* **Country**: Displays the country where the rates will be applied.  
* **State**: Indicates the state applicable for the rates.  
* **City**: Lists the city to which the rates apply.  
* **Zip From \- To**: Specifies the range of postcodes where the rate applies. For example, "From: 20001 To: 30000" applies to all postcodes within that range. UK postcode formats are also supported.  
* **Price From \- To**: Defines the price range for which the shipping rate will apply, summarizing products with the same shipping type.  
* **Weight From \- To**: Sets the weight range for which the rate applies, based on the product's weight.  
* **Qty From \- To**: Specifies the quantity range in the cart for the applicable rate.  
* **Shipping Type**: If set to "All," the rate applies to all products regardless of their type.  
* **Rate**: Displays the fixed shipping rate applied to the entire order.  
* **PPP (Percentage Per Product Price)**: Calculates shipping as a percentage of the product price.  
* **FRPP (Fixed Rate Per Product Price)**: Calculates shipping by multiplying the product quantity in the cart by the FRPP value.  
* **FRPUW (Fixed Rate Per Unit of Weight)**: Calculates the shipping rate based on the product’s weight. For example, if FRPUW is set to 3.25 and the product weight is 4.15, the shipping cost will be `3.25 * 4.15 = $13.48`.  
* **Estimated Delivery (days)**: Indicates the estimated delivery days for the shipping method. These values can be displayed on the frontend by using the `{day}` variable in the **Name** field.

![Methods and Rates](https://github.com/user-attachments/assets/4f2739ee-9cad-42d4-b057-b7fcc16dcd65)

### **Download Shipping Rates CSV**

If you need to download the saved Shipping Table Rates in the future, follow these steps:

* Navigate to **Sales \> Shipping Table Rates** in your Magento admin panel.  
* Select the existing method for which you want to download the rates.  
* Go to the **Import** tab.  
* Click the **Download** button next to the "Existing Shipping Rates CSV" option to download the file.

![Download Shipping Rates CSV](https://github.com/user-attachments/assets/6dc81e1f-2311-4f3f-9c2c-8314b98e8461)

### **Step 2: Configure Settings**

![Configure Settings](https://github.com/user-attachments/assets/14180ef3-5820-4a98-9c56-ee7c4fa4cf29)

To configure the Shipping Table Rates method in Magento 2, follow these steps:

1. **Log in to Magento 2 Admin Panel**:  
   Navigate to **Stores \> Configuration \> Sales \> Shipping Methods \> Shipping Table Rates** to access the configuration settings.  
2. **Settings to Configure**:  
* **Enabled for Checkout**: Set to **Yes** to enable the Shipping Table Rates method for checkout.  
* **Title**: Enter the title for the shipping method, which will appear on the checkout page.  
* **Ship to Applicable Countries**: Choose the countries where the shipping method will be available.  
* **Displayed Error Message**: Specify the error message to display if the shipping method is unavailable.  
* **Allow Free Shipping Promotions**: Select **Yes** to apply free shipping rules from shopping cart promotions.  
* **Ignore Price and Quantity of Virtual Products**: Choose **Yes** to exclude virtual products' price and quantity when calculating shipping rates.  
* **Compare Post Codes as**:  
  * **Range**: Treat the postcodes in the CSV as a range (e.g., 05101 to 05109 or AB10 to AB50).  
  * **Regular Expression**: Treat the postcodes as patterns or expressions (e.g., BB%, %1B%, B%A%).  
* **Use Price AFTER Discount**: Set to **Yes** to calculate shipping based on the discounted price.  
* **Use Price INCLUDING Tax**: Set to **Yes** to calculate shipping based on the price inclusive of taxes.  
* **Use Only One Shipping Type for the Method**:  
  * If **Yes**, when the cart contains products with different shipping types, the rate for **Shipping Types \= All** will apply.  
* **Sort Order**: Define the display order for this shipping method on the frontend.

### **Step 3: Create Shipping Type Options**

* **Create Shipping Type Attribute Options**

To create options for the Shipping Type attribute, follow these steps:

1. Navigate to Catalog \> Products \> Attributes in the Magento admin panel.  
2. Select the action Edit Product Attribute for Shipping Type.  
3. Go to the Manage Label/Options section to define the required options for the attribute.

![Create Shipping Type Attribute Options](https://github.com/user-attachments/assets/a501e5ac-f915-4a28-8aad-955d04cf6251)

* **Configure Shipping Type Options**  
  * Go to the **Properties** tab within the **Attribute Information** menu.  
  * Click the **Add Option** button to add new shipping type options, as illustrated below.

![Configure Shipping Type Options](https://github.com/user-attachments/assets/e371091f-a8d6-486d-94d4-b4d32bc5bba8)

* **Assign Shipping Type to Products :** After creating shipping type options, assign the appropriate attribute value to each product to enable Shipping Table Rates calculations.

![Assign Shipping Type to Products](https://github.com/user-attachments/assets/badb73c2-0312-4c67-8ed8-b9e50f2c1035)

### **Step 4: Check Shipping Table Rates on the Frontend**

After configuring the settings and enabling the shipping method, add a product to the cart to view the calculated Shipping Table Rates applied on the frontend.

* **Shipping Table Rates on the Cart Page :** When a customer adds products to their cart, the Shipping Table Rates will be displayed on the cart page.

![Shipping Table Rates on the Cart Page](https://github.com/user-attachments/assets/b7f7f97f-d94f-47a6-8931-4f50b85d3d0d)

* **Shipping Table Rates on the Checkout Page :** As the customer proceeds to checkout, the Shipping Table Rates will also be displayed on the checkout page.

![Shipping Table Rates on the Checkout Page](https://github.com/user-attachments/assets/11626253-1c8f-44b9-b446-bbfb9d69357d)

* **Shipping Table Rates on the My Account Page :** After an order is successfully placed using the Shipping Table Rates method, the shipping details will be displayed under the "My Orders" tab in the My Account section.

![Shipping Table Rates on the My Account Page](https://github.com/user-attachments/assets/c045cb6c-8e00-459f-b0fd-7babe2734d5a)

### **Step 5: Shipping Table Rates Details in Admin Order View**

In addition to the frontend, the admin can view the Shipping Table Rates details in the backend by navigating to **Sales \> Orders \> Order View**.

![Shipping Table Rates Details in Admin Order View](https://github.com/user-attachments/assets/c0410b07-0a78-4f0c-915d-0f04b5b620e2)

## Download the [Magento 2 Shipping Table Rates](https://meetanshi.com/magento-2-shipping-table-rates.html) Extension

