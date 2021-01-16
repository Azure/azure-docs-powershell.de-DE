---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: 3423331e36fd9fbd636a1ae877275badd5912324
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460812"
---
# Update-AzTag

## SYNOPSIS

Aktualisiert die Gruppe von Markierungen für eine Ressource oder ein Abonnement selektiv.

## SYNTAX

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOperation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## BESCHREIBUNG

Das **Cmdlet "Update-AzTag"** mit einer **"ResourceId"** aktualisiert selektiv die Markierungen einer Ressource oder eines Abonnements.
Dieser Vorgang ermöglicht das Ersetzen, Zusammenführen oder selektive Löschen von Tags für die angegebene Ressource oder das angegebene Abonnement. Die angegebene Entität kann am Ende des Vorgangs maximal 50 Tags enthalten. Die Option "Ersetzen" ersetzt den gesamten Satz vorhandener Tags durch einen neuen Satz. Die Option "Zusammenführen" ermöglicht das Hinzufügen von Tags mit neuen Namen und das Aktualisieren der Werte von Tags mit vorhandenen Namen. Die Option "Löschen" ermöglicht das selektive Löschen von Tags basierend auf bestimmten Namen oder Name/Wert-Paaren.

## BEISPIELE

### Beispiel 1: Selektives Aktualisieren der Gruppe von Markierungen in einem Abonnement mit "Zusammenführen"-Vorgang

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

Mit diesem Befehl werden die Markierungen im Abonnement mit {subId} zusammengeführt.

### Beispiel 2: Selektives Aktualisieren der Gruppe von Tags in einem Abonnement durch "Ersetzen"-Vorgang

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

Mit diesem Befehl wird die Gruppe von Tags für das Abonnement mit {subId} erneut umschalten.

### Beispiel 3: Selektives Aktualisieren der Gruppe von Markierungen in einem Abonnement mit dem Vorgang "Löschen"

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

Mit diesem Befehl wird die Gruppe von Tags für das Abonnement mit {subId} gelöscht.

## PARAMETERS

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

### -ResourceId
Der Ressourcenbezeichner für die markierte Entität. Möglicherweise ist eine Ressource, eine Ressourcengruppe oder ein Abonnement markiert.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Die Gruppe von Tags, die für die Aktualisierung verwendet werden.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Operation
Der Aktualisierungsvorgang. Die Optionen sind "Zusammenführen", "Ersetzen" und "Löschen".

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOperation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Tags.Model.TagPatchOperation

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.Tags.Model.PSTagResource

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)
