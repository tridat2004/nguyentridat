// script.js

// Mảng chứa thông tin các sản phẩm trong giỏ hàng
let cartItems = [];

// Hàm thêm sản phẩm vào giỏ hàng
function addToCart(productName, price) {
    // Tạo một đối tượng sản phẩm mới
    const newItem = {
        name: productName,
        price: price
    };

    // Thêm sản phẩm vào mảng giỏ hàng
    cartItems.push(newItem);

    // Cập nhật số lượng sản phẩm trong giỏ hàng và hiển thị thông tin giỏ hàng
    updateCart();
}

// Hàm cập nhật số lượng sản phẩm trong giỏ hàng và hiển thị thông tin giỏ hàng
function updateCart() {
    // Lấy thẻ div giỏ hàng
    const cartContainer = document.getElementById('cart-items');
    // Xóa nội dung cũ trong giỏ hàng
    cartContainer.innerHTML = '';

    // Tổng số tiền cần thanh toán
    let totalAmount = 0;

    // Lặp qua từng sản phẩm trong giỏ hàng để hiển thị và tính tổng giá tiền
    for (let item of cartItems) {
        // Hiển thị thông tin sản phẩm trong giỏ hàng
        const itemElement = document.createElement('div');
        itemElement.classList.add('cart-item');
        itemElement.innerHTML = `
            <span class="item-name">${item.name}</span>
            <span class="item-price">${item.price.toFixed(2)} VNĐ</span>
        `;
        cartContainer.appendChild(itemElement);

        // Tính tổng giá tiền
        totalAmount += item.price;
    }

    // Hiển thị tổng số tiền cần thanh toán
    const totalAmountElement = document.getElementById('total-amount');
    totalAmountElement.innerText = `Tổng tiền: ${totalAmount.toFixed(2)} VNĐ`;
}

// Hàm mua hàng
function buy() {
    // Kiểm tra nếu giỏ hàng không có sản phẩm
    if (cartItems.length === 0) {
        alert('Giỏ hàng của bạn đang trống. Vui lòng thêm sản phẩm vào giỏ hàng trước khi thanh toán.');
        return;
    }

    // Tính tổng số tiền cần thanh toán
    let totalAmount = 0;
    for (let item of cartItems) {
        totalAmount += item.price;
    }

    // Hiển thị thông báo về tổng số tiền cần thanh toán
    alert(`Tổng số tiền cần thanh toán: ${totalAmount.toFixed(2)} VNĐ`);

    // Xóa các sản phẩm trong giỏ hàng sau khi mua hàng thành công
    cartItems = [];
    // Cập nhật giỏ hàng
    updateCart();
}
