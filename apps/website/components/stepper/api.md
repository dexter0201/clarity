---
title: API
toc: true
---

## Angular Components

{.section-header}

### ClrStepper

A Stepper structures a multi-step process into two or more expanding panels.

#### Selector & Basic Usage

<DocDemo toggle="false">

```html
<!-- template form -->
<form clrStepper #contactForm="ngForm" (ngSubmit)="templateFormSubmit(contactForm.value)">
  <!-- multiple clr-step-panel children -->
</form>

<!-- reactive form -->
<form clrStepper [formGroup]="form" (ngSubmit)="reactiveFormSubmit()">
  <!-- multiple clr-step-panel children -->
</form>
```

</DocDemo>

### ClrStepPanel

ClrStepperPanel extends [ClrAccordionPanel](../accordion/api/#clraccordionpanel)

#### Selector & Basic Usage

<DocDemo toggle="false">

```html
<!-- template form -->
<form clrStepper #contactForm="ngForm" (ngSubmit)="templateFormSubmit(contactForm.value)">
  <clr-stepper-panel ngModelGroup="name">
    <!-- clr-step-title -->
    <!-- clr-step-description -->
    <!-- clr-step-content -->
  </clr-stepper-panel>
</form>
<!-- reactive form -->
<form clrStepper [formGroup]="form" (ngSubmit)="reactiveFormSubmit()">
  <!-- multiple clr-step-panel children -->
  <clr-stepper-panel formGroupName="name">
    <!-- clr-step-title -->
    <!-- clr-step-description -->
    <!-- clr-step-content -->
  </clr-stepper-panel>
</form>
```

</DocDemo>

### ClrStepTitle

#### Selector & Basic Usage

<DocDemo toggle="false">

```html
<!-- clr-step-title is the same for template or reactive forms -->
<form clrStepper [formGroup]="form" (ngSubmit)="submit()">
  <clr-stepper-panel formGroupName="name">
    <clr-step-title>Legal Name</clr-step-title>
    <!-- clr-step-description -->
    <!-- clr-step-content -->
  </clr-stepper-panel>
</form>
```

</DocDemo>

**Note:** `clr-step-title` is an overloaded selector and is the same component as [ClrAccordionTitle](../accordion/api/#clraccordiontitle)

### ClrStepDescription

#### Selector & Basic Usage

<DocDemo toggle="false">

```html
<!-- clr-step-description is the same for template or reactive forms -->
<form clrStepper [formGroup]="form" (ngSubmit)="submit()">
  <clr-stepper-panel formGroupName="name">
    <!--clr-step-title -->
    <clr-step-description>Step description</clr-step-description>
    <!-- clr-step-content -->
  </clr-stepper-panel>
</form>
```

</DocDemo>

**Note:** `clr-step-description` is an overloaded selector and is the same component as [ClrAccordionDescription](../accordion/api/#clraccordiondescription)

### ClrStepContent

#### Selector & Basic Usage

<DocDemo toggle="false">

```html
<!-- clr-step-content is the same for template or reactive forms -->
<form clrStepper [formGroup]="form" (ngSubmit)="submit()">
  <clr-stepper-panel formGroupName="name">
    <!-- clr-step-title -->
    <!-- clr-step-description -->>
    <clr-step-content>Step description</clr-step-content>
  </clr-stepper-panel>
</form>
```

</DocDemo>

**Note:** `clr-step-content` is an overloaded selector and is the same component as [ClrAccordionContent](../accordion/api/#clraccordioncontent)

## Angular Directives

{.section-header}

### ClrStepButton

#### Selector & Basic Usage

<DocDemo toggle="false">

```html
<!-- reactive forms -->
<form clrStepper [formGroup]="form" (ngSubmit)="reactiveFormSubmit()">
  <clr-stepper-panel formGroupName="name">
    <!-- clr-step-title -->
    <!-- clr-step-description-->
    <clr-step-content *clrIfExpanded>
      <!--one or more clr-control-containers -->
      <button clrStepButton="next">next</button>
    </clr-step-content>
  </clr-stepper-panel>

  <clr-stepper-panel formGroupName="name">
    <!-- clr-step-title -->
    <!-- clr-step-description-->
    <clr-step-content *clrIfExpanded>
      <!--one or more clr-control-containers -->
      <button clrStepButton="submit">submit</button>
    </clr-step-content>
  </clr-stepper-panel>
</form>

<!-- template forms -->
<form clrStepper #contactForm="ngForm" (ngSubmit)="templateFormSubmit(contactForm.value)">
  <clr-stepper-panel ngModelGroup="name">
    <!-- clr-step-title -->
    <!-- clr-step-description-->
    <clr-step-content>
      <!--one or more clr-control-containers -->
      <button clrStepButton="next">next</button>
    </clr-step-content>
  </clr-stepper-panel>

  <clr-stepper-panel ngModelGroup="password">
    <!-- clr-step-title -->
    <!-- clr-step-description-->
    <clr-step-content>
      <!--one or more clr-control-containers -->
      <button clrStepButton="submit">submit</button>
    </clr-step-content>
  </clr-stepper-panel>
</form>
```

</DocDemo>

#### Bindings

<DocComponentApi component="ClrStepButton" item="bindings" />
