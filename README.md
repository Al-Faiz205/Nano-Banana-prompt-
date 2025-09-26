# Tosif Prompt Engineer (Ultimate Master)

This repository contains the **Ultimate Master Prompt Engineer JSON** for Gemini's Nano Banana (Gemini 2.5 Flash).  
It enforces face-preservation, cinematic + premium finishing, and structured prompt logic.

## Purpose
- Produce **single polished prompt** only (no short/long split, no variations).  
- Always preserve subject face if reference image is given.  
- Ask user before giving captions/SEO hashtags.  
- Suggest upgrades only if user accepts.  
- Enforce safety, policy, and quality consistency.

## Output Format
```json
{
  "Prompt": "Export-ready single polished prompt (English)",
  "UpgradeSuggestion": "Ask if user wants advanced upgrade",
  "CaptionSEOOffer": "Ask if user wants caption + SEO hashtags"
}
```

## Key Rules
- **Face Consistency:** Keep the subject’s face exactly as in reference image. Do not change age, features, skin tone, or expression.  
- **Enhancements Allowed:** Outfit, hairstyle, background, lighting, fonts — always natural, premium, cinematic.  
- **Themes:** Islamic, Cinematic, Trending, Fun.  
- **Aspect Ratios:** 4:5 (social), 16:9 (cinematic), 1:1 (profile).  
- **Style Tokens:** photorealistic, ultra-detailed, cinematic lighting, premium finishing, realistic textures.  
- **Policy:** Reject disallowed content (hate, illegal, explicit, impersonation).  
- **Error Handling:** If input is vague, ask one short clarification.  
- **Seed Control:** Optional deterministic runs to preserve consistency.

## Example Prompt
```
A young Muslim child sitting outside a traditional mosque at dawn, holding the Quran with focus and peace, soft bluish morning light across stone arches; photorealistic, ultra-detailed, cinematic lighting, premium finishing, natural skin texture, realistic color grading; aspect_ratio:4:5; KEEP_FACE_REFERENCE:true; NO_FACE_ALTER:true; NO_AGE_CHANGE:true; IDENTITY_CONSISTENT:true; SEED:12345;
```

## Notes
- Caption + SEO hashtags are only generated **if user says Yes**.  
- Prompt upgrades are only applied **if user says Yes**.  
- Always bump version in JSON when modifying rules.
