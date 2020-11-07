---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c5ab79ca42096ab93102be1288c772cab1ac01f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663868"
---
# Unregister-AzureRmRecoveryServicesBackupContainer

## Synopsis
Hebt die Registrierung eines Windows-Servers oder eines anderen Containers aus dem Tresor auf.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Unregister-AzureRmRecoveryServicesBackupContainer** " hebt die Registrierung eines Windows-Servers oder eines anderen Sicherungs Containers aus dem Tresor auf.
Dieses Cmdlet entfernt Verweise auf einen Container aus dem Tresor.
Bevor Sie die Registrierung eines Containers aufheben können, müssen Sie alle geschützten Daten löschen, die diesem Container zugeordnet sind.

Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.

## Beispiele

### Beispiel 1: Aufheben der Registrierung eines Windows-Servers aus dem Tresor
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

Der erste Befehl ruft den Windows-Container mit dem Namen Server01.contoso.com ab, der im Tresor registriert ist, und speichert ihn dann in der $cont-Variablen.

Der zweite Befehl hebt die Registrierung des angegebenen Windows-Servers aus dem Azure Backup Vault auf.

## Parameter

### -Container
Gibt ein Backup-Containerobjekt an, um die Registrierung aufzuheben.
Verwenden Sie das Get-AzureRmRecoveryServicesBackupContainer-Cmdlet, um ein **BackupContainer** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmRecoveryServicesBackupContainer](./Get-AzureRmRecoveryServicesBackupContainer.md)


