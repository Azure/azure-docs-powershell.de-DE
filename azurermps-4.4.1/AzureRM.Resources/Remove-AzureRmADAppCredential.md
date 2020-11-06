---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: a5e99f045701a373e14990c25627696d40a04a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500721"
---
# Remove-AzureRmADAppCredential

## Synopsis
Entfernt Anmeldeinformationen aus einer Anwendung.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ApplicationObjectIdWithKeyIdParameterSet (Standard)
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectIdWithAllParameterSet
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationIdWithKeyIdParameterSet
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationIdWithAllParameterSet
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Remove-AzureRmADAppCredential-Cmdlet kann verwendet werden, um einen Anmeldeinformationsschlüssel aus einer Anwendung im Fall einer Gefährdung oder als Teil des Rollover-Ablaufs von Anmeldeinformationen zu entfernen.
Die Anwendung wird identifiziert, indem entweder die Objekt-ID oder die Anwendungs-ID angegeben wird.
Die zu entfernenden Anmeldeinformationen werden durch die Schlüssel-ID identifiziert, wenn einzelne Anmeldeinformationen entfernt werden sollen, oder mit einem Schalter "alle", um alle Anmeldeinformationen zu löschen, die der Anwendung zugeordnet sind.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

Mit diesem Befehl wird ein Anmeldeinformationsschlüssel aus einer Anwendung entfernt.
In diesem Beispiel wird der Schlüssel mit der ID "9044423a-60a3-45ac-9ab1-09534157ebb" aus der Anwendung entfernt.

### --------------------------Beispiel 2--------------------------
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

Mit diesem Befehl wird ein Anmeldeinformationsschlüssel aus einer Anwendung entfernt.
In diesem Beispiel werden alle Anmeldeinformationen aus der Anwendung entfernt, die dem ApplicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58" zugeordnet ist.

## Parameter

### – Alle
Wechseln Sie, um alle Anmeldeinformationen zu entfernen, die der Anwendung zugeordnet sind.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationId
Die ID der Anwendung, aus der die Anmeldeinformationen entfernt werden sollen.

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Wechseln Sie, um die Anmeldeinformationen ohne Bestätigung zu löschen.

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

### -KeyId
Gibt den Anmeldeinformationsschlüssel an, der entfernt werden soll.
Die Schlüssel-IDs für die Anwendung können mit dem Get-AzureRmADAppCredential-Cmdlet abgerufen werden.

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectID
Die Objekt-ID der Anwendung, aus der die Anmeldeinformationen entfernt werden sollen.

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
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

## Notizen

## Verwandte Links

[Get-AzureRmADAppCredential](./Get-AzureRmADAppCredential.md)

[Neu – AzureRmADAppCredential](./New-AzureRmADAppCredential.md)

[Get-AzureRmADApplication](./Get-AzureRmADApplication.md)
