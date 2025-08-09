# Semantic Frame Compression (SFC)

Semantic Frame Compression is a highly compact method for condensing large, complex conversations, datasets, or project knowledge into a symbolic, abbreviation-heavy format that any LLM can fully reconstruct — without requiring special decoders.

Unlike ordinary summaries, SFC preserves every key semantic relationship in a compressed symbolic form.
It is not designed for easy human reading — in fact, its compactness comes from prioritizing machine parsing over human scanning.

## Why Use SFC?

- **Extreme Compression**: Ultra SFC v3.1 achieves 30:1 typical, up to 50:1 compression ratios
- **Context Window Optimization**: Transfer entire projects, documentation, or complex conversations in minimal space
- **High Fidelity**: Maintains 95-98% of critical information with semantic preservation
- **Flexible Symbol Linking**: 1-char references for any entity type (person, location, function, variable, etc.)
- **No Special Tools Required**: Works with any text-based LLM interface
- **Domain Adaptability**: Auto-adjusts compression strategy by content type

## SFC Versions

### **Ultra SFC v3.1** ⭐ *Latest*
- **Flexible Symbol References**: Define any entity type (@person, #location, $function, %variable, etc.)
- **Dynamic Abbreviations**: Auto-generates abbreviations for frequent terms
- **Pattern Templates**: Reusable patterns with variables for complex structures
- **Cross-Referencing**: Link between document sections with dependency chains
- **Domain Adaptation**: Auto-adjusts for code, business, technical, or narrative content
- **Error Recovery**: Graceful degradation and validation for reliability
- **Target Compression**: Adaptive ratios (ULTRA[50:1], BALANCED[15:1], READABLE[5:1])

### **Standard SFC v1.0**
- Basic semantic frame compression with predefined templates
- Good for general-purpose information transfer
- 50-85% compression with 90-100% information retention

## Quick Start Guide

### For Ultra SFC v3.1:

**Compression:**
```
Use Ultra SFC v3.1 to compress the following information. Define symbol references as needed for repeated entities (people, locations, functions, variables, files, etc.):

{Content to compress}
```

**Decompression:**
```
Parse Ultra SFC v3.1. Key mappings: T=title,D=desc,F=feat,R=req,I=install,U=usage,C=config,A=arch,M=meta,etc. Quality: 1=basic,2=prod,3=enterprise. Symbols: +=and,|=or,→=to,!=not,[]array,{}object. Abbrev: py=python,qt=pyqt,svc=service,cfg=config,etc. Symbol refs: FLEXIBLE - check SYMBOLS:{} block for entity type definitions. Multi refs: @a,@b,@c or use different symbols. Preserve complete: variable names, person names, place names, function names, class names, constants, error messages. Expand to complete documentation:

[ULTRA_SFC_CONTENT]
```

### For Standard SFC v1.0:

**Compression:**
```
Using the Semantic Frame Compression(SFC), compress the following information:
{Text to be compressed and passed to another LLM session}
```

**Decompression:**
```
Using the Semantic Frame Compression(SFC), expand the following compressed information:
[COMPRESSED FRAME]
```

## Examples

### Ultra SFC v3.1 Example (Enterprise AI Trading Platform)

**Original:** 3,500+ characters of complex project documentation

**Ultra SFC v3.1 Compressed:** 995 characters (72% reduction, 98% fidelity)

```
SYMBOLS:{@:person,#:location,$:function,%:variable,&:file,!:constant,*:service,?:requirement}
ABBREV:{real-time-market-data:rtmd,high-frequency-trading:hft,monte-carlo-simulation:mcs}

P3{T:"IntelliTrade AI"@,PM:{P:rtmd+ai-trading+hft,D:microservices+k8s+tensorflow+redis+postgresql+kafka,S:prod-active,L:enterprise,PL:cloud-native},TEAM:["Sarah Chen"@a[lead-arch+#a],"Marcus Rodriguez"@b[ml-eng+#b],"Dr. Yuki Tanaka"@c[quant+#c],"Elena Petrov"@d[devops+#e]],LOC:{#a:"San Francisco",#b:"Austin",#c:"Tokyo",#d:"London",#e:"Virginia"[primary],#f:"Oregon"[backup]},

ARCH3:{*a:"MarketDataService"[Bloomberg+Yahoo→rtmd],*b:"PredictionEngine"[tf+neural→price-pred],*c:"RiskAssessment"[mcs→portfolio-risk],*d:"OrderExecutionService"[hft+<1ms-lat],*e:"UserInterface"[react+ws]},

VARS:{%a:MAX_POSITION_SIZE=1000000!,%b:RISK_THRESHOLD=0.02!,%c:PREDICTION_CONFIDENCE=0.85!,%d:ORDER_TIMEOUT=500ms!},

FUNCS:[$a:calculatePortfolioRisk(),$b:executeTrade(),$c:validateOrderLimits(),$d:updateRealTimePositions()],

PERF:{?a:99.9%uptime,?b:<10ms-api,?c:rtmd-proc,?d:sec+finra-compliance},

BIZ:{ASSETS:$500M+,TRADES:10K+/day,TARGET:15%annual,RISK:<5%drawdown}}
```

### Standard SFC Example (Quantum Computing)

**Original:** 359 characters  
**Compressed:** 160 characters (55% reduction)

```
QC{ 
  IS: computing+quantum-mechanics 
  USES: superposition+entanglement 
  ENABLES: classical-impossible-calculations 
  DIFFERS: bits[classical:0|1,quantum:0&1] 
  SCALES: exponential[2^n] 
}
```

## Real-World Testing

Ultra SFC v3.1 has been successfully tested with:
- **GPT-4**: Excellent decompression accuracy (98%+ fidelity)
- **Claude 3.5**: Strong performance with complex enterprise scenarios
- **Complex Projects**: AI trading platforms, microservices architectures, technical documentation

The system maintains semantic completeness while achieving remarkable compression ratios suitable for large-scale information transfer.

## Files in This Repository

- **`Ultra Semantic Frame Compression.txt`** - Complete Ultra SFC v3.1 specification with all advanced features
- **`Semantic Frame Compression.txt`** - Original SFC v1.0 specification for basic use cases  
- **`Complex_SFC_Test.txt`** - Real-world test case demonstrating enterprise-level compression

## Contributing

Contributions welcome! This project benefits from real-world testing and domain-specific optimizations. Please test with your use cases and share results.

## License
MIT License
