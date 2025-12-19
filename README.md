# 💰 Splitwise Expense Dashboard

A powerful, AI-powered expense tracking and analysis dashboard for Splitwise data. Built with vanilla HTML, CSS, and JavaScript - no dependencies required!

## ✨ Features

### 📊 Expense Analytics
- **Interactive Visualizations**: Category breakdown with color-coded intensity
- **Top 10 Biggest Expenses**: Filterable and removable for "what-if" analysis
- **Year-over-Year Comparisons**: Track spending trends across years
- **Multi-Category Filtering**: Select multiple categories with intuitive checkboxes
- **Time-based Filtering**: Filter by year, month, quarter, or all time
- **Search Functionality**: Find expenses by description

### 💸 Partner Financial Tracking
- **Total Paid by Person**: See who actually paid for what
- **Who Owes Whom**: Clear breakdown of balances between partners
- **Payment Transfers Separated**: Internal transfers excluded from expense analysis

### 🤖 AI-Powered Features

#### Smart Categorization
- Automatically recategorizes "Other" expenses using Claude AI
- Learns from existing categories
- Provides summary of changes before applying
- Smart rules for common categories (streaming, groceries, cash, etc.)

#### AI Financial Advisor
- **Spending Analysis**: Identifies areas for improvement
- **Savings Calculator**: Projects S&P 500 ETF returns over 10 years
- **Pattern Recognition**: Detects shopping habits and frequency
- **Inflation Comparison**: Compares increases to German inflation rates
- **Actionable Recommendations**: Personalized, data-driven advice
- **Frequency Analysis**: Tracks convenience shopping (Flink, Uber, etc.)

### 🎨 User Experience
- Beautiful gradient design
- Responsive layout
- Dark/light themed sections
- Interactive charts with hover effects
- Loading animations
- Real-time filtering

## 🚀 Getting Started

### Prerequisites
- A Splitwise CSV export
- (Optional) Claude API key for AI features

### Installation
1. Download `expense-dashboard.html`
2. Open it in any modern web browser
3. That's it! No server or installation needed.

### Usage

1. **Upload CSV**: Click "Upload CSV File" and select your Splitwise export
2. **AI Categorization** (Optional): 
   - If "Other" categories are detected, enter your Claude API key
   - Click "Recategorize with AI" to improve categories
   - Review and apply changes
3. **Explore Your Data**: Use filters, search, and visualizations
4. **Get AI Insights**: Click "Get Financial Insights" for personalized advice

## 📁 CSV Format

Your Splitwise CSV should have these columns:
```
Date, Description, Category, Cost, Currency, Person1, Person2
```

Example:
```csv
Date,Description,Category,Cost,Currency,John,Joe
2024-01-15,Netflix,TV/Phone/Internet,15.99,EUR,7.99,8.00
2024-01-16,Rewe Groceries,Groceries,45.50,EUR,22.75,22.75
```

**Note**: Person columns represent each person's share/portion of the expense. Negative values mean that person owes money.

## 🔑 Getting a Claude API Key

1. Go to [Anthropic Console](https://console.anthropic.com/)
2. Sign up or log in
3. Navigate to API Keys
4. Create a new key
5. Copy and paste into the dashboard

**Cost**: Claude API usage is pay-as-you-go. Typical analysis costs < €0.05.

## 🎯 Key Features Explained

### Payment Separation
The dashboard automatically separates "Payment" category transactions (money transfers between partners) from actual expenses. This ensures:
- Accurate expense totals
- Clean category breakdowns
- Correct AI insights
- Separate payment tracking section

### Color-Coded Intensity
Expense bars use opacity to show magnitude:
- **Darker/More Opaque**: Higher expenses
- **Lighter/More Transparent**: Lower expenses

### Year Filter Integration
When you filter by year, ALL features respect it:
- Statistics update
- Charts recalculate
- AI insights focus on that year
- YoY comparisons adjust

### Frequency Analysis
The AI tracks how often you use specific merchants:
- **Flink**: Convenience delivery (expensive)
- **Rewe, Edeka, Aldi, Lidl**: Grocery stores
- **Uber, Lieferando, Wolt**: Food delivery

It then provides specific savings recommendations based on your habits.

## 🛠️ Technical Details

- **No Backend Required**: 100% client-side
- **Privacy First**: All data stays in your browser
- **Modern JavaScript**: ES6+ features
- **Responsive Design**: Works on desktop, tablet, mobile
- **API Integration**: Direct Anthropic API calls (your key stays local)

## 📊 AI Categorization Rules

The AI follows these rules when recategorizing:
1. Cash/ATM → "Cash" (never TV/Internet or General)
2. Streaming (Netflix, Spotify) → "TV/Phone/Internet"
3. Home items (candles, furniture) → "Furniture" or "Home"
4. Tourist attractions → "Tickets" or "Entertainment"
5. Co-working spaces → "Services" or "Office"
6. Groceries → "Groceries" or "Food and drink"

## 🎓 Example Use Cases

### Monthly Review
1. Filter to current month
2. Review category breakdown
3. Check "Who Owes Whom"
4. Get AI insights for improvement areas

### Annual Planning
1. Filter to last year
2. Compare with previous year using YoY feature
3. Get AI financial advisor recommendations
4. Project 10-year savings

### What-If Analysis
1. Remove specific expenses (vacation, one-time purchases)
2. See how totals change
3. Use "Reset Removed Items" to restore

## 🤝 Contributing

This is a single-file HTML dashboard. To contribute:
1. Fork the repository
2. Make your changes to `expense-dashboard.html`
3. Test thoroughly in multiple browsers
4. Submit a pull request

## 📝 License

MIT License - feel free to use, modify, and distribute!

## 🙏 Acknowledgments

- Built with ❤️ for better financial awareness
- Powered by Claude AI (Anthropic)
- Inspired by Splitwise

## 📧 Support

If you encounter issues or have questions:
1. Check the CSV format matches the expected structure
2. Ensure you're using a modern browser (Chrome, Firefox, Safari, Edge)
3. For AI features, verify your API key is valid

---

**Made with 💜 for smarter expense tracking**
