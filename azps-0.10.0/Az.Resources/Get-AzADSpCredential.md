---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 40543468145c7fcfaf49fcfc7cad1cbf70938adf
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843471"
---
# Get-AzADSpCredential

## Synopsis
Ruft eine Liste mit Anmeldeinformationen ab, die einem Dienstprinzipal zugeordnet sind.

## Syntax

### ObjectIdParameterSet (Standard)
```
Get-AzADSpCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
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
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mithilfe des Get-AzADSpCredential-Cmdlets können Sie eine Liste mit Anmeldeinformationen abrufen, die einem Dienstprinzipal zugeordnet sind.
Dieser Befehl ruft alle Anmelde Informationseigenschaften (aber nicht den Anmelde Informationswert) ab, die dem Dienstprinzipal zugeordnet sind.

## Beispiele

### Beispiel 1 – Listen Anmeldeinformationen nach SPN

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

Gibt eine Liste der Anmeldeinformationen zurück, die dem Dienstprinzipal mit SPN ' ' zugeordnet sind http://test12345 .

### Beispiel 2: Auflisten von Anmeldeinformationen nach Objekt-ID

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

Gibt eine Liste der Anmeldeinformationen zurück, die dem Dienstprinzipal mit der Objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" zugeordnet sind.

### Beispiel für 3-Listen-Anmeldeinformationen durch Piping

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

Ruft den Dienstprinzipal mit der Objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" ab und leitet ihn an das Get-AzADSpCredential-Cmdlet weiter, um alle Anmeldeinformationen für diesen Dienstprinzipal aufzulisten.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Der Anzeigename des Dienst Prinzipals

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

### -ObjectID
Die Objekt-ID des Dienst Prinzipals, von dem die Anmeldeinformationen abgerufen werden sollen.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Der Name (SPN) des Dienst Prinzipals, aus dem Anmeldeinformationen abgerufen werden sollen.

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
Das Dienstprinzipal Objekt, aus dem die Anmeldeinformationen abgerufen werden sollen.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. GUID

### System. String

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal
Parameter: ServicePrincipalObject (ByValue)

## Ausgaben

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential

## Notizen

## Verwandte Links

[Neu – AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

