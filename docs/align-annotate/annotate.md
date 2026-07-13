---
icon: lucide/pen-tool
---
# Annotate
Once the ST and TT tokens are aligned, you may want to annotate the aligned data. This page provides step-by-step guidance on creating and applying an annotation schema.

## 1. Set up an annotation schema
You can either (1) create a new annotation schema or (2) fork an existing default schema.

### (1) Creating your own schema
#### Step 1
Go to **Dashboard** and select **View My Studies**.


#### Step 2
Click **Manage Schemas** in the upper-right corner → Click **Create New Schema** → Enter a **Schema Name** → Choose the access level **Private** or **Public**.

Here we created a private error classification schema for demonstration.

![Schema creation](img/A1.png)

#### Step 3
Click **Add Category** → Assign a **Hotkey** → Set a **Category Code** (for reference only; not displayed on the tokens) → Enter a **Display Name** (shown on the aligned tokens) → Choose where the category can be applied: **Source only**, **Target only**, **Both sides**, or **Either side** (for unaligned tokens) → Select the **Color** and **Icon** for the category.

!!! tip 

    Within each category, you can add multiple severity levels: Neutral, Minor, Major, and Critical.

![Example Schema](img/A2.png)

In this example, we create a category named Mistranslation and define two severity levels: Minor and Major.

#### Step 4
After setting up the categories, click **Save Schema**.

---

### (2) Forking a default schema
Instead of creating a new schema from scratch, you can adapt one of the existing default schemas.

#### Step 1
Navigate to **Dashboard** → **My Studies** → **Manage Schemas** → click **Fork** for the desired schema.

![Forking a schema](img/A3.png)

#### Step 2
Modify the schema as needed in the editing interface.

![Editing a forked schema](img/A4.png)

The remaining steps are identical to Steps 3–4 for creating a new schema.

## 2. Apply the annotation schema to aligned tokens

Once you have an annotation schema, you can apply it to your aligned tokens.

### Step 1
Right-click the token(s) you want to annotate to open the options menu. Then, select an annotation category or use the predefined hotkey to apply the annotation.

![Options menu](img/A5.png)

In this example, the aligned tokens *点心* and *cake* are annotated as Mistranslation (Major).

![Annotated aligned tokens](img/A6.png)

An asterisk, the predefined icon for this category, will appear on the annotated tokens to indicate that the annotation has been applied.

### Step 2 
Tick **Done** or click **Save Alignments** to save your annotations.

!!! note

    ·Each study can use only one annotation schema. You cannot assign different annotation schemas to different sessions within the same study.

    ·Once annotations have been added to any session using the current annotation schema, you cannot switch to a different schema until those annotations are removed.

    ·To remove an annotation, right-click the annotated tokens and select the same annotation category again.

    ·After making any changes, don't forget to click Done or Save Alignments to save your work.📝

## 3. View public annotated datasets
Some public studies, such as DG21error and AR22, include annotations. You can view these annotations by opening the aligned ST and TT.

### Step 1
Navigate to **Dashboard** → Click **the eye icon** in the rightmost column → **View Sessions** → **Open Aligner**.

The following example is taken from AR22.

![Annotated English-Arabic tokens](img/A7.png)

### Step 2
Click **Annotation Schema** to see what the icons represent.

![AR22 schema](img/A8.png)

By referring to the schema, we can see that the Arabic translations of *in* and *early* are annotated as Critical Mistranslation and Critical Cohesion, respectively.























