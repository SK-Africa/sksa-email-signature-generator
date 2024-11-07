# SearchKings Africa Email Signature Generator
## Standard Operating Procedure (SOP)

### 1. Overview
This document outlines the procedures for managing and maintaining the SearchKings Africa Email Signature Generator, a Jekyll-based web application that generates standardized email signatures for team members.

### 2. System Requirements
- Ruby
- Bundler
- Jekyll

### 3. Installation
1. Install required dependencies:
   ```bash
   gem install bundler jekyll
   ```
2. Clone the repository to your local environment
3. Run the application locally:
   ```bash
   bundle exec jekyll serve
   ```
4. Access the application at `localhost:4000`

### 4. File Structure
```
├── _config.yml           # Global configuration
├── _data/
│   └── team-members.yml  # Team member information
├── img/
│   └── sk-logo-large.png # Company logo
├── 404.html             # Error page
├── README.md            # Project documentation
├── email-generator.html # Signature template
└── index.html          # Main page
```

### 5. Configuration Management

#### 5.1 Company Information (_config.yml)
Update the following parameters as needed:
- `title`: Application title
- `description`: Application description
- `phone`: Company phone number
- `logo`: Path to company logo
- `website_url`: Company website URL

#### 5.2 Team Member Management (team-members.yml)
##### Data Structure
```yaml
firstName: [Required]
lastName: [Required]
title: [Required]
image_directory: [Required] Format: YYYY/MM
avatar: [Optional] Default: firstName-lastName.png
email: [Optional] Default: firstName@searchkingsafrica.com
```

##### Adding New Team Members
1. Open `_data/team-members.yml`
2. Add new entry under `teamMembers:`
3. Provide required fields
4. Add optional fields if needed
5. Upload profile photo to specified image directory

##### Removing Team Members
1. Comment out or remove the team member's entry from `team-members.yml`
2. Format for commenting out:
   ```yaml
   # - firstName: Name
   #   lastName: Surname
   #   title: Title
   ```

### 6. Image Management
#### 6.1 Profile Photos
- Location: WordPress media library
- Path format: `/wp-content/uploads/YYYY/MM/firstname-lastname.png`
- Directory structure defined in `image_directory` field
- Custom image names can be specified using `avatar` field

#### 6.2 Logo
- Stored in `/img/sk-logo-large.png`
- Used consistently across all signatures

### 7. Email Signature Format
The generated signature includes:
- Profile photo (100px width)
- Full name (bold)
- Job title (italic)
- Phone number
- Company logo with website link

### 8. Maintenance Procedures

#### 8.1 Regular Updates
1. Review team member list monthly
2. Update contact information as needed
3. Verify all profile photos are current
4. Test signature generation for new additions

#### 8.2 Troubleshooting
Common issues and solutions:
- Missing profile photo: Verify image path and upload status
- Incorrect email format: Check email field in team-members.yml
- Layout issues: Verify HTML/CSS in email-generator.html

### 9. Best Practices
1. Keep team-members.yml organized and properly formatted
2. Maintain consistent image naming conventions
3. Test signature generation after any configuration changes
4. Document all system modifications
5. Regularly backup configuration files

### 10. Security Considerations
1. Restrict access to configuration files
2. Use placeholder.png for temporary profiles
3. Verify email addresses before publication
4. Monitor system access logs

### 11. Support
For technical support or questions:
- Refer to internal IT team
- Check Jekyll documentation
- Review project README.md

### 12. Version Control
Document all changes to:
- Configuration files
- Template modifications
- Team member updates
- System upgrades

This SOP should be reviewed and updated quarterly or as needed to maintain accuracy and relevance.

## SK SA Email Signature Generator
For local, internal use to generate all available email signatures.

