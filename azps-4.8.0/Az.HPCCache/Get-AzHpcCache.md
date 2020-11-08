---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009262"
---
# Get-AzHpcCache

## Synopsis
Ruft einen Cache (s) ab.

## Syntax

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzHpcCache** " Ruft einen einzelnen Cache, Cache (s) in einer bestimmten Ressourcengruppe oder eine Abonnement weite Liste von Caches ab.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### Beispiel 2
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### Beispiel 3
```powershell
PS C:\> Get-AzHPCCache
```

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
Name des bestimmten Caches.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe, unter der Sie den Cache (s) auflisten möchten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

### Microsoft. Azure. PowerShell. Cmdlets. HPCCache. Models. PSHPCCache

## Notizen

## Verwandte Links
