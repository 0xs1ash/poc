# The words entered are displayed again on the page within the input field without being sanitized, which creates the potential for an XSS attack.
	

## 1) Stored XSS.
   
_Exposed  Address:  Settings/Email/Signature/EditHtmlSource_
<img width="643" alt="19-03-2025-04-17-23" src="https://github.com/user-attachments/assets/246be7a6-d48f-4519-a628-5127bdd7b028" />

Picture 2.1. Bypassing the filter in the EditHTMLSource section and executing malicious JavaScript.

<img width="647" alt="19-03-2025-04-17-52" src="https://github.com/user-attachments/assets/5575c064-5fde-418d-9d29-7919591cdfc6" /> 

Picture 2.2 Written malicious code and its execution.

<img width="642" alt="19-03-2025-04-18-05" src="https://github.com/user-attachments/assets/899ca600-f820-4395-bd3e-3c87c6d2f1d4" />

Picture 2.3. 

------

## 2) When a file with a malicious JavaScript code in its name is uploaded to the system, it is displayed again on the page within the input field without being sanitized. This creates the potential for an XSS attack.

<img width="640" alt="19-03-2025-04-18-36" src="https://github.com/user-attachments/assets/f03e9b6f-6341-4b34-a52a-b07932520950" />

Picture 2.4. ATTACHMENT . Exposed Address.


<img width="655" alt="19-03-2025-04-18-59" src="https://github.com/user-attachments/assets/8e8a1a1f-bb8d-4ab5-bde5-4ff6d9da75c6" />

Picture 2.5 Uploading a malicious file with a harmful filename to the system and executing the malicious JavaScript code..


<img width="651" alt="19-03-2025-04-23-28" src="https://github.com/user-attachments/assets/b5446cc0-5baf-41b4-897b-367fe90e7437" />

Picture 2.6 The malicious JavaScript code of that file being reflected in the source.

## SOLUTION
_After properly sanitizing and escaping user-side parameters, echo them to the user's browser. You can achieve this in PHP programming language with the help of the following functions:
**htmlspecialchars(), urlencode(), strip_tags, htmlentities(), preg_replace()**, etc._
## References:
https://www.owasp.org/index.php/XSS_(Cross_Site_Scripting)_Prevention_Cheat_Sheet
https://www.wordfence.com/learn/how-to-prevent-cross-site-scripting-attacks/
http://resources.infosecinstitute.com/how-to-prevent-cross-site-scripting-attacks/
http://php.net/manual/en/function.htmlspecialchars.php
