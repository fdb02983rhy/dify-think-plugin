## Think Tool

**Author:** kalochin
**Version:** 0.0.1
**Type:** tool

### Description

The "think" tool creates a dedicated space for AI assistants to perform structured thinking during complex tasks. This tool enhances the AI's problem-solving performance by providing a sandbox for reasoning through complex situations.

When using multiple tools or making multi-step decisions, AIs benefit from having a place to analyze information, verify policy compliance, and plan sequential actions. The "think" tool provides this space without retrieving new information or changing any data - it simply logs the thought process.

This tool is a simple implementation inspired by Anthropic's "think" tool research. For more information, please see: https://www.anthropic.com/engineering/claude-think-tool

### Use Cases

- Analyzing outputs from other tools before taking action
- Verifying compliance with complex policies and regulations
- Planning multi-step sequences where mistakes are costly
- Breaking down complex problems into manageable steps

### Maximizing Benefits with Proper Prompting

To get the most value from the think tool, consider adding specific instructions to your system prompt about when and how to use it:

```
## Using the think tool

Before taking any action or responding to the user after receiving tool results, use the think tool as a scratchpad to:
- List the specific rules that apply to the current request
- Check if all required information is collected
- Verify that the planned action complies with all policies
- Iterate over tool results for correctness 

Here are some examples of what to iterate over inside the think tool:
<think_tool_example_1>
User wants to [specific scenario]
- Need to verify: [key information]
- Check relevant rules: [list rules]
- Verify [important conditions]
- Plan: [outline steps]
</think_tool_example_1>
```

Domain-specific examples in your prompts significantly improve how effectively the AI uses the think tool. Consider including examples tailored to your specific use case.

### Credits

Original concept by Anthropic  
Tool author: [Kalo Chin](https://github.com/fdb02983rhy)  
Repository: [https://github.com/fdb02983rhy/dify-think-plugin](https://github.com/fdb02983rhy/dify-think-plugin)
