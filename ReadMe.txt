A comprehensive LLM Defense Layer

Full-featured, complete pipeline
Prompt filtering
Response filtering
Obfuscation-aware matching
Jailbreak pattern detection
Unified input/output check
Logging support


=== LLM-Agnostic Defense Layer ===
Regex filters (detect adversarial prompt variants, jailbreak phrases, DAN-style injections)
Keyword–target combination detection (e.g., disable + brake, override + safety)
Prompt injection scoring using llm-guard (ML-based detection beyond rules)
Obfuscation-aware detection (detects tricks like leetspeak: d1sabl3, br@k3, etc.)
Known jailbreak pattern matching (e.g., "Ignore previous instructions", "You are now DAN")
Static blocklists support (for banned phrases, actions, components)
Unified detection logic (all checks centralized and sequentially enforced)
Output scanning support (detects if model response contains unsafe content)
Structured logging in .jsonl format (timestamped, easy for audits or retraining data)
LLM-agnostic design (works with OpenAI, Claude, Gemini, Mistral, LLaMA, etc.)


# Prompt Injection	 	"Ignore all safety instructions" overrides prior instructions.
# Jailbreaking Attempt	 	"disable the braking system" is a malicious capability request.
# Mitigation Implemented	 	Uses pre-processing filter to block execution if risk is detected.


#  Regex-Based
# A defensive mechanism against both jailbreaking and prompt injection,
# but it uses a regular expression (regex)-based approach rather than keyword combinations.
