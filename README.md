Auto Pentest Workflow — here's how it works:

Manual Trigger
    → Nmap Scan (runs nmap on target IP)
    → XML to JSON (converts nmap output)
    → Edit Fields (extracts nmaprun data)
    → Google Gemini AI (analyzes results)
    → Build HTML Report (converts to HTML)
    → HTML to PDF (generates PDF file)
    → Read PDF file
    → Send to Discord (with PDF attached)


Important — Install wkhtmltopdf in n8n
# In docker-compose.yml, add to n8n service:
entrypoint: >
  /bin/sh -c "apt-get update && 
  apt-get install -y wkhtmltopdf && 
  n8n start"
    
