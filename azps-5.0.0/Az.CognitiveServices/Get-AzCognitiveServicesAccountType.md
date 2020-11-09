---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300375"
---
# Get-AzCognitiveServicesAccountType

## Synopsis
Ruft die verfügbaren kognitiven Dienstkonto Typen ab.

## Syntax

### GetAccountTypes (Standard)
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetAccountTypeWithName
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzCognitiveServicesAccountType** " Ruft die verfügbaren kognitiven Dienstkonto Typen unter diesem Abonnement ab.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

Rufen Sie die Liste der verfügbaren Typen ab.

### Beispiel 2
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

Rufen Sie die Liste der verfügbaren Typen in westus ab.

### Beispiel 3
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

Überprüfen Sie `Face` , ob es sich um einen gültigen Typnamen handelt, der Name wird zurückgegeben, wenn es sich um einen gültigen Namen handelt.

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

### -Standort
Standort des kognitiven Dienstkontos

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeName
Name des kognitiven Dienstkonto Typs

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### System. String []

### System. String

## Notizen

## Verwandte Links
