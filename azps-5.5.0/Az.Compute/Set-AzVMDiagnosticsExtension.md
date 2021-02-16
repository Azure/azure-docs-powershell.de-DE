---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 5705d899f06d4a834b8864ec2a66c268e1c99c84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166404"
---
# Set-AzVMDiagnosticsExtension

## SYNOPSIS
Konfiguriert die Azure-Diagnoseerweiterung auf einem virtuellen Computer.

## SYNTAX

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzVMDiagnosticsExtension** konfiguriert die Azure-Diagnoseerweiterung auf einem virtuellen Computer.

## BEISPIELE

### Beispiel 1: Aktivieren der Diagnose mithilfe eines Speicherkontos, das in einer Diagnosekonfigurationsdatei angegeben ist
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

Dieser Befehl verwendet eine Diagnosekonfigurationsdatei, um die Diagnose zu aktivieren.
Die Dateidateidiagnostics_publicconfig.xml enthält die öffentliche XML-Konfiguration für die Diagnoseerweiterung, einschließlich des Namens des Speicherkontos, an das Diagnosedaten gesendet werden.
Das Speicherkonto für die Diagnose muss im selben Abonnement wie der virtuelle Computer enthalten sein.

### Beispiel 2: Aktivieren der Diagnose mithilfe eines Speicherkontonamens
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

Dieser Befehl verwendet den Namen des Speicherkontos, um die Diagnose zu aktivieren.
Wenn in der Diagnosekonfiguration kein Speicherkontoname angegeben wird oder Sie den in der Konfigurationsdatei angegebenen Namen des Diagnosespeicherkontos außer Kraft setzen möchten, verwenden Sie den *Parameter "StorageAccountName".*
Das Speicherkonto für die Diagnose muss im selben Abonnement wie der virtuelle Computer enthalten sein.

### Beispiel 3: Aktivieren der Diagnose mithilfe von Name und Schlüssel des Speicherkontos
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

Dieser Befehl verwendet den Namen und Schlüssel des Speicherkontos, um die Diagnose zu aktivieren.
Wenn das Speicherkonto für die Diagnose in einem anderen Abonnement als der virtuelle Computer enthalten ist, aktivieren Sie das Senden von Diagnosedaten an dieses Speicherkonto, indem Sie dessen Namen und Schlüssel explizit angeben.

## PARAMETERS

### -AutoUpgradeMinorVersion
Gibt an, ob dieses Cmdlet es dem Azure-Gast-Agent erlaubt, die Erweiterung automatisch auf eine neuere Nebenversion zu aktualisieren.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -DiagnosticsConfigurationPath
Gibt den Pfad der Konfigurationsdatei an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Gibt den Speicherort des virtuellen Computers an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen einer Erweiterung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoWait
Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet. Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des virtuellen Computers an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountEndpoint
Gibt den Endpunkt des Speicherkontos an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountKey
Gibt den Speicherkontoschlüssel an.

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

### -StorageAccountName
Gibt den Namen des Speicherkontos an.

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

### -StorageContext
Gibt den Azure -Speicherkontext an.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.
Führen Sie zum Abrufen der Version das Get-AzVMExtensionImage cmdlet mit dem Wert "Microsoft.Compute" für den *Parameter "PublisherName"* und "VMAccessAgent" für den Parameter *"Type"* aus.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet ausgeführt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

### System.Boolean

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzVMDiagnosticsExtension](./Get-AzVMDiagnosticsExtension.md)

[Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md)

[Remove-AzVMDiagnosticsExtension](./Remove-AzVMDiagnosticsExtension.md)


