---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 83212224ba14e0a079db936d058522d4759430fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923464"
---
# Get-AzADSpCredential

## SYNOPSIS
Ruft eine Liste der Anmeldeinformationen ab, die einem Dienstprinzipal zugeordnet sind.

## SYNTAX

### ObjectIdParameterSet (Standard)
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNObjectParameterSet
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das Get-AzADSpCredential-Cmdlet kann verwendet werden, um eine Liste der Anmeldeinformationen abzurufen, die einem Dienstprinzipal zugeordnet sind.
Mit diesem Befehl werden alle Anmeldeinformationseigenschaften (aber nicht der Anmeldeinformationswert) abgerufen, die dem Dienstprinzipal zugeordnet sind.

## BEISPIELE

### Beispiel 1 : Listenanmeldeinformationen nach SPN

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

Gibt eine Liste der Anmeldeinformationen zurück, die dem Dienstprinzipal mit SPN ' ' zugeordnet http://test12345 sind.

### Beispiel 2– Listenanmeldeinformationen nach Objekt-ID

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

Gibt eine Liste der Anmeldeinformationen zurück, die dem Dienstprinzipal mit der Objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" zugeordnet sind.

### Beispiel 3 : Listenanmeldeinformationen durch Piping

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

Ruft den Dienstprinzipal mit der Objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" ab und gibt ihn an das Get-AzADSpCredential-Cmdlet weiter, um alle Anmeldeinformationen für diesen Dienstprinzipal auflisten.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -DisplayName
Der Anzeigename des Dienstprinzipals

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Die Objekt-ID des Dienstprinzipals zum Abrufen von Anmeldeinformationen.

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Der Name (SPN) des Dienstprinzipals, aus dem Anmeldeinformationen abgerufen werden.

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalObject
Das Dienstprinzipalobjekt zum Abrufen der Anmeldeinformationen.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### Microsoft.Azure.Commands.ActiveDirectory.PSDServicePrincipal

## AUSGABEN

### Microsoft.Azure.Commands.ActiveDirectory.PSDCredential

## NOTIZEN

## VERWANDTE LINKS

[New-AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

