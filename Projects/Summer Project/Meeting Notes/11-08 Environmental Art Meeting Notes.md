
## Asset Import Settings
- Our baked lighting was messed up and we couldn't figure out why.
- It turns out, the default import settings for models are TERRIBLE when it comes to the lightmap settings.
- So, whenever you guys import any models:

1. Open the model within Unreal
2. In the details panel for the model, look up "light"
3. In the fields for "Min Lightmap Resolution" and "Light Map Resolution", set the value to 32 or 64.

![](<../../../_Meta/Attachments/Pasted image 20251108145537.png>)