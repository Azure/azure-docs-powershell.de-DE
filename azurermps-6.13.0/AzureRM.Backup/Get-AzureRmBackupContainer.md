---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: e20276d8a2dfec8ffb39665e5122cfe4be74dc42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662698"
---
# Get-AzureRmBackupContainer

## Synopsis
Ruft Sicherungs Container ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmBackupContainer** " ruft Azure-Sicherungs Container ab.
Ein **AzureBackupContainer** kapselt Datenquellen, geschützte Elemente und Wiederherstellungspunkte.
Eine **AzureBackupContainer** kann eine der folgenden Optionen sein: 
- Ein Windows Server-Computer
- Einen scdpm-Server (System Center Data Protection Manager) 
- Eine Azure Infrastructure as a Service (IaaS) Virtual Machine, bevor Backup eine Datenquelle oder ein Element sichern kann, müssen Sie den Container registrieren, in dem der Azure-Sicherungsdienst enthalten ist.
Der Container muss authentifiziert werden, um Sicherungsdaten an den sicherungstresor zu senden.
Bei Windows Server-Computern und scdpm-Servern wird die Registrierung mit dem vollqualifizierten Domänennamen des Servers abgehalten.

## Beispiele

### Beispiel 1: Anzeigen aller für einen Tresor registrierten Server
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

Der erste Befehl ruft den Tresor mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** ab.
Der Befehl speichert das Objekt in der $Vault Variablen.
Der zweite Befehl ruft alle Container des Typs Windows aus dem Tresor in $Vault ab.

### Beispiel 2: Abrufen eines bestimmten Containers
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

Dieser Befehl ruft den Container mit dem Namen DPMSERVER ab. CONTOSO.com.
Der Befehl gibt den Tresor in $Vault und den Typ des Containers an.

### Beispiel 3: Anzeigen aller registrierten Azure Virtual Machines
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

Dieser Befehl ruft die registrierten virtuellen Computer aus dem Tresor in $Vault ab.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -ManagedResourceGroupName
Gibt den Namen der Ressourcengruppe an, die dem Container zugeordnet ist.
Dieser Name ist derselbe Wert, den Sie für den *Service* Name-oder *ResourceGroupName* -Parameter des Register-AzureRmBackupContainer-Cmdlets angegeben haben.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Containers an, den dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Gibt den aktuellen Status der Container an, die dieses Cmdlet erhält.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- NotRegistered 
- Registriert 
- Registrieren

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Typ
Gibt den Typ der Container an, die dieses Cmdlet erhält.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Gibt einen sicherungstresor an, aus dem dieses Cmdlet Container erhält.
Verwenden Sie zum Abrufen eines **AzureRmBackupVault** das Get-AzureRmBackupVault-Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault
Parameter: Vault (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupContainer

## Notizen
* Keine

## Verwandte Links

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Registrieren-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)

[Registrierung aufheben-AzureRmBackupContainer](./Unregister-AzureRmBackupContainer.md)


