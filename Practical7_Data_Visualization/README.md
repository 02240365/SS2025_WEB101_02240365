# 📊 Practical 7: Data Visualization

A comprehensive React-based analytics dashboard implementing various charting libraries to display data for analytics purposes.

## 🎯 Overview

This project demonstrates the implementation of different charting libraries in React to create an interactive analytics dashboard. The dashboard includes various chart types for data analysis, responsive design, and optimized performance.

## ✨ Features

- **📈 Monthly Sales Chart**: Line chart showing sales trends vs targets using Recharts
- **🥧 Product Category Chart**: Pie chart displaying market share by category using Recharts  
- **👥 Customer Acquisition Chart**: Bar chart comparing new vs returning customers using Recharts
- **📅 Weekly Visitors Chart**: Area chart showing visitor patterns using Recharts

## 🛠️ Technologies Used

- **React 18** with Next.js App Router
- **Recharts** - Primary charting library for responsive charts
- **TypeScript** - Type safety and better development experience
- **Tailwind CSS** - Styling and responsive design
- **Lucide React** - Icons (replaced with emojis as requested)

## 📦 Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/02240365/SS2025_WEB101_02240365.git
   cd Practical7_Data_Visualization
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Install required charting libraries**
   ```bash
   npm install recharts
   ```

4. **Run the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

5. **Open your browser**
   Navigate to `http://localhost:3000` to view the dashboard

## 📁 Project Structure

```
src/
├── app/
│   ├── page.tsx                 # Main dashboard page
│   └── layout.tsx              # Root layout
├── components/
│   ├── monthly-sales-chart.tsx      # Line chart component
│   ├── product-category-chart.tsx   # Pie chart component
│   ├── customer-acquisition-chart.tsx # Bar chart component
│   └── weekly-visitors-chart.tsx    # Area chart component
└── README.md
└── Reflection.md
```

## 🎨 Chart Components

### 1. Monthly Sales Chart (Line Chart)
- **Purpose**: Track monthly sales performance against targets
- **Features**: 
  - Dual line comparison (actual vs target)
  - Interactive tooltips
  - Responsive design
  - Custom styling with gradients

### 2. Product Category Chart (Pie Chart)
- **Purpose**: Visualize market share by product categories
- **Features**:
  - Custom label rendering with percentages
  - Color-coded segments
  - Interactive legend
  - Hover effects

### 3. Customer Acquisition Chart (Bar Chart)
- **Purpose**: Compare new vs returning customer acquisition
- **Features**:
  - Grouped bar chart
  - Quarterly data comparison
  - Custom tooltips
  - Rounded corners for modern look

### 4. Weekly Visitors Chart (Area Chart)
- **Purpose**: Show visitor patterns throughout the week
- **Features**:
  - Gradient fill areas
  - Multiple data series
  - Smooth curves
  - Interactive tooltips

## 🎯 Key Implementation Details

### Data Structure
Each chart component uses mock data structured for optimal visualization:

```javascript
// Example: Monthly Sales Data
const salesData = [
  { month: 'Jan', sales: 4000, target: 3800 },
  { month: 'Feb', sales: 3000, target: 3200 },
  // ... more data points
]
```

### Responsive Design
All charts use `ResponsiveContainer` from Recharts to ensure proper scaling across devices:

```jsx
<ResponsiveContainer width="100%" height="100%">
  <LineChart data={salesData}>
    {/* Chart components */}
  </LineChart>
</ResponsiveContainer>
```

### Custom Styling
Charts feature custom colors, gradients, and styling for professional appearance:

```jsx
<defs>
  <linearGradient id="colorVisitors" x1="0" y1="0" x2="0" y2="1">
    <stop offset="5%" stopColor="#3b82f6" stopOpacity={0.8}/>
    <stop offset="95%" stopColor="#3b82f6" stopOpacity={0.1}/>
  </linearGradient>
</defs>
```

## 🚀 Performance Optimizations

1. **Component Memoization**: Charts are optimized to prevent unnecessary re-renders
2. **Responsive Containers**: Efficient resizing without performance loss
3. **Minimal Dependencies**: Using only necessary chart libraries
4. **Static Data**: Mock data is defined outside components to prevent recreation

## 📱 Responsive Features

- **Mobile-First Design**: Charts adapt to different screen sizes
- **Grid Layout**: Responsive grid system using CSS Grid
- **Touch-Friendly**: Interactive elements optimized for touch devices
- **Scalable Text**: Font sizes adjust based on screen size

## 🎨 Customization Options

### Colors
Modify chart colors by updating the color values in each component:

```jsx
const categoryData = [
  { name: 'Electronics', value: 35, color: '#3b82f6' },
  // Update colors here
]
```

### Data
Replace mock data with real API data by updating the data arrays in each component.

### Styling
Customize appearance using Tailwind CSS classes in the main dashboard component.

## 🔧 Troubleshooting

### Common Issues

1. **Charts not rendering**: Ensure Recharts is properly installed
2. **Responsive issues**: Check container dimensions and ResponsiveContainer usage
3. **Data not displaying**: Verify data structure matches expected format

### Dependencies
Make sure all required packages are installed:

```bash
npm install recharts react react-dom next
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 🙏 Acknowledgments

- **Recharts** team for the excellent charting library
- **Next.js** team for the React framework
- **Tailwind CSS** for the utility-first CSS framework

