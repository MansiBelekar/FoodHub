# App title
st.title("FoodHub")

# Food options
food_options = {
    "Pizza": 299.00,
    "Burger": 149.00,
    "Salad": 99.00,
    "Sushi": 249.00,
    "Tacos": 199.00
}

# Beverage options
beverage_options = {
    "Soda": 20.00,
    "Water": 10.00,
    "Juice": 50.00,
    "Coffee": 30.00,
    "Tea": 10.00
}

# User input for food
st.header("Add your order")
food_selected = st.selectbox("Choose your food", list(food_options.keys()))
food_price = food_options[food_ordered]

# User input for beverage
st.header("Add beverage")
beverage_selected = st.selectbox("Choose your beverage", list(beverage_options.keys()))
beverage_price = beverage_options[beverage_ordered]

# Display user's selection
st.header("Your order in cart")
st.write(f"Food: {food_ordered} (${food_price:.2f})")
st.write(f"Beverage: {beverage_ordered} (${beverage_price:.2f})")
st.write(f"Total: ${(food_price + beverage_price):.2f}")

# Add a button to place order
if st.button("Place Order"):
    st.success("Your Order is Placed. Enjoy your food.")

# Add a button to clear order
if st.button("Clear Order"):
    st.write("Order is cleared!")
