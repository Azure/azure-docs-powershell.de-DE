---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: 669a1beecaed14c0ab0705979188995daaf9d95f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845848"
---
# Remove-AzADSpCredential

## Synopsis
Entfernt eine Anmeldeinformationen von einem Dienstprinzipal.

## Syntax

### ObjectIdWithKeyIdParameterSet (Standard)
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithKeyIdParameterSet
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyIdParameterSet
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalObjectParameterSet
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Remove-AzADSpCredential-Cmdlet kann verwendet werden, um einen Anmeldeinformationsschlüssel aus einem Dienstprinzipal zu entfernen, wenn es sich um einen Kompromiss handelt oder als Teil des Rollover-Ablaufs des Anmeldeinformationsschlüssels.
Der Dienstprinzipal wird identifiziert, indem entweder die Objekt-ID oder der Dienstprinzipalname (Service Principal Name, SPN) bereitgestellt wird.
Die zu entfernenden Anmeldeinformationen werden durch die Schlüssel-ID identifiziert, wenn einzelne Anmeldeinformationen entfernt werden sollen, oder mit einem Schalter "alle", um alle dem Dienstprinzipal zugeordneten Anmeldeinformationen zu löschen.

## Beispiele

### Beispiel 1: Entfernen einer bestimmten Anmeldeinformationen von einem Dienstprinzipal

```
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

Entfernt die Anmeldeinformationen mit der Schlüssel-ID "9044423a-60a3-45ac-9ab1-09534157ebb" aus dem Dienstprinzipal mit der Objekt-ID "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82".

### Beispiel 2 – Entfernen aller Anmeldeinformationen eines Dienst Prinzipals

```
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

Entfernt alle Anmeldeinformationen aus dem Dienstprinzipal mit dem SPN " http://test123 ".

### Beispiel 3: Entfernen aller Anmeldeinformationen von einem Dienstprinzipal mithilfe von Piping

```
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

Ruft den Dienstprinzipal mit der Objekt-ID "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82" und Pipes ab, die zum Cmdlet Remove-AzADSpCredential, um alle Anmeldeinformationen aus diesem Dienstprinzipal zu entfernen.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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
Der Anzeigename des Dienst Prinzipals.

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
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
Die Schlüssel-IDs für einen Dienstprinzipal können mit dem Get-AzADSpCredential-Cmdlet abgerufen werden.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectID
Die Objekt-ID des Dienst Prinzipals, aus dem die Anmeldeinformationen entfernt werden sollen.

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.

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

### -ServicePrincipalName
Der Name (SPN) des Dienst Prinzipals, aus dem die Anmeldeinformationen entfernt werden sollen.

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalObject
Das Dienstprinzipal Objekt, aus dem die Anmeldeinformationen entfernt werden sollen.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal

### System. GUID

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[Neu – AzADSpCredential](./New-AzADSpCredential.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

