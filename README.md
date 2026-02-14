Website Audit Tool


Professional website analysis tool for UK Business Automations
Generate comprehensive, client-ready audit reports in seconds.
































🎯 Overview

A powerful lead generation tool designed for UK Business Automations to deliver professional website audit reports to potential clients. This application analyses websites across multiple dimensions and generates detailed, actionable reports with visual data representations.

Key Features

✅ Comprehensive Website Analysis

•
SEO performance and optimisation

•
Page speed and Core Web Vitals

•
Mobile responsiveness

•
Accessibility compliance (WCAG standards)

✅ Advanced Digital Presence Audit

•
GEO/AEO optimisation (AI search engine readiness)

•
Social media presence analysis (6 major platforms)

•
Google Business Profile optimisation

•
Voice agent implementation readiness

✅ Competitor Intelligence

•
Side-by-side comparison with up to 2 competitors

•
Traffic analysis and market positioning

•
Visual charts and data representations

✅ Social Media Deep Dive

•
Facebook, Instagram, LinkedIn, Twitter/X, TikTok, YouTube

•
Profile completeness scoring

•
Posting frequency analysis

•
Engagement metrics

•
Follower growth tracking

✅ Professional Reporting

•
Branded UK Business Automations design

•
Prioritised, actionable recommendations

•
Visual charts and graphs (Recharts)

•
High Level CRM integration ready

•
Export-ready format




🚀 Quick Start

Prerequisites

•
Node.js 22.x or higher

•
pnpm 10.x or higher (recommended) or npm

Installation

Bash


# Clone the repository
git clone https://github.com/millionaireKerry/website-scan.git
cd website-scan

# Install dependencies
pnpm install

# Start development server
pnpm dev



The application will be available at http://localhost:3000

Build for Production

Bash


# Create production build
pnpm build

# Preview production build
pnpm preview






📋 Usage

Generating an Audit Report

1.
Enter Website Details

•
Website URL (e.g., https://example.co.uk )

•
Business name

•
Industry sector



2.
Add Social Media Profiles (Optional)

Leave blank for platforms the business doesn't use - the tool will flag these as opportunities

•
Facebook URL

•
Instagram URL

•
LinkedIn URL

•
Twitter/X URL

•
TikTok URL

•
YouTube URL



3.
Add Competitor URLs (Optional but Recommended)

The tool will compare the client's website against competitors

•
Competitor 1 URL

•
Competitor 2 URL



4.
Generate Report

•
Click "Generate Free Audit Report"

•
Review comprehensive analysis

•
Use as lead magnet for client acquisition



Report Sections

The generated report includes:

1.
Executive Summary - Overall scores and key metrics

2.
SEO Analysis - Technical SEO, meta tags, schema markup

3.
Performance Metrics - Load times, Core Web Vitals, optimisation opportunities

4.
Accessibility Audit - WCAG compliance, contrast ratios, keyboard navigation

5.
GEO/AEO Readiness - AI search engine optimisation for ChatGPT, Perplexity, Google SGE

6.
Social Media Presence - Platform analysis, engagement metrics, growth opportunities

7.
Voice Agent Potential - Talking website implementation readiness

8.
Google Business Profile - Local SEO optimisation opportunities

9.
Competitor Analysis - Side-by-side comparison with market positioning

10.
Actionable Recommendations - Prioritised list of improvements with impact ratings




🎨 Branding

The tool uses UK Business Automations brand colours:

•
Background: #000000 (Black)

•
Primary Text: #FFFFFF (White)

•
Accent Gold: #FFD700 (Highlights and CTAs)

•
Accent Teal: #006D75 (Data visualisation and charts)

All content is written in UK English and tailored for a UK business audience.




🔧 Technology Stack

Frontend

•
React 19.2 - UI framework

•
TypeScript 5.6 - Type safety

•
Tailwind CSS 4 - Styling

•
Vite 7 - Build tool and dev server

•
Wouter - Client-side routing

UI Components

•
shadcn/ui - Component library

•
Radix UI - Accessible primitives

•
Recharts - Data visualisation

•
Lucide React - Icons

•
Framer Motion - Animations

Development

•
ESLint - Code linting

•
Prettier - Code formatting

•
pnpm - Package management




📁 Project Structure

Plain Text


website-scan/
├── client/                 # Frontend application
│   ├── public/            # Static assets
│   ├── src/
│   │   ├── components/    # React components
│   │   │   ├── ui/       # shadcn/ui components
│   │   │   ├── AuditForm.tsx
│   │   │   ├── AuditReport.tsx
│   │   │   └── SocialMediaSection.tsx
│   │   ├── contexts/      # React contexts
│   │   ├── hooks/         # Custom hooks
│   │   ├── lib/          # Utilities and helpers
│   │   │   ├── types.ts
│   │   │   ├── auditAnalysis.ts
│   │   │   └── utils.ts
│   │   ├── pages/        # Page components
│   │   ├── App.tsx       # Main app component
│   │   ├── main.tsx      # Entry point
│   │   └── index.css     # Global styles
│   └── index.html        # HTML template
├── server/               # Server configuration (static hosting)
├── shared/              # Shared types and constants
├── package.json
├── tsconfig.json
├── vite.config.ts
└── README.md






🔌 Integration with High Level CRM

The tool includes a placeholder for High Level form integration. To connect:

1.
Navigate to client/src/components/AuditReport.tsx

2.
Locate the High Level form section

3.
Replace the placeholder with your High Level form embed code or webhook URL

4.
Configure form fields to capture:

•
Name

•
Email

•
Phone

•
Company name

•
Website URL



Automated Lead Flow

Once integrated, the tool can:

1.
Capture lead information before showing the full report

2.
Automatically send audit PDF to High Level

3.
Trigger follow-up sequences

4.
Schedule consultation calls

5.
Track lead engagement




📊 Business Use Cases

Lead Generation

Use as a free lead magnet on social media, offering "Free £500 Website Audit" to attract UK small business owners.

Sales Conversations

Generate live audits during discovery calls to demonstrate expertise and identify pain points.

Proposal Creation

Export audit data to create professional service proposals with specific recommendations and pricing.

Client Onboarding

Baseline audit before starting work to measure improvement over time.




🛠️ Customisation

Updating Brand Colours

Edit client/src/index.css:

CSS


:root {
  --background: oklch(0.141 0.005 285.823); /* Black background */
  --foreground: oklch(0.85 0.005 65);       /* White text */
  --primary: oklch(0.85 0.15 85);           /* Gold #FFD700 */
  --accent: oklch(0.45 0.12 200);           /* Teal #006D75 */
}



Adding New Audit Metrics

1.
Update types in client/src/lib/types.ts

2.
Add analysis logic in client/src/lib/auditAnalysis.ts

3.
Create UI component in client/src/components/

4.
Import and render in AuditReport.tsx

Modifying Recommendations

Edit the recommendation generation logic in client/src/lib/auditAnalysis.ts:

TypeScript


function generateRecommendations(data: AuditData): Recommendation[] {
  // Add your custom recommendation logic
}






📝 Supporting Documents

This repository includes three essential business documents in the root directory:

1.
Technical_Cheat_Sheet_Website_Audit_Fixes.md
Internal guide explaining how to fix each issue identified in audits

2.
Client_Action_Blueprint.md
Actionable checklist for clients who want to implement fixes themselves

3.
Service_Proposal_Template.md
Professional proposal template with pricing structure and service packages




🚢 Deployment

Manus Hosting (Recommended)

The project is built with Manus webdev tools and can be deployed directly through the Manus platform with one-click publishing.

Vercel

Bash


# Install Vercel CLI
npm i -g vercel

# Deploy
vercel



Netlify

Bash


# Install Netlify CLI
npm i -g netlify-cli

# Deploy
netlify deploy --prod



Custom Server

Bash


# Build the project
pnpm build

# Serve the dist/public folder with any static hosting service






🤝 Contributing

This is a proprietary tool for UK Business Automations. For internal contributions:

1.
Create a feature branch

2.
Make your changes

3.
Test thoroughly

4.
Submit a pull request with detailed description




📄 License

Copyright © 2026 UK Business Automations. All rights reserved.

This software is proprietary and confidential. Unauthorised copying, distribution, or use is strictly prohibited.




📞 Support

For questions, issues, or feature requests:

•
Website: ukbusinessautomations.com

•
Email: [Your contact email]

•
GitHub Issues: Create an issue




🎯 Roadmap

Planned Features




PDF export functionality




Email delivery automation




Real-time API integrations (Google PageSpeed, SimilarWeb)




Historical audit tracking




Multi-language support




White-label customisation




Automated competitor discovery




AI-powered content suggestions




🙏 Acknowledgements

Built with:

•
React

•
Tailwind CSS

•
shadcn/ui

•
Recharts

•
Vite




Made with ❤️ by UK Business Automations
Helping UK small businesses implement AI-powered solutions

