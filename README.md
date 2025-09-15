# n8n Local Market Research Workflows

A collection of n8n automation workflows for conducting local market research and creating newsletters based on Google Maps data.

## 📁 Workflows

### 1. LOCAL MARKET RESEARCH Workflow
**File:** `LOCAL MARKET RESEARCH.json`

This comprehensive workflow automates the collection and analysis of local business data from Google Maps using the Apify API. It processes business information and organizes it into structured Google Sheets for analysis.

**Key Features:**
- Fetches business data from Google Maps via Apify API
- Extracts and structures multiple data categories:
  - **Overview**: Business names, categories, ratings, reviews
  - **Contact Info**: Addresses, phones, websites, emails
  - **Social Media**: Instagram, Facebook, LinkedIn, YouTube, TikTok, Twitter, Pinterest links
  - **Ratings & Reviews**: Detailed review distributions and tags
  - **Customer Reviews**: Individual reviews with sentiment and metadata
  - **Popular Times**: Peak hours and live busyness data
  - **Competitive Analysis**: "People also search for" data
- Automatically creates and populates Google Sheets with organized data
- Uses AI (OpenAI) to generate insights and summaries

### 2. Local Newsletter Creation Workflow
**File:** `Local Newsletter creation workflow.json`

Transforms market research data into professional newsletters using AI-powered content generation.

**Key Features:**
- Takes research findings as input
- Uses OpenRouter Chat Model for content generation
- Creates polished, subscriber-facing newsletter articles
- Automatically formats content with:
  - Compelling headlines
  - Actionable insights (5 insider secrets/lessons)
  - Data-backed proof points with citations
  - Clear calls-to-action
- Exports to Google Docs for easy editing and distribution

## 🚀 Getting Started

### Prerequisites

1. **n8n Instance**: You need n8n installed locally or access to n8n cloud
2. **API Credentials Required**:
   - **Apify API**: For Google Maps data scraping
   - **Google OAuth**: For Sheets and Docs integration
   - **OpenAI API**: For AI-powered insights (optional)
   - **OpenRouter API**: For newsletter generation (optional)

### Installation

1. Import the workflow JSON files into your n8n instance:
   - Go to your n8n dashboard
   - Click "Import Workflow"
   - Upload the JSON files

2. Configure credentials:
   - Replace placeholder API keys
   - Set up OAuth connections for Google services
   - Configure AI service credentials if using

### ⚠️ Important Security Notes

**Before uploading to GitHub:**

1. **Remove ALL API Keys**: The workflows contain credential references that must be removed
2. **Replace with placeholders**: Use `YOUR_API_KEY_HERE` format
3. **Update the Apify URL**: Line 17 in LOCAL MARKET RESEARCH.json contains:
   ```
   https://api.apify.com/v2/datasets/datasetid/items?token=apify_(YOUR_API_KEY)
   ```
   Replace `datasetid` and `token` with placeholders

## 🔧 Configuration

### Apify Setup
1. Create an Apify account at https://apify.com
2. Set up Google Maps Scraper actor
3. Get your API token from account settings
4. Replace the placeholder in the workflow

### Google Services Setup
1. Enable Google Sheets API and Google Docs API in Google Cloud Console
2. Create OAuth 2.0 credentials
3. Configure in n8n's credentials section

### AI Services (Optional)
- **OpenAI**: For advanced data analysis
- **OpenRouter**: For newsletter content generation

## 📊 Workflow Outputs

### Market Research Workflow generates:
- **Overview Sheet**: Business listings with ratings and categories
- **Contact Sheet**: Complete contact information database
- **Social Media Sheet**: Social presence mapping
- **Ratings Analysis**: Review distributions and sentiment
- **Reviews Database**: Individual customer feedback
- **Competitor Analysis**: Related businesses and alternatives

### Newsletter Workflow produces:
- Professional newsletter drafts (400-600 words)
- Structured content with headlines and sections
- Data-backed insights with citations
- Ready-to-send Google Docs

## 🤝 Contributing

Feel free to submit issues and enhancement requests!

## 📝 License

This project is provided as-is for educational and business automation purposes.

## ⚡ Tips

- Start with a small dataset to test the workflows
- Monitor API usage to avoid rate limits
- Customize the AI prompts for your specific industry
- Regular backups of your Google Sheets data recommended

## 🔗 Resources

- [n8n Documentation](https://docs.n8n.io)
- [Apify Google Maps Scraper](https://apify.com/compass/google-maps-scraper)
- [Google Sheets API](https://developers.google.com/sheets/api)
- [OpenAI API Docs](https://platform.openai.com/docs)