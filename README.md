# App title
st.title("Food and Beverage App")

# Food options
food_options = {
    "Pizza": 10.99,
    "Burger": 9.99,
    "Salad": 8.99,
    "Sushi": 12.99,
    "Tacos": 11.99
}

# Beverage options
beverage_options = {
    "Soda": 2.99,
    "Water": 1.99,
    "Juice": 3.99,
    "Coffee": 2.49,
    "Tea": 2.49
}

# User input for food
st.header("Select your food")
food_selected = st.selectbox("Choose your food", list(food_options.keys()))
food_price = food_options[food_selected]

# User input for beverage
st.header("Select your beverage")
beverage_selected = st.selectbox("Choose your beverage", list(beverage_options.keys()))
beverage_price = beverage_options[beverage_selected]

# Display user's selection
st.header("Your order")
st.write(f"Food: {food_selected} (${food_price:.2f})")
st.write(f"Beverage: {beverage_selected} (${beverage_price:.2f})")
st.write(f"Total: ${(food_price + beverage_price):.2f}")

# Add a button to place order
if st.button("Place Order"):
    st.success("Order placed successfully!")

# Add a button to clear order
if st.button("Clear Order"):
    st.write("Order cleared!")
