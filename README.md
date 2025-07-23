# Fashion Review System

A comprehensive web-based tool for reviewing, editing, and approving fashion items from multiple collections. This system allows manual quality control and data curation for fashion e-commerce applications.

## 🚀 Features

### Multi-Collection Management
- **Celebrity Lookbook**: Curated celebrity street style outfits
- **Seasonal Capsules**: Season-specific fashion collections
- **Event Ready**: Special occasion and event outfits
- **Everyday Essentials**: Daily wear and basic wardrobe items

### Product Review & Approval
- ✅ **Approval System**: Check/uncheck items for approval
- 📝 **Inline Editing**: Edit product titles and prices directly
- 🔍 **Smart Filtering**: Filter by collection, availability, or approval status
- 📊 **Real-time Statistics**: Track approved vs total items

### Availability Tracking
- 🟢 **Available**: Items confirmed in stock
- 🔴 **Out of Stock**: Items confirmed unavailable
- 🟡 **Status Unknown**: Items without availability data
- 📈 **Confidence Scores**: AI-powered availability confidence ratings

### Data Export
- 📤 **Clean Export**: Export only approved items to JSON
- 🔄 **Edit Preservation**: All manual edits included in export
- 📝 **Timestamped Files**: Automatic filename timestamping

## 🛠️ Technology Stack

- **Frontend**: Vanilla HTML, CSS, JavaScript
- **Data Format**: JSON
- **Server**: Python HTTP server (development)
- **No Dependencies**: Pure web technologies, no frameworks needed

## 🚦 Getting Started

### Prerequisites
- Python 3.x (for local server)
- Modern web browser
- Fashion data JSON files

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/explore-page-review.git
   cd explore-page-review
   ```

2. **Start the local server**
   ```bash
   python3 -m http.server 8000
   ```

3. **Access the application**
   Open your browser and navigate to `http://localhost:8000`

## 📁 Project Structure

```
explore-page-review/
├── index.html                                    # Main application file
├── fin_output_celebrity_lookbook_backup.json     # Celebrity fashion data
├── fin_output_seasonal_capsules.json             # Seasonal collections
├── fin_output_event_ready_edits.json            # Event-ready outfits
├── fin_output_everyday_essentials.json          # Daily essentials
├── README.md                                     # This file
└── .gitignore                                   # Git ignore rules
```

## 🎯 How to Use

### 1. Review Collections
- Browse through different fashion collections using the filter buttons
- View Pinterest inspiration images and product details
- Check availability status and confidence scores

### 2. Edit Product Data
- Click "📝 Edit Mode: OFF" to enable editing
- Click on product titles or prices to edit them directly
- Press Enter or click away to save changes
- See "● EDITED" indicators for modified items

### 3. Approve Items
- Click the checkbox on product images to approve/disapprove
- Use "Approved Only" filter to review selected items
- Watch real-time statistics update

### 4. Export Final Data
- Click "Export Approved Items" when review is complete
- Download includes all approved items with edits applied
- Use exported JSON for production systems

## 📊 Data Structure

### Product Object
```json
{
  "product_id": "unique_identifier",
  "title": "Product Name",
  "price": "$XX*",
  "brand": "Brand Name",
  "retailer": "Store Name",
  "link": "https://store.com/product",
  "img_url": "https://image.url",
  "garment_type": "tops|bottoms|accessories|footwear",
  "stock_status": {
    "is_available": true,
    "confidence": 0.95,
    "reason": "Availability check reason",
    "last_checked": "2025-01-01T00:00:00.000000"
  }
}
```

### Outfit Object
```json
{
  "outfit_title": "Outfit Name",
  "outfit_pinterest_img_url": "https://pinterest-image.url",
  "outfit_pinterest_url": "https://pinterest.com/pin/123",
  "shopping_results": [/* array of products */]
}
```

## 🔧 Development

### Adding New Collections
1. Add JSON file to project directory
2. Update `jsonFiles` array in `index.html`
3. Add corresponding filter button if needed

### Customizing Styles
- Edit CSS variables in `<style>` section of `index.html`
- Modify color schemes, spacing, or layout as needed
- All styles are contained in the single HTML file

### Extending Functionality
- Add new product fields by updating the editing system
- Implement additional filters in the `renderOutfits()` function
- Enhance export format in `exportApprovedItems()`

## 📈 Statistics Tracked

- **Total Outfits**: Number of complete outfit combinations
- **Total Items**: Individual products across all collections
- **Available Items**: Products confirmed in stock
- **Approved Items**: Products marked for approval
- **Edited Items**: Products with manual modifications

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Pinterest for outfit inspiration data
- Various retailers for product information
- AI-powered availability checking system

---

**Built for efficient fashion curation and quality control** 🎨✨ 