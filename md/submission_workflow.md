
# Workflow diagrams

    flowchart TD
      A[Start: Complete assignment] --> B{Where is your work stored?}
    
      B -->|GitHub Repo| C[Commit & push changes]
      B -->|GitHub Gist| D[Create/Update gist]
      B -->|Colab| E[Share notebook link (viewable)]
      B -->|OneCompiler| F[Save as unlisted link]
    
      C --> G[Copy submission URL]
      D --> G
      E --> G
      F --> G
    
      G --> H[Open Google Form for Assignment X]
      H --> I[Fill: name, email, section (if any), URL]
      I --> J[Submit form]
      J --> K[Confirmation page/screenshot optional]
      K --> L[Done]

    flowchart TD
    %% Student lane
    subgraph S[Student]
      S1[Complete assignment] --> S2[Publish artifact<br/>Repo/Gist or Colab or OneCompiler]
      S2 --> S3[Ensure link works<br/>(incognito test)]
      S3 --> S4[Submit URL via Google Form]
    end
    
    %% Collection lane
    subgraph C[Collection]
      C1[Google Form] --> C2[Responses stored in Google Sheet<br/>(timestamped)]
    end
    
    %% Instructor lane
    subgraph I[Instructor]
      I1[Open response sheet] --> I2[Filter by Assignment X]
      I2 --> I3[Click URL to review/run]
      I3 --> I4[Record score + comments<br/>in grade sheet]
      I4 --> I5[Return feedback<br/>(email or published sheet)]
    end
    
    %% Connections
    S4 --> C1
    C2 --> I1

