---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 95908e6b0976baf2ce9f3c117f54a6f1552e4957
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663942"
---
# Set-AzureRmDtlVMsPerLabPolicy

## Synopsis
Legt die virtuellen Computer pro Lab-Richtlinie einer Übungseinheit in DevTest Labs fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Aktivieren (Standard)
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Deaktivieren
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Set-AzureRmDtlVMsPerLabPolicy** werden die virtuellen Computer pro Lab-Richtlinie für eine Übungseinheit festgelegt, wodurch die Gesamtzahl der in einer Übungseinheit zulässigen virtuellen Computer festgelegt wird.
Das Cmdlet verwendet die angegebene Ressourcengruppe und den Namen der Übungseinheit, um die Richtlinie festzulegen.

## Beispiele

## Parameter

### -Deaktivieren Sie
Gibt an, dass dieses Cmdlet die Richtlinie der Übungseinheit deaktiviert.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Gibt an, dass dieses Cmdlet die Richtlinie der Übungseinheit aktiviert.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LabName
Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die virtuellen Computer pro Lab-Richtlinie festlegt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxVMs
Gibt die maximale Anzahl virtueller Computer an, die in der Übungseinheit erstellt werden können.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy
Dieses Cmdlet gibt die Richtlinie zurück, die die maximale Anzahl virtueller Computer angibt, die in der Übungseinheit erstellt werden können.

## Notizen

## Verwandte Links

[Get-AzureRmDtlVMsPerLabPolicy](./Get-AzureRmDtlVMsPerLabPolicy.md)


