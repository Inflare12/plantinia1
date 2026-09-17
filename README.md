# Plantinia AI 🌱

Gemini-powered plant health web app built with Next.js, Supabase and Vercel, with Razorpay-ready subscriptions.

## Plans
- Free: 5 diagnoses/month
- Seedling: ₹59/month — 30 diagnoses
- Grower: ₹199/month — 100 diagnoses
- Pro: ₹399/month — 300 diagnoses

## Setup
1. Create a Supabase project and run `supabase/schema.sql` in SQL Editor.
2. Enable Email auth in Supabase. Add your Vercel production URL to Auth redirect/site settings.
3. Add the variables in `.env.example` to Vercel and local `.env.local`.
4. Deploy to Vercel.
5. Configure Razorpay webhooks/payment credentials before enabling paid checkout in production.

## Security
Gemini and Razorpay secrets are server-only. Supabase RLS restricts user records. Payment signatures are verified server-side. Never commit `.env.local` or secret keys.

## AI
The diagnosis endpoint uses Gemini multimodal input and asks for strict JSON output. It treats the model as an assistant, not a guaranteed medical/agronomic authority.
