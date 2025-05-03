📝 Assignment: Database Design and Normalization

-- Question 01

INSERT INTO ProductDetail_1NF (orderID, CustomerName, Product)
VALUES
(101, 'John Doe', 'Laptop'),
(101, 'john Doe', 'Mouse'),
(102, 'jane Smith', 'Tablet'),
(102, 'jane Smith', 'Keyboard'),
(102, 'jane Smith', 'Mouse'),
(103, 'Emily Clark', 'Phone');


-- Question 02

CREATE TABLE OrderDetails_2NF (
Orderid INT NOT NULL,
Product VARCHAR(100),
Quantity INT,
FOREIGN KEY (OrderId) REFERENCES orders(orderId)
ON DELETE CASCADE
ON UPDATE CASCADE 
) ENGINE= 	innoDB;
