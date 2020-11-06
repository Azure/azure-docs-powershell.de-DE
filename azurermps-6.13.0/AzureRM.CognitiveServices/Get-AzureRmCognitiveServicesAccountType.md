---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
ms.openlocfilehash: 05a4af3e92febcf30d44de9b114972a7c1f61d5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501173"
---
# Get-AzureRmCognitiveServicesAccountType

## Synopsis
Ruft die verfügbaren kognitiven Dienstkonto Typen ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### GetAccountTypeWithName
```
Get-AzureRmCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetAccountTypes
```
Get-AzureRmCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmCognitiveServicesAccountType** " Ruft die verfügbaren kognitiven Dienstkonto Typen unter diesem Abonnement ab.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType
```

Rufen Sie die Liste der verfügbaren Typen ab.

### Beispiel 2
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -Location westus
```

Rufen Sie die Liste der verfügbaren Typen in westus ab.

### Beispiel 3
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -TypeName Face

Face
```

Überprüfen Sie `Face` , ob es sich um einen gültigen Typnamen handelt, der Name wird zurückgegeben, wenn es sich um einen gültigen Namen handelt.

## Parameter

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### System. String []

### System. String

## Notizen

## Verwandte Links
