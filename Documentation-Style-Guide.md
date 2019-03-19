# Markdown documentation guidelines
This page provides style guidelines for writing documentation, mainly API documentation, in Markdown. These are guidelines, not rules. Use your best judgment, and feel free to propose changes to this document.

**Tip:** For a Markdown syntax cheatsheet, see this [GitHub flavored markdown handout](https://enterprise.github.com/downloads/en/markdown-cheatsheet.pdf).

## Formatting standards

With the exception of the first item below, which is a new standard, and some of the points under [Inline code formatting](#inline), the formatting rules below conform to our TechPubs style  guide. 

### Referring to API objects

When you refer to an API object, use the same uppercase and lowercase letters that are used in the actual object name. 

Don't split the API object name into separate words. For example, use TalkAgent, not Talk Agent.

Refer to API objects without including "object," unless omitting "object" leads to an awkward construction.

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>The Pod has two containers.</td><td>The pod has two containers.</td></tr>
  <tr><td>The NinaMobileController is responsible for ...</td><td>The NinaMobileController object is responsible for ...</td></tr>
  <tr><td>A PodList is a list of Pods.</td><td>A Pod List is a list of pods.</td></tr>
  <tr><td>The two TalkAgentRequests ...</td><td>The two TalkAgentRequest objects ...</td></tr>
  <tr><td>The two ContainerStateTerminated objects ...</td><td>The two ContainerStateTerminateds ...</td></tr>
</table>

### Use italics for placeholder text

When you use italics for placeholders, always tell the reader what the placeholder represents.

For example:

DELETE base_URL/jobs/_job_id_

Where *job_id* is a reference as returned by a job request (such as a batch transcription) or job query command. 

(Presumably base_URL is explained somewhere as well, probably in an earlier topic, in which case the string itself may be a hyperlink.)

### Use italics to define or introduce new terms

Optional. Use italics if you wish, the first time the term is mentioned. 

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>A <i>cluster</i> is a set of nodes ...</td><td>A "cluster" is a set of nodes ...</td></tr>
  <tr><td>These components form the <i>control plane.</i></td><td>These components form the <strong>control plane.</strong></td></tr>
</table>

### Use italics for filenames, directories, and paths

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>Open the <em>envars.yaml</em> file.</td><td>Open the <code>envars.yaml</code> file.</td></tr>
  <tr><td>Go to the <em>/docs/tutorials</em> directory.</td><td>Go to the /docs/tutorials directory.</td></tr>
</table>

### Place punctuation inside quotes

Unless you are showing a literal string in a code example, or punctuation is part of the quoted material, place periods, commas, and other end punctuation inside the closing quote.

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>When prompted by the application, say, "Account balance."</td><td>When prompted by the application, say, "Account balance".</td></tr>
  <tr><td>What is meant by "user experience"?</td><td>What is meant by "user experience?"</td></tr>
  <tr><td>A user asks, "How do I create a new intent?"</td><td>A user asks, "How do I create a new intent"?</td></tr>
  <tr><td>Open a command-prompt window and enter:<br /><code>wm.smnp.V2TrapHandlers="localhost:1234"</code></td><td>Open a command-prompt window and enter wm.smnp.V2TrapHandlers="localhost:1234."</td></tr>
</table>
## Inline code formatting<a id="inline"></a>

### Use code style for inline code and commands

In Markdown, use the backtick (\`). For inline code in HTML, such as within an HTML table, use the `code` tag.

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>The <code>startSession</code> command starts a session.</td><td>The "startSession" command starts a session.</td></tr>
  <tr><td>To check if you have Git installed, open a command prompt and type <code>git --version</code>.</td><td>To check if you have Git installed, open a command prompt and type "git --version".</td></tr>  
  <tr><td>For declarative management, use <code>kubectl apply</code>.</td><td>For declarative management, use "kubectl apply".</td></tr>
</table>

### Use code style for object field names and properties, methods...

Use code font for object field names and properties, methods and functions, XML and HTML element names (with their angle brackets), and attribute names and values.

For methods, omit the class name unless it's needed to prevent ambiguity. Use parentheses with a method call, even if no parameters are passed, to clearly indicate that it is a method.

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>Set <code>application_name</code> in the configuration file.</td><td>Set "application_name" in the configuration file.</td></tr>
    <tr><td>The <code>fullfill()</code> method tells the runtime...</td><td>The <code>state.fulfill()</code> method tells the runtime...</td></tr>
  <tr><td>The value of <code>exec</code> is an ExecAction object.</td><td>The value of the <em>exec</em> field is an ExecAction object.</td></tr>
</table>

### Use normal style for string and integer field values

For field values of type string or integer, use normal style without quotation marks.

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>Set the value of <code>kryptonEnableProfanityFilter</code> to true to enable profanity filtering.</td><td>Set the value of <code>kryptonEnableProfanityFilter</code> to "true".</td></tr>
  <tr><td>Set the value of <code>image</code> to nginx:1.8.</td><td>Set the value of <code>image</code> to <code>nginx:1.8</code>.</td></tr>
  <tr><td>Set the value of the <code>replicas</code> field to 2.</td><td>Set the value of the <code>replicas</code> field to <code>2</code>.</td></tr>
</table>

## Code snippet formatting

### Don't include the command prompt

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>kubectl get pods</td><td>$ kubectl get pods</td></tr>
</table>

### Separate commands from output

Verify that the Pod is running on your chosen node:

    kubectl get pods --output=wide

The output is similar to this:

    NAME     READY     STATUS    RESTARTS   AGE    IP           NODE
    nginx    1/1       Running   0          13s    10.200.0.4   worker0

## Code samples

For including code samples, see [this Slate Markdown syntax reference in GitHub](https://github.com/lord/slate/wiki/Markdown-Syntax#code-samples). 

Always remember to put the code snippet first, to correctly align the text in the center column with the code on the right.

## Notes and warnings

In Slate documentation you can add highlighted warnings and notes using the \<aside\> HTML element. For more information see the above link.

### Note

Use class="notice" to highlight a tip or a piece of information that may be helpful to the reader.

For example:

```
<aside class="notice">
You can _still_ use Markdown inside these callouts.
</aside>
```

### Warning

Use class="warning" to indicate danger or a piece of information that is crucial to follow.

For example:

```
<aside class="warning">
Beware.
</aside>
```

## Content best practices

This section contains suggested best practices for writing clear, concise, and consistent content. The main principles are the same as those found in our TechPubs Style Guide.

### Use present tense

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>This command starts a session.</td><td>This command will start a session.</td></tr>
</table>

Exception: Use future or past tense if it is required to convey the correct meaning.

### Use active voice

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>You can explore the API using a browser.</td><td>The API can be explored using a browser.</td></tr>
  <tr><td>The YAML file specifies the configuration settings.</td><td>The configuration settings are specified in the YAML file.</td></tr>
</table>

Exception: Use passive voice if active voice leads to an awkward construction.

### Use simple and direct language

Avoid using unnecessary phrases, such as "in order to" and "please."

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>To create a session, ...</td><td>In order to create a session, ...</td></tr>
  <tr><td>See the configuration file.</td><td>Please see the configuration file.</td></tr>
  <tr><td>View the JSON output.</td><td>With this next command, we'll view the JSON output.</td></tr>
</table>

### Address the reader as "you" only when necessary

In general use the imperative. However, you can use "you" when necessary.

<table>
  <tr><th>Do</th><th>Don't</th></tr>
   <tr><td>To implement a new universal, add the phrase to the <em>universal.gsl</em> file.</td><td>To implement a new universal, you add the phrase to the <em>universal.gsl</em> file.</td></tr>
    <tr><td>In the preceding output, you can see...</td><td>In the preceding output, we can see ...</td></tr>
</table>
### Avoid Latin phrases

Prefer English terms over Latin abbreviations.

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>For example, ...</td><td>e.g., ...</td></tr>
  <tr><td>That is, ...</td><td>i.e., ...</td></tr>
  <tr><td>...and so on, ...</td><td>...etc., ...</td></tr>
</table>
## Patterns to avoid

### Avoid using "we"

It's potentially confusing and not necessary.

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>Version 1.4 includes ...</td><td>In version 1.4, we have added ...</td></tr>
  <tr><td>Web API provides a new feature for ...</td><td>We provide a new feature ...</td></tr>
  <tr><td>This section describes how to...</td><td>In this section, we describe how to...</td></tr>
</table>
### Avoid jargon and idioms

Some readers speak English as a second language. Avoid jargon and idioms to prevent confusion.

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>Internally, ...</td><td>Under the hood, ...</td></tr>
    <tr><td>Create a new cluster.</td><td>Turn up a new cluster.</td></tr>
</table>

### Avoid statements that will soon be out of date

Avoid words like "currently" and "new." A feature that is new today might not be considered new in a few months.

<table>
  <tr><th>Do</th><th>Don't</th></tr>
  <tr><td>In version 1.4, ...</td><td>In the current version, ...</td></tr>
    <tr><td>The command-chaining feature provides ...</td><td>The new command-chaining feature provides ...</td></tr>
</table>
