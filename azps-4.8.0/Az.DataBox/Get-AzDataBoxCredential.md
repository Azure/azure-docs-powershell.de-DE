---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009937"
---
# Get-AzDataBoxCredential

## Synopsis
Ruft die Datenbox-Anmeldeinformationen eines bestimmten Auftrags ab.

## Syntax

### GetByNameParameterSet (Standard)
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzDataBoxCredential** " Ruft die Anmeldeinformationen der Datenbox eines bestimmten Auftrags ab. Die internen Eigenschaften des zurückgegebenen Credentials-Objekts sind für verschiedene SKU-Typen unterschiedlich.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

Diese gibt die JobSecrets des angegebenen Auftrags

### Beispiel 2
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

Diese gibt die JobSecrets des angegebenen Auftrags

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

### -Name
DataBox-Auftrags Name

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Datenbox-Auftrags Ressourcengruppen Name

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
DataBox-Auftrags Ressourcen-ID

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

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

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Management. DataBox. Models. UnencryptedCredentials, Microsoft. Azure. Management. DataBox, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## Notizen

## Verwandte Links
