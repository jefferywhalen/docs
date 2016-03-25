<!--
title: "Common Java Keytool Commands"
description: "Common Keytool commands and workflows"
tags: "configuration SSL EOP administration tools keytool"
-->
# Who Should Read this Document
This is an overview of useful commands and introductory principles for a person assuming system administration of Contrast TeamServer EOP and agent deployment where SSL is part of your deployment.  Examples presented below are not presented as a step-by-step document but intended to be helpful for debugging SSL/HTTPS problems when your first try is unsuccessful.

Some situations where you may need to use the `keytool` include:
* Setting up TeamServer HTTPS
* Integrating with LDAP or Active Directory where you see `ldaps://`
* Securing communication between agents and TeamServer.

## Certificate Signing Request
1. Generate a Private Key and a CSR
2. Generate a CSR from an Existing Private Key

## SSL Certificates
1. Generate a Self-Signed Certificate
2. Generate a Self-Signed Certificate from an Existing Private Key

## View Certificates
1. View CSR Entries
2. View Certificate Entries
3. Verify a Certificate was Signed by a CA

## Creating the Keystore
1. Generate Keys in New/Existing Keystore
2. Generate CSR For Existing Private Key
3. Import Signed/Root/Intermediate Certificate
4. Generate Self-Signed Certificate in New/Existing Keystore

## Viewing Keystore
1. List Keystore Certificate Fingerprints
2. List Verbose Keystore Contents
3. Use Keytool to View Certificate Information
4. Export Certificate

## Editing the Keystore
1. Change Keystore Password
2. Delete Alias
3. Rename Alias
