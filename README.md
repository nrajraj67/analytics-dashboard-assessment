# Electric Vehicle Analytics Dashboard

A complete analytics dashboard for visualizing Electric Vehicle (EV) population data built for the MapUp Analytics Dashboard Assessment. This dashboard provides comprehensive insights into EV types, manufacturer trends, registration patterns, and electric range distributions.

## 🚀 Live Dashboard

**Dashboard URL**: [Add your deployed URL here after deployment]

## ⚡ Quick Start

**Fastest way to view:**
1. Download the project
2. Open `index.html` in your browser
3. Done!

**See QUICKSTART.md for detailed instructions**

## Features

- **Interactive Visualizations**: Charts showing EV type distribution, top manufacturers, year trends, and range analysis
- **Dynamic Filtering**: Filter data by model year and manufacturer
- **Key Statistics**: Quick overview cards showing total vehicles, BEV/PHEV percentages, and average range
- **Detailed Table View**: Browse individual vehicle records with key details
- **Responsive Design**: Works on desktop, tablet, and mobile devices

## Key Insights

1. **EV Type Distribution**: Visual breakdown of Battery Electric Vehicles (BEV) vs Plug-in Hybrid Electric Vehicles (PHEV)
2. **Manufacturer Analysis**: Top 5 manufacturers by vehicle count
3. **Registration Trends**: Year-over-year growth in EV registrations
4. **Range Analysis**: Distribution of electric range capabilities across vehicles

## Technology Stack

- **Frontend**: React.js (via CDN)
- **Data Parsing**: PapaParse for CSV handling
- **Visualizations**: Chart.js for interactive charts
- **Styling**: Custom CSS with modern design
- **Fonts**: DM Sans and Outfit from Google Fonts

## Project Structure

```
ev-analytics-dashboard/
├── index.html              # Main dashboard file
├── data/                   # CSV data directory
│   └── ev-data.csv        # Electric vehicle dataset
├── package.json           # Project configuration
└── README.md             # Project documentation
```

## Installation & Setup

### Local Development

1. Clone this repository:
```bash
git clone [your-repo-url]
cd ev-analytics-dashboard
```

2. Open the dashboard:
```bash
# Option 1: Open directly in browser
open index.html

# Option 2: Use a local server
npx http-server -p 3000
```

3. Navigate to `http://localhost:3000` in your browser

### Using Your Own Data

To use your own EV dataset:

1. Place your CSV file in the `data/` directory
2. Update the data loading section in `index.html`:
   - Modify the file path in the Papa.parse function
   - Ensure your CSV has these columns: VIN, Make, Model, Model Year, Electric Vehicle Type, Electric Range, City, County

## Deployment

This dashboard can be deployed to any static hosting service:

### Netlify (Recommended)
1. Push code to GitHub
2. Connect repository to Netlify
3. Deploy automatically

### Vercel
1. Install Vercel CLI: `npm i -g vercel`
2. Run: `vercel`
3. Follow prompts

### GitHub Pages
1. Push to GitHub repository
2. Enable GitHub Pages in repository settings
3. Select main branch as source

### Other Options
- AWS S3 + CloudFront
- Azure Static Web Apps
- Google Cloud Storage
- Render

## Data Source

Dataset: Electric Vehicle Population Data
Source: Washington State Department of Licensing (DOL)

## Features Breakdown

### Dashboard Components

1. **Header Section**
   - Title and description
   - Clean, professional design

2. **Filter Controls**
   - Year selector (all years or specific year)
   - Manufacturer selector (all makes or specific make)

3. **Statistics Cards**
   - Total vehicle count
   - BEV percentage
   - PHEV percentage
   - Average electric range

4. **Visualization Charts**
   - Doughnut chart: EV type distribution
   - Bar chart: Top 5 manufacturers
   - Line chart: Registration trend by year
   - Bar chart: Electric range distribution

5. **Data Table**
   - Shows first 10 filtered records
   - Displays key vehicle information
   - Interactive and scrollable

## Design Decisions

### Visual Design
- **Color Scheme**: Dark theme with blue and purple accents for modern, professional look
- **Typography**: DM Sans for body text, Outfit for headings
- **Layout**: Responsive grid system that adapts to screen sizes
- **Animations**: Subtle hover effects and transitions for better UX

### Technical Decisions
- **Single File Application**: All code in one HTML file for easy deployment
- **CDN Libraries**: No build process required, faster setup
- **Chart.js**: Reliable, well-documented charting library
- **Vanilla React**: Simple state management without complex dependencies

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Performance

- Lightweight: < 100KB total size (excluding external libraries)
- Fast loading: All assets from CDN
- Efficient rendering: React for optimal updates

## Future Enhancements

Potential features for future versions:
- CSV upload functionality
- More advanced filters (city, county, range)
- Geographic map visualization
- Export filtered data to CSV
- Dark/light theme toggle
- Comparison mode for multiple datasets

## Contributing

This is an assessment project, but suggestions are welcome!

## License

MIT License - feel free to use this code for your own projects.

## Contact

For questions about this project, please reach out via the assessment submission form.

---

**Note**: This dashboard was created as part of the MapUp Analytics Dashboard Assessment. The implementation focuses on clean code, good design principles, and effective data visualization.
