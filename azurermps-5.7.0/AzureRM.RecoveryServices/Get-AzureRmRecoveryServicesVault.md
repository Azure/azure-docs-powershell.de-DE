---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bbc059751ee4713b59f6b915efe32bdf57419be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501453"
---
# Get-AzureRmRecoveryServicesVault

## Synopsis
Ruft eine Liste der Vaults für Wiederherstellungsdienste ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmRecoveryServicesVault** " Ruft eine Liste der Wiederherstellungsdienste-Tresore im aktuellen Abonnement ab.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

Abrufen der Liste des Tresors im ausgewählten Abonnement

### Beispiel 2
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

Abrufen der Liste des Tresors in der Gruppe "Ressource" im ausgewählten Abonnement

### Beispiel 3
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

Abrufen des Tresors in der Ressourcengruppe mit dem angegebenen Namen

## Parameter

### -Name
Gibt den Namen des zu abfragenden Tresors an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Azure-Ressourcengruppe an, in der erstellt werden soll, oder aus der das angegebene Wiederherstellungsdienste-Objekt abgerufen werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
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

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. RecoveryServices. ARSVault]

## Notizen

## Verwandte Links

[Get-AzureRmRecoveryServicesVaultSettingsFile](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[Neu – AzureRmRecoveryServicesVault](./New-AzureRmRecoveryServicesVault.md)

[Remove-AzureRmRecoveryServicesVault](./Remove-AzureRmRecoveryServicesVault.md)


