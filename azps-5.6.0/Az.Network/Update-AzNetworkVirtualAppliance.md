---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 8a1712fa995790c80e2b8d42bb5d76b2404aa1f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918432"
---
# Update-AzNetworkVirtualAppliance

## SYNOPSIS
Aktualisieren oder Ändern einer virtuellen Netzwerkgerätressource.

## SYNTAX

```
Update-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String>
 [-Sku <PSVirtualApplianceSkuProperties>] [-VirtualApplianceAsn <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Die Update-AzNetworkVirtualAppliance ändert eine virtuelle Netzwerkgerätressource.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> Update-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -VirtualApplianceAsn 1234
```

Ändern Sie die ASN-Nummer der virtuellen Einheit.

### Beispiel 2

Aktualisieren oder Ändern einer virtuellen Netzwerkgerätressource. (automatisch generiert)

<!-- Aladdin Generated Example -->
```powershell
Update-AzNetworkVirtualAppliance -Name nva -ResourceGroupName testrg -Sku <PSVirtualApplianceSkuProperties>
```

## PARAMETER

### -AsJob
Ausführen des Cmdlets im Hintergrund

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Erzwingen
Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten

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

### -Name
Der Ressourcenname.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
Die Sku der virtuellen Appliance.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Eine Hashtable, die Ressourcentags darstellt.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualApplianceAsn
Die ASN-Nummer der virtuellen Appliance.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System.String

### Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties

### System.Int32

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance

## NOTIZEN

## VERWANDTE LINKS
