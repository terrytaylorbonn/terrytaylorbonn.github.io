# DocSearch Integration Setup Guide

This repository now includes DocSearch integration for enhanced search functionality on your ZiptieAI.com site.

## What's Been Added

1. **DocSearch Integration Files:**
   - `_includes/docsearch.html` - Main DocSearch configuration and styling
   - `_data/docsearch.yml` - Configuration data file (optional)
   - `search.html` - Fallback search page

2. **Modified Files:**
   - `_includes/head.html` - Added DocSearch include
   - `_includes/header.html` - Added search box container
   - `_includes/footer.html` - Cleaned up

## Setup Instructions

### Option 1: Apply for Free DocSearch (Recommended)

1. **Apply for DocSearch** at https://docsearch.algolia.com/apply/
   - Fill out the form with your site details
   - Make sure your site is publicly accessible
   - DocSearch is free for open source and documentation sites

2. **Wait for Approval** (usually 1-2 weeks)
   - Algolia will crawl your site and create an index
   - You'll receive credentials via email

3. **Update Configuration** in `_includes/docsearch.html`:
   ```javascript
   appId: 'YOUR_ACTUAL_APP_ID',
   apiKey: 'YOUR_ACTUAL_SEARCH_API_KEY',
   indexName: 'your_actual_index_name',
   ```

### Option 2: Set Up Your Own Algolia Index

1. **Create Algolia Account** at https://www.algolia.com/
2. **Create Application and Index**
3. **Set up Web Crawler** or use Algolia CLI to index your content
4. **Update Configuration** with your credentials

## Testing

1. **Local Testing:**
   ```bash
   bundle exec jekyll serve
   ```
   - The search box will appear but won't work until you add real credentials
   - Use the fallback search at `/search/` for basic functionality

2. **Production:**
   - Deploy to GitHub Pages
   - Once DocSearch credentials are added, the search will be fully functional

## Features Included

- **Responsive Design** - Works on desktop and mobile
- **Keyboard Navigation** - Use arrow keys, Enter, and Escape
- **Recent Searches** - Saves recent search queries
- **Custom Styling** - Matches your site's theme
- **Fallback Search** - Basic search functionality without Algolia

## Customization

### Styling
Modify the CSS in `_includes/docsearch.html` to match your theme:

```css
.DocSearch-Button {
  /* Customize search button appearance */
}
```

### Search Behavior
Update the `searchParameters` in `_includes/docsearch.html`:

```javascript
searchParameters: {
  hitsPerPage: 20,
  facetFilters: ['category:documentation'], // Filter by category
  typoTolerance: true // Enable typo tolerance
}
```

### Translations
Modify the `translations` object to change text and labels.

## Troubleshooting

1. **Search box appears but doesn't work:**
   - Check browser console for errors
   - Verify DocSearch credentials are correct
   - Ensure your site is properly indexed

2. **Search box doesn't appear:**
   - Check that `#docsearch` container exists in header
   - Verify DocSearch CSS/JS files are loading
   - Check browser developer tools for errors

3. **No search results:**
   - Verify your index name is correct
   - Check if your content has been crawled/indexed
   - Try the debug mode: `debug: true`

## Next Steps

1. Apply for DocSearch or set up your own Algolia index
2. Update the configuration with real credentials
3. Test the search functionality
4. Customize styling and behavior as needed
5. Consider adding structured data to improve search results

## Resources

- [DocSearch Documentation](https://docsearch.algolia.com/docs/what-is-docsearch)
- [Algolia Documentation](https://www.algolia.com/doc/)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
