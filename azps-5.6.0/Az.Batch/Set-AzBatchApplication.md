---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
ms.openlocfilehash: b96d65354522e72e9eb96f585aeb2847fe5ee883
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925216"
---
# Set-AzBatchApplication

## SYNOPSIS
Aktualisiert die Einstellungen für die angegebene Anwendung.

## SYNTAX

```
Set-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzBatchApplication** ändert die Einstellungen für die angegebene Azure Batch-Anwendung.

## BEISPIELE

### Beispiel 1: Aktualisieren einer Anwendung in einem Batchkonto
```powershell
PS C:\>Set-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $False
```

Dieser Befehl ändert, ob die Litware-Anwendung im ContosoBatch-Konto Updates zulässt.
Der Befehl ändert weder die Standardversion noch den Anzeigenamen der Anwendung.

### Beispiel 2

Aktualisiert die Einstellungen für die angegebene Anwendung. (automatisch generiert)

<!-- Aladdin Generated Example -->
```powershell
Set-AzBatchApplication -AccountName 'ContosoBatch' -ApplicationName 'Litware' -DefaultVersion <String> -ResourceGroupName 'ContosoBatchGroup'
```

## PARAMETER

### -AccountName
Gibt den Namen des Batchkontos an, für das dieses Cmdlet eine Anwendung ändert.

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

### -AllowUpdates
Gibt an, ob Pakete innerhalb der Anwendung mit derselben Versionszeichenfolge überschrieben werden können.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationName
Gibt den Namen der Anwendung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -DefaultVersion
Gibt an, welches Paket verwendet werden soll, wenn ein Client die Anwendung anfordert, aber keine Version angibt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisplayName
Gibt den Anzeigenamen für die Anwendung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die das Batchkonto enthält.

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

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### System.Nullable'1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## AUSGABEN

### System.Void

## NOTIZEN

## VERWANDTE LINKS

[Get-AzBatchApplication](./Get-AzBatchApplication.md)

[Get-AzBatchApplicationPackage](./Get-AzBatchApplicationPackage.md)

[New-AzBatchApplication](./New-AzBatchApplication.md)

[New-AzBatchApplicationPackage](./New-AzBatchApplicationPackage.md)

[Remove-AzBatchApplication](./Remove-AzBatchApplication.md)

[Remove-AzBatchApplicationPackage](./Remove-AzBatchApplicationPackage.md)


