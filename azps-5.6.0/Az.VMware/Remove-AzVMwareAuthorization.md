---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareAuthorization.md
ms.openlocfilehash: b45e06bd6d70e2c5e0999ce3f9be678580f07048
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936392"
---
# Remove-AzVMWareAuthorization

## SYNOPSIS
Löschen einer ExpressRoute-Schaltkreisautorisierung in einer privaten Cloud

## SYNTAX

### Löschen (Standard)
```
Remove-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### DeleteViaIdentity
```
Remove-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESCHREIBUNG
Löschen einer ExpressRoute-Schaltkreisautorisierung in einer privaten Cloud

## BEISPIELE

### Beispiel 1: Löschen der Autorisierung für die private Cloud
```powershell
PS C:\> Remove-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

Löschen der Autorisierung für die private Cloud

## PARAMETER

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
Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AuthorizationName

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
Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.

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

### -PrivateCloudName
Name der privaten Cloud

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

### -ResourceGroupName
Der Name der Ressourcengruppe.
Der Name ist groß- und kleinschreibungsunabhängiger.

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
Die ID des Zielabonnements.

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

### -Bestätigen
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

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity

## AUSGABEN

### System.Boolean

## NOTIZEN

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält. Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.


INPUTOBJECT <IVMWareIdentity> : Identitätsparameter
  - `[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud
  - `[ClusterName <String>]`: Name des Clusters in der privaten Cloud
  - `[HcxEnterpriseSiteName <String>]`: Name der HCX Enterprise-Website in der privaten Cloud
  - `[Id <String>]`: Ressourcenidentitätspfad
  - `[Location <String>]`: Azure Region
  - `[PrivateCloudName <String>]`: Name der privaten Cloud
  - `[ResourceGroupName <String>]`: Der Name der Ressourcengruppe. Der Name ist groß- und kleinschreibungsunabhängiger.
  - `[SubscriptionId <String>]`: Die ID des Zielabonnements.

## VERWANDTE LINKS

