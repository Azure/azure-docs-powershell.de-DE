---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: 4adda2affcba1c29352f6fe9235a5f10a3c1382a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165006"
---
# Update-AzTag

## Synopsis

Aktualisiert selektiv die Gruppe von Tags für eine Ressource oder ein Abonnement.

## Syntax

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOpeation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## Beschreibung

Das Cmdlet " **Update-AzTag** " mit einer Ressourcen-Kennung aktualisiert selektiv die Gruppe von Tags für eine Ressource **oder ein Abonnement** .
Dieser Vorgang ermöglicht das ersetzen, Zusammenführen oder selektives Löschen von Tags für die angegebene Ressource oder das angegebene Abonnement. Die angegebene Entität kann am Ende des Vorgangs maximal 50-Tags enthalten. Mit der Option "ersetzen" wird der gesamte Satz vorhandener Tags durch einen neuen Satz ersetzt. Mit der Option "Zusammenführen" können Sie Tags mit neuen Namen hinzufügen und die Werte von Tags mit vorhandenen Namen aktualisieren. Die Option "Löschen" ermöglicht das selektive Löschen von Tags auf der Grundlage von angegebenen Namen oder Name-Wert-Paaren.

## Beispiele

### Beispiel 1: selektives Aktualisieren der Gruppe von Transpondern in einem Abonnement mit dem Vorgang "Zusammenführen"

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

Dieser Befehl führt die Gruppe von Tags im Abonnement mit {subId} zusammen.

### Beispiel 2: selektives Aktualisieren der Gruppe von Transpondern in einem Abonnement mit dem Vorgang "ersetzen"

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

Dieser Befehl Repalces den Satz von Tags für das Abonnement mit {subId}.

### Beispiel 3: selektives Aktualisieren der Gruppe von Transpondern in einem Abonnement mit dem Vorgang "Löschen"

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

Mit diesem Befehl wird der Satz von Tags im Abonnement mit {subId} gelöscht.

## Parameter

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

### -Resourcen-Nr
Der Ressourcenbezeichner für die markierte Entität. Eine Ressource, eine Ressourcengruppe oder ein Abonnement können markiert sein.

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
Die Gruppe von Tags, die für die Aktualisierung verwendet werden sollen.

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

### -Vorgang
Der Aktualisierungsvorgang. Optionen sind "Zusammenführen", "ersetzen" und "Löschen".

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### Microsoft. Azure. Commands. Tags. Model. TagPatchOpeation

### System. Collections. Hashtable

## Ausgaben

### Microsoft. Azure. Commands. Tags. Model. PSTagResource

## Notizen

## Verwandte Links

[Get-AzTag](./Get-AzTag.md)

[Neu – AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)
