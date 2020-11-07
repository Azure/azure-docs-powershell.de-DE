---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: 87d7ff04b62bcee2e735dacbbdd9ddb3ab04d425
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844255"
---
# Set-AzVMAEMExtension

## Synopsis
Ermöglicht die Unterstützung für die Überwachung von SAP-Systemen.

## Syntax

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzVMAEMExtension** " aktualisiert die Konfiguration einer virtuellen Maschine, um die Unterstützung für die Überwachung von SAP-Systemen zu aktivieren oder zu aktualisieren, die auf dem virtuellen Computer installiert sind.
Das Cmdlet installiert die Erweiterung Azure Enhanced Monitoring (AEM), die die Leistungsdaten erfasst und für das SAP-System auffindbar macht.

## Beispiele

### Beispiel 1: Verwenden der AEM-Erweiterung
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

Dieser Befehl konfiguriert den virtuellen Computer mit dem Namen "Contoso-Server", um die AEM-Erweiterung zu verwenden.
Der Befehl gibt das Speicherkonto mit dem Namen "stdstorage" an.

## Parameter

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

### -DisableWAD
Gibt an, dass dieses Cmdlet keine Azure-Diagnose für den virtuellen Computer aktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWAD
Wenn dieser Parameter bereitgestellt wird, aktiviert der Unifiedgroup Windows Azure-Diagnose für diesen virtuellen Computer.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSType
Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.
Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.
Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des virtuellen Computers an, die von diesem Cmdlet geändert wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipStorage
Gibt an, dass dieses Cmdlet die Konfiguration des Speichers überspringt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Gibt den Namen einer virtuellen Maschine an.
Mit diesem Cmdlet wird die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt, hinzugefügt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WADStorageAccountName
Gibt den Namen des speicherkontos an, das dieses Cmdlet zum Konfigurieren der LinuxDiagnostics-oder IaaSDiagnostics-Erweiterung verwendet.
Wenn auf dem virtuellen Computer kein Standardspeicher Konto verwendet wird, müssen Sie einen Wert für diesen Parameter angeben.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse

## Notizen

## Verwandte Links

[Get-AzVMAEMExtension](./Get-AzVMAEMExtension.md)

[Remove-AzVMAEMExtension](./Remove-AzVMAEMExtension.md)

[Test-AzVMAEMExtension](./Test-AzVMAEMExtension.md)


