# Flask Shop App

## 项目概述
Flask Shop App是一个基于Flask框架开发的电子商务网站，支持用户注册登录、商品管理、购物车、订单处理和支付流程。

## 技术架构

### 后端技术
- **Flask**: Python Web框架
- **Flask-SQLAlchemy**: ORM数据库工具
- **Flask-Security**: 用户认证和授权管理
- **Flask-Mail**: 邮件发送功能
- **Flask-Babel**: 国际化支持
- **Flask-Uploads**: 文件上传管理
- **SQLAlchemy**: 数据库ORM
- **PostgreSQL**: 关系型数据库

### 前端技术
- **Jinja2**: 模板引擎
- **HTML5/CSS3**: 页面结构和样式
- **Bootstrap**: 响应式UI框架

## 项目结构

```
flask_shop/
├── static/
│   └── login.css
├── templates/
│   ├── layout.html
│   ├── search.html
│   ├── sell.html
│   ├── product.html
│   ├── order.html
│   ├── orders.html
│   ├── pay.html
│   └── security/
│       ├── login_user.html
│       └── register_user.html
├── __init__.py
├── flask_shop.py
└── requirements.txt
```

## 核心功能

### 1. 用户管理
- 用户注册和登录
- 角色管理（卖家/买家）
- 个人信息管理

### 2. 商品管理
- 商品发布（卖家）
- 商品图片上传
- 商品搜索和浏览

### 3. 订单管理
- 购物车功能
- 订单创建和管理
- 订单状态跟踪

### 4. 支付系统
- 支付信息收集
- 支付状态管理

## 数据库设计

### 主要数据表
- **user**: 用户信息
- **role**: 角色信息
- **role_user**: 用户-角色关联
- **product**: 商品信息
- **order**: 订单信息
- **bought_product**: 订单商品关联
- **address**: 地址信息

## 快速开始

### 环境要求
- Python 3.6+
- PostgreSQL

### 安装步骤
1. 克隆仓库
   ```bash
   git clone https://github.com/sangjiexun/Flask-Shop-Master.git
   cd Flask-Shop-Master
   ```

2. 安装依赖
   ```bash
   pip install -r flask_shop/requirements.txt
   ```

3. 配置数据库
   修改 `flask_shop.py` 中的数据库连接信息：
   ```python
   SQLALCHEMY_DATABASE_URI='postgresql://shop_writer:password@localhost:5432/shop'
   ```

4. 初始化数据库
   ```bash
   flask initdb
   ```

5. 运行应用
   ```bash
   python flask_shop/flask_shop.py
   ```

## 部署说明

### 生产环境部署
- 使用Gunicorn作为WSGI服务器
- 使用Nginx作为反向代理
- 配置HTTPS
- 启用生产模式

### 环境变量配置
- `FLASK_SHOP_CFG`: 配置文件路径
- 邮件服务器配置
- 数据库连接信息

## 许可证

MIT License

---

# Flask Shop App

## Project Overview
Flask Shop App is an e-commerce website developed based on the Flask framework, supporting user registration and login, product management, shopping cart, order processing, and payment流程.

## Technical Architecture

### Backend Technologies
- **Flask**: Python Web framework
- **Flask-SQLAlchemy**: ORM database tool
- **Flask-Security**: User authentication and authorization management
- **Flask-Mail**: Email sending functionality
- **Flask-Babel**: Internationalization support
- **Flask-Uploads**: File upload management
- **SQLAlchemy**: Database ORM
- **PostgreSQL**: Relational database

### Frontend Technologies
- **Jinja2**: Template engine
- **HTML5/CSS3**: Page structure and styling
- **Bootstrap**: Responsive UI framework

## Project Structure

```
flask_shop/
├── static/
│   └── login.css
├── templates/
│   ├── layout.html
│   ├── search.html
│   ├── sell.html
│   ├── product.html
│   ├── order.html
│   ├── orders.html
│   ├── pay.html
│   └── security/
│       ├── login_user.html
│       └── register_user.html
├── __init__.py
├── flask_shop.py
└── requirements.txt
```

## Core Features

### 1. User Management
- User registration and login
- Role management (seller/buyer)
- Personal information management

### 2. Product Management
- Product publishing (seller)
- Product image upload
- Product search and browsing

### 3. Order Management
- Shopping cart functionality
- Order creation and management
- Order status tracking

### 4. Payment System
- Payment information collection
- Payment status management

## Database Design

### Main Data Tables
- **user**: User information
- **role**: Role information
- **role_user**: User-role association
- **product**: Product information
- **order**: Order information
- **bought_product**: Order-product association
- **address**: Address information

## Quick Start

### Environment Requirements
- Python 3.6+
- PostgreSQL

### Installation Steps
1. Clone the repository
   ```bash
   git clone https://github.com/sangjiexun/Flask-Shop-Master.git
   cd Flask-Shop-Master
   ```

2. Install dependencies
   ```bash
   pip install -r flask_shop/requirements.txt
   ```

3. Configure database
   Modify the database connection information in `flask_shop.py`:
   ```python
   SQLALCHEMY_DATABASE_URI='postgresql://shop_writer:password@localhost:5432/shop'
   ```

4. Initialize database
   ```bash
   flask initdb
   ```

5. Run the application
   ```bash
   python flask_shop/flask_shop.py
   ```

## Deployment Instructions

### Production Environment Deployment
- Use Gunicorn as WSGI server
- Use Nginx as reverse proxy
- Configure HTTPS
- Enable production mode

### Environment Variables Configuration
- `FLASK_SHOP_CFG`: Configuration file path
- Email server configuration
- Database connection information

## License

MIT License