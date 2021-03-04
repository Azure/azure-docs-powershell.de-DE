---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 9aa895245f491e7b7ee077d083f052cd7e4e46e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935280"
---
# Set-AzVMSqlServerExtension

## SYNOPSIS
Legt die Azure SQL Server auf einem virtuellen Computer fest.

## SYNTAX

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzVMSqlServerExtension** legt die AzureSQL Server-Erweiterung auf einem virtuellen Computer fest.

## BEISPIELE

### Beispiel 1: Festlegen der Einstellungen für automatisches Patchen auf einem virtuellen Computer
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

Der erste Befehl erstellt ein Konfigurationsobjekt mithilfe des **Cmdlets New-AzVMSqlServerAutoPatchingConfig.**
Der Befehl speichert die Konfiguration in der $AutoPatchingConfig-Variable.
Der zweite Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine11 für den Dienst mit dem Namen Service02 ab, indem er das cmdlet Get-AzVM verwendet.
Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet legt die einstellungen für automatisches Patchen in $AutoPatchingConfig für den virtuellen Computer fest.
Der Befehl übergibt den virtuellen Computer an das Update-AzVM Cmdlet.

### Beispiel 2: Festlegen automatischer Sicherungseinstellungen auf einem virtuellen Computer
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

Der erste Befehl erstellt ein Konfigurationsobjekt mithilfe des **Cmdlets New-AzVMSqlServerAutoBackupConfig.**
Mit dem Befehl wird die Konfiguration in der $AutoBackupConfig gespeichert.
Der zweite Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine11 für den Dienst "Service02" ab und übergibt ihn dann an das aktuelle Cmdlet.
Das aktuelle Cmdlet legt die automatischen Sicherungseinstellungen in $AutoBackupConfig für den virtuellen Computer fest.
Der Befehl übergibt den virtuellen Computer an das Update-AzVM Cmdlet.

### Beispiel 3: Deaktivieren SQL Server Erweiterung auf einem virtuellen Computer
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

Dieser Befehl ruft einen virtuellen Computer namens VirtualMachine08 auf Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.
Der Befehl deaktiviert SQL Server Erweiterung virtueller Computer auf diesem virtuellen Computer.

### Beispiel 4: Deinstallieren SQL Server Erweiterung auf einem bestimmten virtuellen Computer
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

Dieser Befehl ruft einen virtuellen Computer namens VirtualMachine08 auf Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.
Mit dem Befehl wird eine SQL Server virtuellen Computererweiterung auf diesem virtuellen Computer deinstalliert.

## PARAMETER

### -AutoBackupSettings
Gibt den automatischen SQL Server an.
Zum Erstellen eines **AutoBackupSettings-Objekts** verwenden Sie das New-AzVMSqlServerAutoBackupConfig Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
Gibt die Einstellungen für die SQL Server an.
Zum Erstellen eines **AutoPatchingSettings-Objekts** verwenden Sie das New-AzVMSqlServerAutoPatchingConfig Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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

### -KeyVaultCredentialSettings
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Gibt den Speicherort des virtuellen Computers an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des SQL Server der Erweiterung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des virtuellen Computers an.

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

### -Version
Gibt die Version der Erweiterung SQL Server an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet die erweiterung SQL Server legt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Compute.AutoPatchingSettings

### Microsoft.Azure.Commands.Compute.AutoBackupSettings

### Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## NOTIZEN

## VERWANDTE LINKS

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[New-AzVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[New-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzVM](./Update-AzVM.md)


