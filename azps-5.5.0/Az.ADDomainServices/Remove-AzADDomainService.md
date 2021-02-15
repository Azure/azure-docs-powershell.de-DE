---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/remove-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
ms.openlocfilehash: f29fbbdd805abb9891f707ed983bcf8aebefc46c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143820"
---
# Remove-AzADDomainService

## SYNOPSIS
Beim Vorgang "Delete Domain Service" wird ein vorhandener Domänendienst gelöscht.

## SYNTAX

### Löschen (Standard)
```
Remove-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DeleteViaIdentity
```
Remove-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESCHREIBUNG
Beim Vorgang "Delete Domain Service" wird ein vorhandener Domänendienst gelöscht.

## BEISPIELE

### Beispiel 1: Löschen der AzADDomain nach ResourceGroupName und Name
```powershell
PS C:\> Remove-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName

```

Löschen der AzADDomain nach "ResourceGroupName" und "Name"

### Beispiel 2: Löschen der AzADDomain von InputObject
```powershell
PS C:\> $GetADDomainExample = Get-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName
Remove-AzADDomainService -InputObject $GetADDomainExample

```

Löschen der AzADDomain von InputObject

## PARAMETERS

### -AsJob
Ausführen des Befehls als Auftrag

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

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name des Domänendiensts.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Asynchrones Ausführen des Befehls

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

### -PassThru
Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.

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

### -ResourceGroupName
Der Name der Ressourcengruppe im Abonnement des Benutzers.
Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.
Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity

## AUSGABEN

### System.Boolean

## HINWEISE

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften. Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.


INPUTOBJECT <IAdDomainServicesIdentity> : Identity Parameter
  - `[DomainServiceName <String>]`: Der Name des Domänendiensts.
  - `[Id <String>]`: Ressourcenidentitätspfad
  - `[ResourceGroupName <String>]`: Der Name der Ressourcengruppe im Abonnement des Benutzers. Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.
  - `[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird. Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.

## LINKS ZU VERWANDTEN THEMEN

