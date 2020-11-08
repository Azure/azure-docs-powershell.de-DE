---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177933"
---
# Get-AzManagedHsm

## Synopsis
Abrufen verwalteter HSMs.

## Syntax

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzManagedHsm** " Ruft Informationen zur verwalteten HSMs in einem Abonnement ab. Sie können alle verwalteten HSMs-Instanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten verwalteten HSM filtern.
Beachten Sie, dass die Angabe der Ressourcengruppe zwar für dieses Cmdlet optional ist, wenn Sie ein einzelnes verwaltetes HSM erhalten, Sie dies jedoch für eine bessere Leistung tun sollten.

## Beispiele

### Beispiel 1: Abrufen aller verwalteten HSMs in Ihrem aktuellen Abonnement
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Dieser Befehl ruft alle verwalteten HSMs in Ihrem aktuellen Abonnement ab.

### Beispiel 2: Abrufen eines bestimmten verwalteten HSM
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Dieser Befehl ruft das verwaltete HSM mit dem Namen myhsm in Ihrem aktuellen Abonnement ab.

### Beispiel 3: Abrufen von verwalteten HSMs in einer Ressourcengruppe
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Dieser Befehl ruft alle verwalteten HSMs in der Ressourcengruppe mit dem Namen myrg1 ab.

### Beispiel 4: Abrufen verwalteter HSMs mithilfe von Filtern
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Dieser Befehl ruft alle verwalteten HSMs im Abonnement ab, die mit "myhsm" beginnen.

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
HSM-Name. Cmdlet erstellt den FQDN eines HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die dem verwalteten HSM zugeordnet ist, das abgefragt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Gibt den Schlüssel und optionalen Wert des angegebenen Tags an, um die Liste der verwalteten HSMs zu filtern.

```yaml
Type: System.Collections.Hashtable
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

### System. Collections. Hashtable

## Ausgaben

### Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem

## Notizen

## Verwandte Links

[Neu – AzManagedHsm](./New-AzManagedHsm.md)

[Remove-AzManagedHsm](./Remove-AzManagedHsm.md)

[Update-AzManagedHsm](./Update-AzManagedHsm.md)