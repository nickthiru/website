<script>
  import WaitlistModal from '$lib/components/WaitlistModal.svelte';
  import SEO from '$lib/components/SEO.svelte';
  
  let isWaitlistOpen = false;
  
  function openWaitlist() {
    isWaitlistOpen = true;
  }
</script>

<SEO
  title="CipherScan - Prove Your Cryptography Is Sound in 48 Hours, Not 2 Weeks"
  description="Connect your GitHub org. CipherScan finds weak, deprecated, misused, and quantum-vulnerable cryptography plus hardcoded secrets across every repo, then gives you a plain-English remediation plan and an auditor-ready cryptographic inventory report. No $5k–$15k consultant assessment. No cryptographer required."
/>

<WaitlistModal bind:isOpen={isWaitlistOpen} productName="CipherScan" productId="cipherscan" />

<div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16">

  <!-- ============================================
       HERO SECTION
       ============================================ -->
  <section class="mb-16">
    <div class="flex items-center gap-3 mb-4">
      <span class="px-3 py-1 bg-[#fedf19] text-[#202020] text-xs font-semibold rounded-full">
        Building Now
      </span>
    </div>

    <h1 class="text-2xl md:text-3xl font-bold text-neutral-900 dark:text-[#fedf19] mb-6">
      CipherScan
    </h1>

    <p class="text-lg text-neutral-600 dark:text-neutral-400 leading-relaxed mb-8">
      Answer the cryptography section of any security questionnaire or audit with verifiable evidence. 
      Connect your GitHub organization. CipherScan inventories every piece of cryptography in your code, 
      flags what's weak, deprecated, misused, or quantum-vulnerable, and hands you a prioritized fix plan 
      plus an auditor-ready report in 48 hours instead of 1–2 weeks. 
      No $5k–$15k consultant assessment. No cryptographer on staff required.
    </p>
  </section>

  <!-- ============================================
       PROBLEM SECTION
       ============================================ -->
  <section class="mb-16">
    <h2 class="text-2xl font-bold text-neutral-900 dark:text-[#fedf19] mb-6">
      The Problem
    </h2>

    <div class="bg-neutral-50 dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-8 space-y-4">
      <p class="text-neutral-700 dark:text-neutral-400 leading-relaxed">
        You're the CTO or Head of Engineering at a 10–100 person B2B SaaS company—fintech, healthtech, legaltech, or anything else 
        that sells into enterprise or regulated customers. An enterprise security questionnaire just landed and it's blocking a deal. 
        Or your SOC 2 / DORA / NIS2 auditor wants evidence for the cryptography control. Or your cyber insurance renewal is asking 
        about cryptographic controls and your post-quantum plan.
      </p>

      <p class="text-neutral-700 dark:text-neutral-400 leading-relaxed">
        <strong>You need to prove what cryptography you run and that none of it is broken.</strong> Not a paragraph of reassurance. 
        A real inventory: <em>which algorithms</em>, <em>where in the code</em>, <em>on which production paths</em>, 
        and <em>what you're doing about the weak spots</em>.
      </p>

      <p class="text-neutral-700 dark:text-neutral-400 leading-relaxed">
        Your options today:
      </p>

      <ul class="text-neutral-700 dark:text-neutral-400 space-y-2 ml-4">
        <li>
          <strong>Hire a consultant:</strong> $5k–$15k. 2–6 weeks. You get a static PDF that's stale the moment your team ships the next commit. 
          Next audit cycle, you pay again.
        </li>
        <li>
          <strong>Grep the codebase and run SSL Labs:</strong> Free. You find some MD5 calls, get an "A" on your marketing domain, 
          and write a paragraph nobody can verify. The reviewer asks for supporting evidence. The deal stalls.
        </li>
        <li>
          <strong>Lean on your existing SAST tool:</strong> Semgrep, Snyk Code, or CodeQL surface weak-crypto hits as a handful of rules among thousands, 
          dumped into a developer issue queue. There's no inventory view, nothing you can forward to a buyer or auditor, and no one on your team 
          who can say which findings actually matter.
        </li>
      </ul>

      <p class="text-neutral-700 dark:text-neutral-400 leading-relaxed mt-4">
        <strong>The root problem:</strong> Cryptography is scattered across every repo where keys, hashing, signing, and encryption happen. 
        Finding it, judging it, fixing it, and documenting it requires a cryptographer you don't have, can't afford to hire, 
        and can't wait 2–6 weeks for.
      </p>
    </div>
  </section>

  <!-- ============================================
       SOLUTION SECTION
       ============================================ -->
  <section class="mb-16">
    <h2 class="text-2xl font-bold text-neutral-900 dark:text-[#fedf19] mb-6">
      The Solution
    </h2>

    <p class="text-lg text-neutral-600 dark:text-neutral-400 mb-8">
      CipherScan turns your GitHub organization into a complete cryptographic inventory, a prioritized fix plan, and shareable evidence—in one sitting.
    </p>
    
    <div class="space-y-6">
      <!-- Step 1 -->
      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <div class="flex items-start gap-4">
          <div class="flex-shrink-0 w-10 h-10 bg-[#fedf19] rounded-lg flex items-center justify-center font-bold text-[#202020]">
            1
          </div>
          <div>
            <h3 class="text-xl font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
              Connect your GitHub organization
            </h3>
            <p class="text-neutral-600 dark:text-neutral-400">
              Sign in with GitHub OAuth and choose the repos to include. CipherScan statically analyzes JS/TS, Python, Go, Java, and C# 
              codebases—monorepos or dozens of small repos—looking for weak and deprecated algorithms (MD5, SHA-1, DES/3DES, RC4, RSA &lt;2048, ECB mode, 
              insecure random), quantum-vulnerable primitives (RSA, ECC/ECDH/ECDSA), hardcoded keys and secrets, and weak crypto libraries in your dependency manifests.
            </p>
            <p class="text-neutral-600 dark:text-neutral-400 mt-2 text-sm">
              Time investment: <strong>a few minutes</strong>. No agents to install, no sales call, no security expertise required.
            </p>
          </div>
        </div>
      </div>

      <!-- Step 2 -->
      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <div class="flex items-start gap-4">
          <div class="flex-shrink-0 w-10 h-10 bg-[#fedf19] rounded-lg flex items-center justify-center font-bold text-[#202020]">
            2
          </div>
          <div>
            <h3 class="text-xl font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
              CipherScan scores every finding by real exposure
            </h3>
            <p class="text-neutral-600 dark:text-neutral-400">
              A risk-scoring agent classifies each finding by severity and exposure: production path vs. test code, 
              secret vs. algorithm, data-in-transit vs. at-rest. You get a cryptographic posture score per repo and for the whole org, 
              so you know which 5 findings matter and which 50 are noise.
            </p>
            <p class="text-neutral-600 dark:text-neutral-400 mt-2 text-sm">
              Time investment: <strong>automated</strong>. Post-quantum findings are flagged as advisory in v1—they inform your PQC plan without inflating severity.
            </p>
          </div>
        </div>
      </div>

      <!-- Step 3 -->
      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <div class="flex items-start gap-4">
          <div class="flex-shrink-0 w-10 h-10 bg-[#fedf19] rounded-lg flex items-center justify-center font-bold text-[#202020]">
            3
          </div>
          <div>
            <h3 class="text-xl font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
              Fix it with a sprint-sized remediation plan
            </h3>
            <p class="text-neutral-600 dark:text-neutral-400">
              For every finding, CipherScan explains what it is, why it matters, and how to fix it in plain English—with a 
              language-specific code snippet that replaces the weak primitive with a modern equivalent. PQC-ready alternatives are flagged 
              where applicable. Everything is ordered into a plan your team can clear in a 1–2 week sprint.
            </p>
            <p class="text-neutral-600 dark:text-neutral-400 mt-2 text-sm">
              Time investment: <strong>one sprint</strong> (your team, fixing). Written for engineers, not cryptographers.
            </p>
          </div>
        </div>
      </div>

      <!-- Step 4 -->
      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <div class="flex items-start gap-4">
          <div class="flex-shrink-0 w-10 h-10 bg-[#fedf19] rounded-lg flex items-center justify-center font-bold text-[#202020]">
            4
          </div>
          <div>
            <h3 class="text-xl font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
              Share the evidence report and stay covered
            </h3>
            <p class="text-neutral-600 dark:text-neutral-400">
              Export a branded PDF or shareable link structured as Cryptographic Inventory + Findings + Remediation Status, 
              with references to the controls it satisfies (SOC 2 CC6, DORA, NIS2, NIST PQC / CNSA 2.0 timelines). 
              Forward it to the buyer's security team, your auditor, or your board the same day. Then let scheduled and on-push re-scans 
              catch regressions so the report is never stale again.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ============================================
       COMPARISON TABLE
       ============================================ -->
  <section class="mb-16">
    <h2 class="text-2xl font-bold text-neutral-900 dark:text-[#fedf19] mb-6">
      CipherScan vs. Your Alternatives
    </h2>

    <div class="overflow-x-auto">
      <table class="w-full text-sm">
        <thead>
          <tr class="border-b border-neutral-300 dark:border-neutral-600">
            <th class="text-left py-3 px-4 font-semibold text-neutral-900 dark:text-neutral-100">
              Factor
            </th>
            <th class="text-left py-3 px-4 font-semibold text-neutral-900 dark:text-neutral-100">
              CipherScan
            </th>
            <th class="text-left py-3 px-4 font-semibold text-neutral-900 dark:text-neutral-100">
              Consultant Assessment
            </th>
            <th class="text-left py-3 px-4 font-semibold text-neutral-900 dark:text-neutral-100">
              General SAST / SSL Labs
            </th>
          </tr>
        </thead>
        <tbody class="divide-y divide-neutral-200 dark:divide-neutral-700">
          <tr>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              <strong>Cost</strong>
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400 bg-green-50 dark:bg-green-900/20">
              Free scan, $49 one-time report, &lt;$300/yr continuous
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              $5k–$15k per assessment
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              Free–$$ (not crypto-focused)
            </td>
          </tr>
          <tr>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              <strong>Time to Evidence</strong>
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400 bg-green-50 dark:bg-green-900/20">
              48 hours
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              2–6 weeks
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              Minutes (but no evidence report)
            </td>
          </tr>
          <tr>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              <strong>Coverage</strong>
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400 bg-green-50 dark:bg-green-900/20">
              Source code across every repo, plus TLS endpoints
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              Scoped sample of code at a point in time
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              A few crypto rules among thousands, or one public endpoint
            </td>
          </tr>
          <tr>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              <strong>Full Cryptographic Inventory</strong>
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400 bg-green-50 dark:bg-green-900/20">
              Yes (inventory + findings + remediation status)
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              Yes (static PDF)
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              No (issue queue or letter grade)
            </td>
          </tr>
          <tr>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              <strong>Fix Guidance</strong>
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400 bg-green-50 dark:bg-green-900/20">
              Plain-English what/why/how + code snippets, sprint-ordered
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              Recommendations (you implement)
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              Rule description only
            </td>
          </tr>
          <tr>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              <strong>Stays Current</strong>
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400 bg-green-50 dark:bg-green-900/20">
              Scheduled + on-push re-scans, regression alerts
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              Stale on delivery; pay again next cycle
            </td>
            <td class="py-3 px-4 text-neutral-700 dark:text-neutral-400">
              Continuous, but no posture trend or report
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>

  <!-- ============================================
       KEY FEATURES
       ============================================ -->
  <section class="mb-16">
    <h2 class="text-2xl font-bold text-neutral-900 dark:text-[#fedf19] mb-6">
      Key Features
    </h2>

    <div class="grid md:grid-cols-2 gap-6">
      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
          Repository Crypto Scanner
        </h3>
        <p class="text-neutral-600 dark:text-neutral-400">
          Static analysis across every connected repo. Detects weak and deprecated algorithms, insecure modes and randomness, 
          quantum-vulnerable primitives, hardcoded keys and secrets, and weak crypto libraries in dependency manifests.
        </p>
      </div>

      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
          Exposure-Based Risk Scoring
        </h3>
        <p class="text-neutral-600 dark:text-neutral-400">
          Each finding is classified by severity and real exposure—production path vs. test code, secret vs. algorithm, 
          in-transit vs. at-rest. Posture scores per repo and per org tell you where to start.
        </p>
      </div>

      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
          Plain-English Remediation Plan
        </h3>
        <p class="text-neutral-600 dark:text-neutral-400">
          What/why/how for every finding, with a language-specific replacement snippet and PQC-ready alternatives flagged. 
          Ordered into a plan sized for a 1–2 week sprint.
        </p>
      </div>

      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
          Auditor-Ready Evidence Report
        </h3>
        <p class="text-neutral-600 dark:text-neutral-400">
          Branded PDF and shareable link: Cryptographic Inventory + Findings + Remediation Status, mapped to SOC 2 CC6, DORA, NIS2, 
          and NIST PQC / CNSA 2.0 timelines. Written for a non-technical reader.
        </p>
      </div>

      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
          Continuous Monitoring
        </h3>
        <p class="text-neutral-600 dark:text-neutral-400">
          Scheduled and on-push re-scans with regression alerts and a historical posture trend. 
          Your evidence stays current instead of going stale after one assessment.
        </p>
      </div>

      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
          TLS Cipher & Certificate Inventory
        </h3>
        <p class="text-neutral-600 dark:text-neutral-400">
          Verify ownership of your domains and CipherScan adds endpoint TLS ciphers and certificates to the inventory—
          so the report covers code and the edge, not just one or the other.
        </p>
      </div>
    </div>
  </section>

  <!-- ============================================
       WHO IT'S FOR
       ============================================ -->
  <section class="mb-16">
    <h2 class="text-2xl font-bold text-neutral-900 dark:text-[#fedf19] mb-6">
      Who It's For
    </h2>

    <div class="space-y-4">
      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
          CTOs Facing an Enterprise Security Questionnaire
        </h3>
        <p class="text-neutral-600 dark:text-neutral-400">
          A deal is stalled on the security review and the cryptography section wants more than a paragraph. 
          CipherScan gives you a verifiable inventory report within 48 hours so the deal keeps moving.
        </p>
      </div>

      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
          Teams Preparing for SOC 2, DORA, or NIS2 Audits
        </h3>
        <p class="text-neutral-600 dark:text-neutral-400">
          Cryptography has been a liability in audits—unverifiable prose or a stale consultant PDF. 
          CipherScan's report becomes your primary evidence for the cryptography control, with remediation status included.
        </p>
      </div>

      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
          Fintech, Healthtech & Legaltech SaaS
        </h3>
        <p class="text-neutral-600 dark:text-neutral-400">
          You handle sensitive data and sell into regulated customers who ask hard questions about encryption, hashing, and key handling. 
          CipherScan answers them with evidence from your actual code.
        </p>
      </div>

      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
          Companies Asked About Their Post-Quantum Plan
        </h3>
        <p class="text-neutral-600 dark:text-neutral-400">
          Insurers and buyers are starting to ask where you use RSA and ECC and what your migration timeline is. 
          CipherScan inventories quantum-vulnerable primitives and flags PQC-ready alternatives so you have a real answer.
        </p>
      </div>

      <div class="bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6">
        <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100 mb-2">
          Dev Agencies & Fractional CTOs
        </h3>
        <p class="text-neutral-600 dark:text-neutral-400">
          Every client needs its own crypto evidence, and consultant assessments don't scale across a portfolio. 
          Run CipherScan across client codebases and deliver evidence for each one without brokering a consultant per client.
        </p>
      </div>
    </div>
  </section>

  <!-- ============================================
       TIMELINE
       ============================================ -->
  <section class="mb-16">
    <h2 class="text-2xl font-bold text-neutral-900 dark:text-[#fedf19] mb-6">
      Timeline to Verifiable Evidence
    </h2>

    <div class="space-y-4">
      <!-- Timeline Item 1 -->
      <div class="flex gap-6">
        <div class="flex flex-col items-center">
          <div class="w-12 h-12 rounded-full bg-[#fedf19] text-[#202020] font-bold flex items-center justify-center text-lg">
            1
          </div>
          <div class="w-1 h-20 bg-gradient-to-b from-[#fedf19] to-neutral-300 dark:to-neutral-600 mt-2"></div>
        </div>
        <div class="pb-8">
          <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100">
            Hour 1: Connect & Scan
          </h3>
          <p class="text-neutral-600 dark:text-neutral-400 mt-2">
            Sign in with GitHub, pick your repos, and start the scan. CipherScan builds your cryptographic inventory and scores every finding.
          </p>
        </div>
      </div>

      <!-- Timeline Item 2 -->
      <div class="flex gap-6">
        <div class="flex flex-col items-center">
          <div class="w-12 h-12 rounded-full bg-[#fedf19] text-[#202020] font-bold flex items-center justify-center text-lg">
            2
          </div>
          <div class="w-1 h-20 bg-gradient-to-b from-[#fedf19] to-neutral-300 dark:to-neutral-600 mt-2"></div>
        </div>
        <div class="pb-8">
          <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100">
            Day 1–2: Review & Share the Report
          </h3>
          <p class="text-neutral-600 dark:text-neutral-400 mt-2">
            Review the prioritized findings, export the branded PDF or share link, and send it to the buyer's security team or your auditor. 
            Questionnaire answered within 48 hours.
          </p>
        </div>
      </div>

      <!-- Timeline Item 3 -->
      <div class="flex gap-6">
        <div class="flex flex-col items-center">
          <div class="w-12 h-12 rounded-full bg-[#fedf19] text-[#202020] font-bold flex items-center justify-center text-lg">
            3
          </div>
        </div>
        <div class="">
          <h3 class="text-lg font-semibold text-neutral-900 dark:text-neutral-100">
            Sprint 1: Clear Critical Findings
          </h3>
          <p class="text-neutral-600 dark:text-neutral-400 mt-2">
            Work through the sprint-sized remediation plan. Zero critical findings on production paths within two weeks, 
            with continuous re-scans keeping the remediation status in your report current.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- Follow the Build -->
	<section class="mb-16 mx-4 sm:mx-6 lg:mx-10">
		<div class="bg-neutral-50 dark:bg-[#202020] border-4 border-neutral-200 dark:border-neutral-700 rounded-lg p-12 text-center">
			<h2 class="text-2xl font-bold text-neutral-900 dark:text-white mb-4">Want to see how CipherScan gets built?</h2>
			<p class="text-lg text-neutral-600 dark:text-neutral-300 mb-8 max-w-2xl mx-auto">
				CipherScan is being built in public. Every architectural decision, engineering challenge, 
				and product direction gets documented and shared — so you can follow the journey from 
				idea to production.
			</p>
			<a
				href="https://nickthiru.dev/writing?series=cipher-scan"
				target="_blank"
				rel="noopener noreferrer"
				class="inline-flex items-center gap-2 px-6 py-3 bg-[#fedf19] text-[#202020] font-semibold rounded-md hover:bg-[#fe1817] hover:text-white transition-colors"
			>
				Read the CipherScan blog series
				<svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
				</svg>
			</a>
		</div>
	</section>

  <!-- ============================================
       PRICING
       ============================================ -->
  <!-- <section class="mb-16">
    <h2 class="text-2xl font-bold text-neutral-900 dark:text-[#fedf19] mb-6">
      Pricing
    </h2>

    <div class="bg-white dark:bg-neutral-800 border-2 border-[#fedf19] rounded-lg p-8 max-w-md">
      <div class="mb-6">
        <div class="text-3xl font-bold text-neutral-900 dark:text-neutral-100 mb-2">
          $49
          <span class="text-lg font-normal text-neutral-600 dark:text-neutral-400">/one-time report</span>
        </div>
        <p class="text-neutral-600 dark:text-neutral-400">
          Free scan to see your posture. $49 for the full evidence report. Continuous monitoring for under $300/year. Compare to $5k–$15k consulting.
        </p>
      </div>

      <ul class="space-y-3 mb-8">
        <li class="flex items-start gap-2">
          <svg class="w-5 h-5 text-[#fe1817] flex-shrink-0 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
          </svg>
          <span class="text-neutral-700 dark:text-neutral-400">GitHub org scan across all connected repos</span>
        </li>
        <li class="flex items-start gap-2">
          <svg class="w-5 h-5 text-[#fe1817] flex-shrink-0 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
          </svg>
          <span class="text-neutral-700 dark:text-neutral-400">Exposure-based risk scoring and posture score</span>
        </li>
        <li class="flex items-start gap-2">
          <svg class="w-5 h-5 text-[#fe1817] flex-shrink-0 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
          </svg>
          <span class="text-neutral-700 dark:text-neutral-400">Plain-English remediation plan with code snippets</span>
        </li>
        <li class="flex items-start gap-2">
          <svg class="w-5 h-5 text-[#fe1817] flex-shrink-0 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
          </svg>
          <span class="text-neutral-700 dark:text-neutral-400">Branded PDF + shareable evidence report (SOC 2 CC6, DORA, NIS2, NIST PQC)</span>
        </li>
        <li class="flex items-start gap-2">
          <svg class="w-5 h-5 text-[#fe1817] flex-shrink-0 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
          </svg>
          <span class="text-neutral-700 dark:text-neutral-400">Continuous monitoring: scheduled + on-push re-scans, regression alerts</span>
        </li>
        <li class="flex items-start gap-2">
          <svg class="w-5 h-5 text-[#fe1817] flex-shrink-0 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
          </svg>
          <span class="text-neutral-700 dark:text-neutral-400">TLS cipher & certificate inventory for verified domains</span>
        </li>
      </ul>

      <div class="flex justify-center mt-8">
        <button 
          on:click={openWaitlist}
          class="inline-flex items-center justify-center gap-2 w-full sm:w-auto px-6 py-3 bg-[#fe1817] text-white font-semibold rounded-md hover:bg-[#fedf19] hover:text-[#202020] transition-colors"
        >
          Join the waitlist
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
          </svg>
        </button>
      </div>
    </div>

  </section> -->

  <!-- ============================================
       FAQ
       ============================================ -->
  <section class="mb-16">
    <h2 class="text-2xl font-bold text-neutral-900 dark:text-[#fedf19] mb-6">
      Frequently Asked Questions
    </h2>

    <div class="space-y-4">
      <!-- FAQ 1 -->
      <details class="group bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6 [&_summary::-webkit-details-marker]:hidden">
        <summary class="flex items-center justify-between font-semibold text-neutral-900 dark:text-neutral-100 cursor-pointer">
          <span>Do I really have to give you read access to my source code?</span>
          <span class="transition duration-300 group-open:-rotate-180">
            <svg fill="none" height="24" shape-rendering="geometricPrecision" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" viewBox="0 0 24 24" width="24">
              <path d="M6 9l6 6 6-6"></path>
            </svg>
          </span>
        </summary>
        <p class="mt-3 text-neutral-600 dark:text-neutral-400">
          Yes—that's what makes the inventory real. Cryptography lives in the code where keys, hashing, signing, and encryption actually happen, 
          and an endpoint grade can't see it. CipherScan uses GitHub OAuth with read-only scope, you choose exactly which repos to include, 
          and you can revoke access at any time from GitHub. We're building CipherScan to meet the same questionnaire standards our customers face, 
          and we'll publish our own security posture before launch.
        </p>
      </details>

      <!-- FAQ 2 -->
      <details class="group bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6 [&_summary::-webkit-details-marker]:hidden">
        <summary class="flex items-center justify-between font-semibold text-neutral-900 dark:text-neutral-100 cursor-pointer">
          <span>Will an auditor or enterprise buyer actually accept the report?</span>
          <span class="transition duration-300 group-open:-rotate-180">
            <svg fill="none" height="24" shape-rendering="geometricPrecision" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" viewBox="0 0 24 24" width="24">
              <path d="M6 9l6 6 6-6"></path>
            </svg>
          </span>
        </summary>
        <p class="mt-3 text-neutral-600 dark:text-neutral-400">
          The report is structured the way reviewers want it: a complete Cryptographic Inventory, Findings, and Remediation Status, 
          with references to the controls it satisfies (SOC 2 CC6, DORA, NIS2, NIST PQC / CNSA 2.0). We can't guarantee any individual 
          reviewer's decision, but before launch we're sharing sample reports with SOC 2 and DORA auditors and recording what they accept 
          and what they ask to change. One tip: submit with remediation status included and critical findings closed—that's what removes grounds for an exception.
        </p>
      </details>

      <!-- FAQ 3 -->
      <details class="group bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6 [&_summary::-webkit-details-marker]:hidden">
        <summary class="flex items-center justify-between font-semibold text-neutral-900 dark:text-neutral-100 cursor-pointer">
          <span>How accurate is the detection? I don't want a wall of false positives.</span>
          <span class="transition duration-300 group-open:-rotate-180">
            <svg fill="none" height="24" shape-rendering="geometricPrecision" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" viewBox="0 0 24 24" width="24">
              <path d="M6 9l6 6 6-6"></path>
            </svg>
          </span>
        </summary>
        <p class="mt-3 text-neutral-600 dark:text-neutral-400">
          Low false positives is the top engineering priority—one obviously wrong finding destroys trust with a technical reviewer. 
          CipherScan combines static analysis with agent-based classification, then scores by exposure so MD5 in a test fixture is not 
          ranked alongside MD5 hashing passwords on a production path. You can mark findings as false positives or accepted risk, 
          and those decisions carry into the report.
        </p>
      </details>

      <!-- FAQ 4 -->
      <details class="group bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6 [&_summary::-webkit-details-marker]:hidden">
        <summary class="flex items-center justify-between font-semibold text-neutral-900 dark:text-neutral-100 cursor-pointer">
          <span>Which languages and ecosystems does CipherScan support?</span>
          <span class="transition duration-300 group-open:-rotate-180">
            <svg fill="none" height="24" shape-rendering="geometricPrecision" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" viewBox="0 0 24 24" width="24">
              <path d="M6 9l6 6 6-6"></path>
            </svg>
          </span>
        </summary>
        <p class="mt-3 text-neutral-600 dark:text-neutral-400">
          At launch: JavaScript/TypeScript, Python, Go, Java, and C#, including dependency manifests for each. Monorepos and many-small-repo 
          setups are both supported. If your stack isn't listed, reach out—we'll consider it for the roadmap.
        </p>
      </details>

      <!-- FAQ 5 -->
      <details class="group bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6 [&_summary::-webkit-details-marker]:hidden">
        <summary class="flex items-center justify-between font-semibold text-neutral-900 dark:text-neutral-100 cursor-pointer">
          <span>Do I need to care about post-quantum cryptography right now?</span>
          <span class="transition duration-300 group-open:-rotate-180">
            <svg fill="none" height="24" shape-rendering="geometricPrecision" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" viewBox="0 0 24 24" width="24">
              <path d="M6 9l6 6 6-6"></path>
            </svg>
          </span>
        </summary>
        <p class="mt-3 text-neutral-600 dark:text-neutral-400">
          Not urgently—but buyers and insurers are starting to ask. CipherScan inventories your quantum-vulnerable primitives (RSA, ECC/ECDH/ECDSA) 
          and flags PQC-ready alternatives, with NIST PQC / CNSA 2.0 timelines referenced in the report. In v1 this is advisory: 
          it informs your migration plan but does not inflate the severity of your findings.
        </p>
      </details>

      <!-- FAQ 6 -->
      <details class="group bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6 [&_summary::-webkit-details-marker]:hidden">
        <summary class="flex items-center justify-between font-semibold text-neutral-900 dark:text-neutral-100 cursor-pointer">
          <span>How is this different from Semgrep, Snyk, CodeQL, or SSL Labs?</span>
          <span class="transition duration-300 group-open:-rotate-180">
            <svg fill="none" height="24" shape-rendering="geometricPrecision" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" viewBox="0 0 24 24" width="24">
              <path d="M6 9l6 6 6-6"></path>
            </svg>
          </span>
        </summary>
        <p class="mt-3 text-neutral-600 dark:text-neutral-400">
          General SAST tools treat weak crypto as a few rules among thousands and output a developer issue queue with no inventory view. 
          SSL Labs tests one public endpoint at a point in time and returns a letter grade with no code visibility. CipherScan treats 
          cryptography as the whole job: a complete inventory across your source, exposure-based prioritization, fix guidance for non-cryptographers, 
          and a report a CTO can forward to a buyer or auditor the same day. Keep your SAST tool—CipherScan answers a different question.
        </p>
      </details>

      <!-- FAQ 7 -->
      <details class="group bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6 [&_summary::-webkit-details-marker]:hidden">
        <summary class="flex items-center justify-between font-semibold text-neutral-900 dark:text-neutral-100 cursor-pointer">
          <span>What happens after I send the report?</span>
          <span class="transition duration-300 group-open:-rotate-180">
            <svg fill="none" height="24" shape-rendering="geometricPrecision" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" viewBox="0 0 24 24" width="24">
              <path d="M6 9l6 6 6-6"></path>
            </svg>
          </span>
        </summary>
        <p class="mt-3 text-neutral-600 dark:text-neutral-400">
          With continuous monitoring, CipherScan re-scans on a schedule and on every push, alerts you if a weak primitive or secret 
          creeps back in, and tracks your posture trend over time. When the next questionnaire, audit, or renewal arrives, 
          your report is already current—no re-engaging a consultant, no stale PDF.
        </p>
      </details>

      <!-- FAQ 8 -->
      <details class="group bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6 [&_summary::-webkit-details-marker]:hidden">
        <summary class="flex items-center justify-between font-semibold text-neutral-900 dark:text-neutral-100 cursor-pointer">
          <span>When will CipherScan launch?</span>
          <span class="transition duration-300 group-open:-rotate-180">
            <svg fill="none" height="24" shape-rendering="geometricPrecision" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" viewBox="0 0 24 24" width="24">
              <path d="M6 9l6 6 6-6"></path>
            </svg>
          </span>
        </summary>
        <p class="mt-3 text-neutral-600 dark:text-neutral-400">
          Currently in active development as part of the SecureStack suite alongside PolicyForge. Waitlist members get early access 
          and founding member pricing. Launch timing will be announced to the waitlist first.
        </p>
      </details>

      <!-- FAQ 9 -->
      <details class="group bg-white dark:bg-neutral-800 border border-neutral-200 dark:border-neutral-700 rounded-lg p-6 [&_summary::-webkit-details-marker]:hidden">
        <summary class="flex items-center justify-between font-semibold text-neutral-900 dark:text-neutral-100 cursor-pointer">
          <span>Is there a free tier?</span>
          <span class="transition duration-300 group-open:-rotate-180">
            <svg fill="none" height="24" shape-rendering="geometricPrecision" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" viewBox="0 0 24 24" width="24">
              <path d="M6 9l6 6 6-6"></path>
            </svg>
          </span>
        </summary>
        <p class="mt-3 text-neutral-600 dark:text-neutral-400">
          Yes. Connect your GitHub org and run a free scan to see your cryptographic posture before paying anything. 
          The full evidence report is a one-time $49, and continuous monitoring is priced under $300 per year—no sales call, 
          no procurement cycle. Waitlist members get priority beta access.
        </p>
      </details>
    </div>
  </section>

  <!-- ============================================
       FINAL CTA
       ============================================ -->
  <section class="bg-neutral-50 dark:bg-[#202020] border-4 border-neutral-200 dark:border-neutral-700 rounded-lg mx-4 sm:mx-6 lg:mx-10 p-12 text-center">
    <h2 class="text-2xl font-bold text-neutral-900 dark:text-white mb-4">
      The questionnaire is due in 2 weeks. CipherScan answers the cryptography section in 48 hours.
    </h2>
    <p class="text-lg text-neutral-600 dark:text-neutral-300 mb-8 max-w-2xl mx-auto">
      Join the waitlist for early access, beta access, and founding member pricing. 
      Pre-beta users help shape the scanner and validate the report with real auditors and enterprise security teams.
    </p>
    <button 
      on:click={openWaitlist}
      class="inline-flex items-center gap-2 px-6 py-3 bg-[#fe1817] text-white font-semibold rounded-md hover:bg-[#fedf19] hover:text-[#202020] transition-colors"
    >
      Join the waitlist
      <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
      </svg>
    </button>
    <p class="text-base text-neutral-600 dark:text-neutral-300 mt-4">
      No spam. Unsubscribe anytime.
    </p>
  </section>

</div>
s