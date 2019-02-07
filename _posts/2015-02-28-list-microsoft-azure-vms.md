---
layout: post
title: List Microsoft Azure VMs
redirect_from:
    - /post/list-microsoft-azure-vms
---
*Update:* I am not sure if these are of any use anymore
### Get all Microsoft Published Azure VMs

    ( Get-AzureVMImage | where-object { $_.PublisherName -like "Microsoft*" } ) | Format-List -Property Label, ImageName -GroupBy PublisherName | Out-String

### Scratch Testing Queries
*Table*

    ( Get-AzureVMImage | where-object { $_.PublisherName -like "*Visual*Studio*" } ) | Format-Table -Property Label, ImageName -AutoSize -GroupBy PublisherName | Out-String

*List*

    ( Get-AzureVMImage | where-object { $_.PublisherName -like "*Visual*Studio*" } ) | Format-List -Property Label, ImageName -GroupBy PublisherName | Out-String