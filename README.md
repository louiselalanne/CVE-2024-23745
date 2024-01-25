# CVE-2024-23745
In Notion Web Clipper 1.0.3(7), a .nib file is susceptible to the Dirty NIB attack. NIB files can be manipulated to execute arbitrary commands. Additionally, even if a NIB file is modified within an application, Gatekeeper may still permit the execution of the application, enabling the execution of arbitrary commands within the application's context.

## Impact
 Attackers could exploit this vulnerability to execute unauthorized commands within the Notion application, potentially compromising sensitive user data or performing malicious actions.

## PoC
- First, you need create de malicious NIB

<img width="592" alt="image1" src="https://github.com/louiselalanne/CVE-2024-23745/assets/100588945/21768f9c-f0e2-4987-b0eb-89691777ed17">
</br>
<img width="253" alt="image2" src="https://github.com/louiselalanne/CVE-2024-23745/assets/100588945/d5cef122-b6fa-44f5-92ad-fac6f3627b71">
</br>
<img width="380" alt="image3" src="https://github.com/louiselalanne/CVE-2024-23745/assets/100588945/d82514c8-b6bb-4a40-94eb-c47db86228f9">
</br>
<img width="382" alt="image4" src="https://github.com/louiselalanne/CVE-2024-23745/assets/100588945/c3adaa53-547c-49d4-bdc6-27e519fe9dbd">
</br>
More details in: https://blog.xpnsec.com/dirtynib/
</br>
</br>
- Notion Application
</br>
</br>
<img alt="image6" src="https://github.com/louiselalanne/CVE-2024-23745/assets/100588945/b6786f30-59fe-482c-827a-cde49930bc36">
</br>
<img alt="image7" src="https://github.com/louiselalanne/CVE-2024-23745/assets/100588945/5c897fea-1271-45e2-bbe6-1bbfc4afec44">
</br>
- Copy malicious nib to app
</br>
</br>
<img alt="image8" src="https://github.com/louiselalanne/CVE-2024-23745/assets/100588945/64f2e7c6-0d25-4bb9-877b-47a1dda0aa5d">
</br>
<img alt="image9" src="https://github.com/louiselalanne/CVE-2024-23745/assets/100588945/e0cc2e78-6f55-41a9-8b91-8dfe8929aec0">
</br>
- Open the malicous application
</br>
</br>
<img alt="image10" src="https://github.com/louiselalanne/CVE-2024-23745/assets/100588945/2f5ed801-0cb5-4f0c-bb66-38e7c2f9f59f">

## Thanks
Thanks to Giovanni Lima, Cyber Security Engineer and friend. We worked together to reproduce de Dirty Nib PoC 😎

## References:</br>
https://book.hacktricks.xyz/macos-hardening/macos-security-and-privilege-escalation/macos-proces-abuse/macos-dirty-nib</br>
https://www.notion.so/web-clipper
