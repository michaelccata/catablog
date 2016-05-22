---
title: 'Contact us'
menu: 'Coffee?'
form:
    name: contact-form
    fields:
        - name: name
          label: 'Name'
          placeholder: 'Enter your name'
          autofocus: on
          autocomplete: on
          type: text
          classes: w-input text-field
          validate:
            required: true

        - name: email
          label: 'Email Address'
          placeholder: 'Enter your email address'
          type: text
          classes: w-input text-field
          validate:
            rule: email
            required: true

        - name: message
          label: 'Message'
          placeholder: "Enter your message"
          size: long
          rows: 6
          type: textarea
          classes: w-input text-field text-area
          validate:
            required: true

    buttons:
        - type: submit
          value: Submit

    process:
        - email:
            from: "{{ config.plugins.email.from }}"
            to:
              - "{{ config.plugins.email.from }}"
            subject: "Message from {{ form.value.name|e }}"
            body: "{% include 'forms/data.html.twig' %}"
        - save:
            fileprefix: contact-
            dateformat: Ymd-His-u
            extension: txt
            body: "{% include 'forms/data.txt.twig' %}"
        - display: thank-you
---

Morbi leo risus, porta ac consectetur ac, vestibulum at eros. Etiam porta sem malesuada magna mollis euismod. Etiam porta sem malesuada magna mollis euismod. Aenean eu leo quam. Pellentesque ornare sem lacinia quam venenatis vestibulum.
