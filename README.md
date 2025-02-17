# Ultimate Debugging Prompt for Claude

![DALL·E 2024-07-24 17 14 32 - A sleek, modern 16x9 image representing a debugging prompt for GitHub  The image features a dark theme with code snippets, a magnifying glass focusing](https://github.com/user-attachments/assets/bf48c21a-7200-441d-b18b-57bf81255627)

Welcome to the Ultimate Debugging Prompt for Claude! This sophisticated and carefully engineered prompt is designed to streamline and enhance your debugging process when working with Claude 3.5 Sonnet. 

## Prompt Structure

The Ultimate Debugging Prompt for Claude consists of the following main sections:

1. **Variables**: A set of predefined variables used to store specific information about the debugging scenario, such as the attached project code, error message, and user task.
2. **Placeholders**: Designated areas within the prompt where users input the necessary information for their specific debugging case.
3. **Code Blocks**: Sections of the prompt where users attach the relevant project files, including source code, logs, and configuration files.
4. **Reasoning and Analysis**: Structured sections that guide Claude's thought process, from generating predictions to narrowing down the root cause of the error.
5. **Explanations and Instructions**: Areas where Claude provides detailed explanations of the identified issue and step-by-step instructions for resolving it.

## Variable Explanations

The following table describes the user inputted variables used in the Ultimate Debugging Prompt for Claude:

| Variable | Description | Input Format |
|----------|-------------|--------------|
| `ATTACHED_PROJECT_CODE` | The code blocks represent your attached code files.  If files are small enough, you can copy and paste the code inside.  I recomend you export your entire code repository in one attached file using my [Code-Repository-to-Text-File tool](https://github.com/PixelPoser/Code-Repository-to-Text-File) to circumvent the 5 file upload restriction.  | `<YOUR_FILE_1.py>`, `<YOUR_FILE_2.py>`, `<YOUR_FILE_3.log>` and so on|
| `APP_USE_CASE` | A brief description of the application's purpose and functionality. | Plain text langugage|
| `USER_TASK` | A description of the specific task the user was performing when the error occurred. | Plain text language |
| `ERROR` | The error message or exception encountered during the debugging scenario. | Plain text language or code snippet |

The following table describes Claude's output variables. Leave these alone:

| Variable | Description |
|----------|-------------|
| `PREDICTIONS` | Claude's educated guesses for potential causes of the error. |
| `SCRATCHPAD` | A designated area for Claude to document the reasoning process and analysis during the debugging. |
| `PROBLEMATIC_CODE` | The specific code segment identified as the root cause of the error. |
| `STEP_BY_STEP_REASONING` | Claude's detailed explanation of the debugging process, from initial assessment to root cause identification. |
| `EXPLANATION` | Claude's detailed explanation of why the identified code segment is the likely root cause of the error. |
| `DEBUG_INSTRUCTIONS` | Step-by-step instructions provided by Claude to resolve the identified issue. |

## Code Block Format

When attaching project files to the debugging prompt, just rename 'YOUR_FILE_1.py' and so forth with your file name. You must have one for every file. 

PRO TOP: Take a screenshot or screenshots of your entire repository folder and use the following prompt in ChatGPT or another conversation of Claude to automate the file's XML tag naming:

Example of real file names to be used in master prompt 
```
<attached_project_code> 

 <business_consulting_chatbot.py>
 {{Attached to convo}} 
</business_consulting_chatbot.py>

  <business_interviewer.py> 
{{Attached to convo}} 
</business_interviewer.py>  

<index.html> 
{{Attached to convo}}
</index.html>

<pdf_conversion.py>
 {{Attached to convo}} 
</pdf_conversion.py>

<prompts.py>
 {{Attached to convo}} 
</prompts.py>

 </attached_project_code>

```

### Prompt for quick automated XML tag file naming:

1. First attach screenshot of repository:

![Screenshot 2024-07-24 at 3 52 39 PM](https://github.com/user-attachments/assets/4b3336d8-61a8-4ed5-b636-f13c072de92e)


3. Use the following prompt in ChatGPT or another conversation of Claude for automated naming:  
```
Analyze the repository in the photo and use the following template to make XML brackets for each file. Leave the inside alone. Write in code block.
"""
<attached_project_code> 
  <YOUR_FILE_1.py>
 {{Attached to convo}} 
</YOUR_FILE_1.py>

  <YOUR_FILE_2.py> 
{{Attached to convo}} 
</YOUR_FILE_2.py>  

<YOUR_FILE_3.log> 
{{Attached to convo}}
</YOUR_FILE_3.log>

 </attached_project_code>
"""

```


Ensure that the code blocks are properly formatted and enclosed within the `<attached_project_code>` tags. Provide the necessary file extensions and language-specific syntax highlighting for better readability.

## Reasoning and Analysis

The Ultimate Debugging Prompt for Claude employs a structured approach to guide Claude's reasoning and analysis process. The prompt breaks down the debugging task into the following steps:

1. **Error Assessment**: Claude examines the provided error message and user task to gain an initial understanding of the problem.
2. **Prediction Generation**: Based on the initial assessment, Claude generates educated predictions for potential causes of the error.
3. **Code Investigation**: Claude meticulously reviews the attached project code, focusing on the segments related to the user task and error.
4. **Prediction Narrowing**: Using a process of elimination, Claude narrows down the predictions by verifying or disproving each one based on code analysis and logical reasoning.
5. **Root Cause Identification**: Claude selects the most likely root cause from the remaining predictions and provides a detailed explanation of why it is the culprit.
6. **Debugging Instructions**: Claude generates clear and actionable step-by-step instructions to resolve the identified issue.

This structured approach ensures that Claude follows a logical and systematic debugging process, leading to accurate and efficient error resolution.

## Integration and Workflow

The Ultimate Debugging Prompt for Claude can be seamlessly integrated into your existing development workflow. Here are some tips for effective integration:

1. **Version Control**: Ensure that your project files are properly versioned using a version control system like Git. This allows you to easily attach the relevant files to the debugging prompt.
2. **Continuous Integration**: Incorporate the debugging prompt into your continuous integration (CI) pipeline. Automatically trigger the prompt when a build fails or when specific error patterns are detected.
3. **Issue Tracking**: Use the debugging prompt in conjunction with your issue tracking system. Attach the prompt's output, including the step-by-step reasoning and debug instructions, to the relevant issue for easy reference and collaboration.
4. **Code Review**: Leverage the debugging prompt during code reviews. Attach the prompt to the review request and use Claude's analysis to facilitate discussions and identify potential issues early in the development process.

Remember to adapt the integration approach based on your specific development environment, tools, and team practices.

## Customization and Extensibility

The Ultimate Debugging Prompt for Claude is designed to be customizable and extensible to suit your specific needs. Consider the following customization options:

1. **Variable Modifications**: Adjust the predefined variables to better align with your project's terminology or add new variables to capture additional debugging information.
2. **Prompt Structure**: Modify the prompt's structure to emphasize specific aspects of the debugging process or to incorporate additional analysis steps.
3. **Language Adaptation**: Tailor the prompt to work with different programming languages by modifying the code block format and providing language-specific examples.
4. **Integration with Other Tools**: Extend the prompt to integrate with other debugging or analysis tools, such as linters, profilers, or test frameworks.

Feel free to experiment with the prompt and share your modifications or improvements with the community. Together, we can continuously enhance the debugging experience with Claude.


## Conclusion

The Ultimate Debugging Prompt for Claude is a powerful tool that leverages Claude's advanced language understanding and reasoning capabilities to revolutionize your debugging workflow. By following the structured approach and utilizing the customization options, you can quickly identify and resolve errors, saving valuable development time.

We encourage you to try out the Ultimate Debugging Prompt for Claude and experience the benefits firsthand. If you have any questions, suggestions, or feedback, please don't hesitate to reach out. Your input is valuable in shaping the future of this debugging solution.

Happy debugging with Claude!
