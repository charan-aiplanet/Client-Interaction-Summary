
# 📋 Client Interaction Summary Generator

An AI-powered multi-agent system for generating professional client interaction summaries using Azure OpenAI and AutoGen. This application helps Relationship Managers (RMs) create structured, consistent summaries from client meetings, calls, and other interactions.

## 🌟 Features

### 🤖 **Multi-Agent Processing**
- **Document Analyzer Agent**: Extracts key information and structure
- **Summary Generator Agent**: Creates formatted summaries following RM standards
- **Quality Reviewer Agent**: Ensures accuracy and completeness
- **Real-time Agent Monitoring**: Visual dashboard showing agent interactions

### 📄 **Document Support**
- **Multiple Formats**: PDF, DOCX, and TXT file processing
- **Smart Text Extraction**: Handles various document structures
- **Document Preview**: Shows extracted content before processing

### 🔐 **Authentication & Security**
- **Secure Login System**: Session-based authentication
- **Persistent Sessions**: Stays logged in until tab closure
- **Demo Credentials**: Quick access for testing

### 📚 **History Management**
- **Processing History**: Tracks all generated summaries
- **Quick Access**: Load any previous summary instantly
- **Smart Storage**: Maintains last 50 processed documents

### 📊 **Professional Output**
- **Standardized Format**: Consistent summary structure
- **Export Options**: Download as DOCX or PDF
- **Clean Formatting**: Professional appearance without markdown artifacts

### ⚙️ **Azure OpenAI Integration**
- **Multiple Models**: Support for GPT-4, GPT-4 Turbo, GPT-3.5 Turbo
- **Flexible Configuration**: Environment variables or Streamlit secrets
- **Error Handling**: Comprehensive error management

## 🚀 Quick Start

### Prerequisites
- Python 3.8 or higher
- Azure OpenAI API access
- API key and endpoint from Azure

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd client-interaction-summary-generator
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure Azure OpenAI**
   
   **Option A: Environment Variables (.env file)**
   ```env
   AZURE_OPENAI_API_KEY=your_api_key_here
   AZURE_OPENAI_ENDPOINT=https://your-resource.openai.azure.com/
   AZURE_OPENAI_API_VERSION=2024-02-15-preview
   AZURE_OPENAI_MODEL=gpt-4
   ```

   **Option B: Streamlit Secrets**
   
   Create `.streamlit/secrets.toml`:
   ```toml
   AZURE_OPENAI_API_KEY = "your_api_key_here"
   AZURE_OPENAI_ENDPOINT = "https://your-resource.openai.azure.com/"
   AZURE_OPENAI_API_VERSION = "2024-02-15-preview"
   AZURE_OPENAI_MODEL = "gpt-4"
   ```

4. **Run the application**
   ```bash
   streamlit run app.py
   ```

5. **Access the application**
   - Open your browser to `http://localhost:8501`
   - Login with demo credentials: Username: `admin`, Password: `password123`

## 📖 Usage Guide

### 🔑 **Authentication**
1. Open the application in your browser
2. Enter credentials on the login screen
3. Demo credentials: Username: `admin`, Password: `password123`

### 📤 **Document Processing**
1. **Upload Document**: Select PDF, DOCX, or TXT file
2. **Optional Template**: Provide custom format template
3. **Generate Summary**: Click the "Generate Summary" button
4. **Monitor Progress**: Watch real-time agent interactions
5. **Download Results**: Export as DOCX or PDF

### 📚 **History Management**
- **View History**: Check sidebar for previous summaries
- **Load Summary**: Click any history item to reload
- **Download Historical**: Export any previous summary

### ⚙️ **Configuration**
- **Model Selection**: Choose Azure OpenAI model in sidebar
- **Processing Options**: Toggle detailed logs and auto-refresh
- **Session Management**: Logout when finished

## 📋 Summary Format

The application generates summaries in this standardized format:

```
Client Interaction Summary
Date of Meeting: [Date]
Participants: [List of attendees]
Client Name: [Client organization]
Meeting Type: [Call/Meeting/Other]

1. Objectives of the Meeting
[Meeting goals and purpose]

2. Key Discussion Points
[Main topics discussed]

3. Decisions Made
[Agreements and resolutions]

4. Action Items (for RM and Client)
[Specific tasks with responsible parties]

Key Takeaways
[Summary of important outcomes]
```

## 🏗️ Architecture

### **Multi-Agent System**
```
Document Input → Document Analyzer → Summary Generator → Quality Reviewer → Final Output
                        ↓                    ↓                    ↓
                   Extract Info      Create Summary      Review & Polish
```

### **Technology Stack**
- **Frontend**: Streamlit
- **AI Engine**: Azure OpenAI (GPT-4/GPT-3.5)
- **Agent Framework**: AutoGen
- **Document Processing**: PyPDF2, python-docx
- **Export**: ReportLab (PDF), python-docx (DOCX)

## 🔧 Configuration Options

### **Environment Variables**
| Variable | Description | Default |
|----------|-------------|---------|
| `AZURE_OPENAI_API_KEY` | Azure OpenAI API key | Required |
| `AZURE_OPENAI_ENDPOINT` | Azure OpenAI endpoint URL | Required |
| `AZURE_OPENAI_API_VERSION` | API version | `2024-02-15-preview` |
| `AZURE_OPENAI_MODEL` | Model name | `gpt-4` |

### **Supported Models**
- `gpt-4` - Highest quality, best for complex summaries
- `gpt-4-turbo` - Faster processing with good quality
- `gpt-35-turbo` - Cost-effective option
- `gpt-4o` - Latest model with enhanced capabilities

## 📁 Project Structure

```
client-interaction-summary-generator/
├── app.py                 # Main application file
├── requirements.txt       # Python dependencies
├── README.md             # Project documentation
├── .env.example          # Environment variables template
├── .streamlit/
│   └── secrets.toml.example  # Streamlit secrets template
└── assets/               # Static assets (if any)
```

## 🔐 Security Features

- **Session Management**: Secure login with session persistence
- **Data Privacy**: Documents processed in memory, not stored permanently
- **API Security**: Secure Azure OpenAI integration
- **Authentication**: Hash-based credential verification

## 🚨 Troubleshooting

### **Common Issues**

1. **Azure OpenAI Configuration Error**
   - Verify API key and endpoint in configuration
   - Check Azure OpenAI service status
   - Ensure proper model deployment

2. **Document Processing Fails**
   - Check file format (PDF, DOCX, TXT supported)
   - Verify file is not corrupted
   - Ensure sufficient text content

3. **Login Issues**
   - Use correct demo credentials: `admin` / `password123`
   - Clear browser cache if session issues persist

4. **Agent Processing Errors**
   - Check Azure OpenAI quota and limits
   - Verify network connectivity
   - Review error messages in application

### **Error Messages**

- `Azure OpenAI configuration missing`: Set up environment variables or secrets
- `Failed to extract text`: Check document format and content
- `Error generating response`: Azure OpenAI API issue, check credentials

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit changes (`git commit -am 'Add new feature'`)
4. Push to branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Check the troubleshooting section above
- Review Azure OpenAI documentation

## 🚀 Future Enhancements

- [ ] Advanced authentication systems
- [ ] Custom summary templates
- [ ] Bulk document processing
- [ ] Analytics dashboard
- [ ] API endpoints for integration
- [ ] Multi-language support
- [ ] Email integration
- [ ] Calendar integration

---

**Built for Relationship Managers to streamline client interaction documentation and enhance professional communication.**
