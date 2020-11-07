---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 41209f3790b7520c50e3105f9ca7c4a5a0e79dfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665114"
---
# Unregister-AzureRmBackupContainer

## Synopsis
Hebt die Registrierung eines Containers aus einem sicherungstresor auf.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Unregister-AzureRmBackupContainer** " hebt die Registrierung des Windows Server-oder Azure Virtual Machine aus einem Azure Backup Vault auf.
Dieses Cmdlet entfernt Verweise auf einen Container aus dem Sicherungsspeicher.
Bevor Sie die Registrierung eines Containers aufheben können, müssen Sie alle geschützten Daten löschen, die diesem Container zugeordnet sind.

## Beispiele

### Beispiel 1: Aufheben der Registrierung eines Windows-Servers
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.
Der Befehl speichert das Objekt in der $Vault Variablen.

Der zweite Befehl ruft mithilfe des Get-AzureRmBackupContainer-Cmdlets einen Container ab, der den angegebenen Namen im Tresor in $Vault aufweist.
Der Befehl speichert das Objekt in der $Container Variablen.

Der endgültige Befehl hebt die Registrierung des angegebenen Windows-Servers aus dem Azure Backup Vault auf.

### Beispiel 2: Aufheben der Registrierung eines Windows-Servers ohne Bestätigung
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

Dieser Befehl hebt die Registrierung des angegebenen Windows-Servers aus dem Azure Backup Vault auf, genau wie im ersten Beispiel.
Mit diesem Befehl wird der *Force* -Parameter angegeben.
Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.

## Parameter

### -Container
Gibt den Windows-Server oder Azure Virtual Machine an, die von diesem Cmdlet aufgehoben werden.
Verwenden Sie zum Abrufen eines **AzureRmBackupContainer** das Get-AzureRmBackupContainer-Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.
Dieser Parameter ist nur für **AzureBackupContainer** -Objekte des Typs Windows relevant.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

### AzureBackupContainer

## Ausgaben

### AzureBackupJob
Dieses Cmdlet gibt $NULL zurück, wenn es sich bei dem Containertyp um Windows Server handelt.

## Notizen
* Keine

## Verwandte Links

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Registrieren-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


