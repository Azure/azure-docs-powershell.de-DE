---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 1795216cbc18da2d503a1e0056d614337cd12785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398239"
---
# Set-AzVMSqlServerExtension

## SYNOPSIS
Legt die Azure SQL Server erweiterung auf einem virtuellen Computer fest.

## SYNTAX

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzVMSqlServerExtension"** legt die AzureSQL -Servererweiterung auf einem virtuellen Computer fest.

## BEISPIELE

### Beispiel 1: Festlegen der Einstellungen für automatisches Patchen auf einem virtuellen Computer
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

Der erste Befehl erstellt ein Konfigurationsobjekt mithilfe des **Cmdlets "New-AzureVMSqlServerAutoPatchingConfig".**
Der Befehl speichert die Konfiguration in der $AutoPatchingConfig Variable.

Der zweite Befehl ruft den virtuellen Computer mit dem Namen "VirtualMachine11" für den Dienst "Service02" mit dem cmdlet Get-AzVM ab.
Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.

Das aktuelle Cmdlet legt die Einstellungen für automatisches Patchen in $AutoPatchingConfig für den virtuellen Computer fest.
Der Befehl übergibt den virtuellen Computer an das Update-AzVM Cmdlet.

### Beispiel 2: Festlegen von Einstellungen für die automatische Sicherung auf einem virtuellen Computer
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

Der erste Befehl erstellt ein Konfigurationsobjekt mithilfe des **Cmdlets "New-AzureVMSqlServerAutoBackupConfig".**
Der Befehl speichert die Konfiguration in der $AutoBackupConfig Variable.

Der zweite Befehl ruft den virtuellen Computer namens "VirtualMachine11" für den Dienst "Service02" ab und übergibt ihn dann an das aktuelle Cmdlet.

Das aktuelle Cmdlet legt die Einstellungen für die automatische Sicherung in $AutoBackupConfig für den virtuellen Computer fest.
Der Befehl übergibt den virtuellen Computer an das Update-AzVM Cmdlet.

### Beispiel 3: Deaktivieren SQL Server Erweiterung auf einem virtuellen Computer
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

Dieser Befehl ruft einen virtuellen Computer namens "VirtualMachine08" auf Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.
Der Befehl deaktiviert die SQL Server des virtuellen Computers auf diesem virtuellen Computer.

### Beispiel 4: Deinstallieren SQL Server Erweiterung auf einem bestimmten virtuellen Computer
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

Dieser Befehl ruft einen virtuellen Computer namens "VirtualMachine08" auf Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.
Mit dem Befehl wird eine SQL Server virtuellen Computererweiterung auf diesem virtuellen Computer deinstalliert.

## PARAMETERS

### -AutoBackupSettings
Gibt die einstellungen für die automatische SQL Server an.
Verwenden Sie zum **Erstellen eines AutoBackupSettings-Objekts** das New-AzureVMSqlServerAutoBackupConfig Cmdlet.

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
Gibt die Einstellungen für das automatische SQL Server patchen an.
Verwenden Sie zum **Erstellen eines AutoPatchingSettings-Objekts** das New-AzureVMSqlServerAutoPatchingConfig Cmdlet.

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -KeyVaultCredentialSettings
```yaml
Type: KeyVaultCredentialSettings
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
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Namens der SQL Server Erweiterung an.

```yaml
Type: String
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
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet die SQL Server legt.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[New-AzureVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[New-AzureVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzVM](./Update-AzVM.md)


