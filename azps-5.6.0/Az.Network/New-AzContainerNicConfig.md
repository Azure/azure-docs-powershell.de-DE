---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: d9a5d566fe2bff61054b701901079f9173ca3490
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922824"
---
# New-AzContainerNicConfig

## SYNOPSIS
Erstellt ein neues Containernetzwerkschnittstellenkonfigurationsobjekt.

## SYNTAX

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzContainerNicConfig** erstellt ein neues Containernetzwerkschnittstellenkonfigurationsobjekt. Dieses Objekt bestimmt die Merkmale der Containernetzwerkschnittstelle, die auf das übergeordnete Netzwerkprofil bezugt.

## BEISPIELE

### Beispiel 1
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

Mit dem ersten Befehl wird eine leere Containernetzwerkschnittstellenkonfiguration erstellt. Die zweite erstellt ein neues Netzwerkprofil, und übergeben Sie die zuvor erstellte Containernetzwerkschnittstellenkonfiguration als Argument an das New-NetworkProfile cmdlet.

### Beispiel 2

Erstellt ein neues Containernetzwerkschnittstellenkonfigurationsobjekt. (automatisch generiert)

<!-- Aladdin Generated Example -->
```powershell
New-AzContainerNicConfig -IpConfiguration <PSIPConfigurationProfile[]> -Name cnic
```

## PARAMETER

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

### -IpConfiguration
Sammlung von IP-Konfigurationsprofilen, die bestimmen, welche IP-Konfigurationen erstellt werden, wenn eine Containernic aus dieser Containernetzwerkschnittstellenkonfiguration instanziiert wird

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Name der Containernetzwerkschnittstellenkonfiguration.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration

## NOTIZEN

## VERWANDTE LINKS

[New-AzContainerNicConfigIpConfig](./New-AzContainerNicConfigIpConfig.md)
