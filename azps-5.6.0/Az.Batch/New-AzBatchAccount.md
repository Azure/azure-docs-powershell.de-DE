---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: d665e6f373a058761fb3e7e170b1d1434ac7786f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949616"
---
# New-AzBatchAccount

## SYNOPSIS
Erstellt ein Batchkonto.

## SYNTAX

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-PublicNetworkAccess <PublicNetworkAccessType>]
 [-IdentityType <ResourceIdentityType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzBatchAccount** erstellt ein Azure Batch-Konto für die angegebene Ressourcengruppe und den angegebenen Speicherort.

## BEISPIELE

### Beispiel 1: Erstellen eines Batchkontos
```powershell
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

Mit diesem Befehl wird ein Batchkonto mit dem Namen "pfuller" mithilfe der Ressourcengruppe "ResourceGroup03" am Standort "USA, Westen" erstellt.

### Beispiel 2

Erstellt ein Batchkonto. (automatisch generiert)

<!-- Aladdin Generated Example -->
```powershell
New-AzBatchAccount -AccountName 'pfuller' -AutoStorageAccountId <String> -Location 'WestUS' -ResourceGroupName 'ResourceGroup03'
```

## PARAMETER

### -AccountName
Gibt den Namen des Batchkontos an, das von diesem Cmdlet erstellt wird.
Batchkontonamen müssen zwischen 3 und 24 Zeichen lang sein und nur Zahlen und Kleinbuchstaben enthalten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoStorageAccountId
Gibt die Ressourcen-ID des Speicherkontos an, das für den automatischen Speicher verwendet werden soll.

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

### -IdentityType
Die dem BatchAccount zugeordnete Identität

```yaml
Type: Microsoft.Azure.Management.Batch.Models.ResourceIdentityType
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultId
Die Ressourcen-ID des Azure-Schlüsseltresors, der dem Batchkonto zugeordnet ist.

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

### -KeyVaultUrl
Die URL des Azure-Schlüsseltresors, der dem Batchkonto zugeordnet ist.

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

### -Location
Gibt den Bereich an, in dem dieses Cmdlet das Konto erstellt.
Weitere Informationen finden Sie unter [Azure-Regionen](https://azure.microsoft.com/en-us/regions).

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

### -PoolAllocationMode
Der Zuweisungsmodus zum Erstellen von Pools im Batchkonto.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode]
Parameter Sets: (All)
Aliases:
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicNetworkAccess
Der Zugriffstyp des öffentlichen Netzwerks

```yaml
Type: Microsoft.Azure.Management.Batch.Models.PublicNetworkAccessType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet das Konto erstellt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle. Beispiel: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### System.Nullable'1[[Microsoft.Azure.Management.Batch. Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=9.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## NOTIZEN

## VERWANDTE LINKS

[Get-AzBatchAccount](./Get-AzBatchAccount.md)

[Remove-AzBatchAccount](./Remove-AzBatchAccount.md)

[Set-AzBatchAccount](./Set-AzBatchAccount.md)

[Azure Batch-Cmdlets](/powershell/module/Az.Batch/)
