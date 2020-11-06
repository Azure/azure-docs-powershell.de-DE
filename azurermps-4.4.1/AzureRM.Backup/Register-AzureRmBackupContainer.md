---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: fe1e1075e14e3752024edff1b68db88419d5bcd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497929"
---
# Register-AzureRmBackupContainer

## Synopsis
Registriert den Container mit einem Sicherungsspeicher.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### V1VM
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### V2VM
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Register-AzureRmBackupContainer** " wird der Container mit einem Azure Backup Vault registriert.
Wenn Sie die Sicherung mithilfe der Azure-Sicherung konfigurieren möchten, registrieren Sie zuerst Ihren Server oder virtuellen Computer mit einem Sicherungsspeicher.
Mit diesem Cmdlet wird eine Infrastruktur als IaaS-virtueller Computer mit dem angegebenen Tresor registriert.
Der Vorgang registrieren ordnet den Azure Virtual Machine dem Sicherungsspeicher zu und verfolgt den virtuellen Computer über den Lebenszyklus der Sicherung.

## Beispiele

### Beispiel 1: Registrieren eines virtuellen Computers in einem Sicherungsspeicher
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.
Der Befehl speichert den Tresor in der $Vault Variablen.

Der zweite Befehl registriert den virtuellen Computer mit dem Namen Contoso03Vm mit dem Tresor in $Vault.
Dieser virtuelle Computer gehört zum Dienst mit dem Namen ContosoService27.

## Parameter

### -Name
Gibt den Namen des virtuellen Computers an, der von diesem Cmdlet registriert wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe für den virtuellen Computer an.

```yaml
Type: System.String
Parameter Sets: V2VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Gibt den Dienstnamen des virtuellen Computers an, den dieses Cmdlet registriert.

In der Regel weist ein Cloud-Dienstname ein Suffix. cloudapp.net auf.
Schließen Sie das Suffix nicht ein, wenn Sie diesen Parameter angeben.

Verwenden Sie das Get-AzureRMVM-Cmdlet, um Informationen zu einem virtuellen Computer zu erhalten.
Der Dienstname ist die **deploymentname** -Eigenschaft des Virtual Machine-Objekts.

```yaml
Type: System.String
Parameter Sets: V1VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vault
Gibt den sicherungstresor an, zu dem dieses Cmdlet den virtuellen Computer registriert.
Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.

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

### AzureRmBackupVault

## Ausgaben

### AzureRmBackupJob

## Notizen

## Verwandte Links

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


