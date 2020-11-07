---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: bf4ba77a7162faaf593e11b68a82fe5a6e55df1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662696"
---
# Get-AzureRmBackupJobDetails

## Synopsis
Ruft die Details eines Backup-Auftrags ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### JobsFiltersSet (Standard)
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### IdFiltersSet
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmBackupJobDetails** " Ruft die Details eines Azure Backup-Auftrags ab.
Sie können dieses Cmdlet verwenden, um Informationen zu einem fehlerhaften Job zu sammeln.

## Beispiele

### Beispiel 1: Anzeigen der Details eines fehlerhaften Auftrags
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

Der erste Befehl ruft den Tresor mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** ab.
Der Befehl speichert das Objekt in der $Vault Variablen.
Der zweite Befehl ruft fehlerhafte Aufträge aus dem Tresor in $Vault ab und speichert Sie dann in der $Jobs-Arrayvariablen.
Der dritte Job ruft Details für den ersten Job in der $Jobs-Variablen ab und speichert diese Details dann in der $JobDetails-Variablen.
Der endgültige Befehl zeigt die **ErrorDetails** -Eigenschaft von $JobDetails mit der standardmäßigen Punktsyntax an.

### Beispiel 2: Anzeigen der empfohlenen Aktion für einen fehlerhaften Auftrag
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

Dieser Befehl zeigt die empfohlene Aktion aus der $JobDetails Variablen an, die im ersten Beispiel erstellt wurde.

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

### -Job
Gibt einen Auftrag an, für den dieses Cmdlet Details erhält.
Verwenden Sie das Get-AzureRmBackupJob-Cmdlet, um ein **AzureRmBackupJob** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Gibt die ID eines Auftrags an, für den dieses Cmdlet Details erhält.
Die ID ist die **InstanceId** -Eigenschaft eines **AzureRmBackupJob** -Objekts.
Verwenden Sie Get-AzureRmBackupJob, um ein **AzureRmBackupJob** -Objekt zu erhalten.

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Gibt den sicherungstresor an, für den dieses Cmdlet Auftragsdetails erhält.
Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob
Parameter: Job (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJobDetails

## Notizen

## Verwandte Links

[Get-AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


