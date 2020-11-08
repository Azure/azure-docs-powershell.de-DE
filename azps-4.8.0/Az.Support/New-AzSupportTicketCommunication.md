---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166737"
---
# New-AzSupportTicketCommunication

## Synopsis
Erstellt eine neue Support Ticket-Kommunikation.

## Syntax

### CreateByNameParameterSet (Standard)
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### CreateByParentObjectParameterSet
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Fügt eine neue Kundenkommunikation zu einem Azure Support-Ticket hinzu.

## Beispiele

### Beispiel 1
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## Parameter

### -AsJob
Führen Sie das Cmdlet im Hintergrund aus.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Body
Der Text der Kommunikation.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der Kommunikationsressource.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Absender
E-Mail-Adresse des Absenders.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Betreff
Betreff der Kommunikation.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportTicketName
Name des Support Tickets

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportTicketObject
Support-Ticket-Objekt.

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. Support. Models. PSSupportTicket

## Ausgaben

### Microsoft. Azure. Commands. Support. Models. PSSupportTicketCommunication

## Notizen

## Verwandte Links
