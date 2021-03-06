---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 34dcb85de9520882b9202edd38ae2e44d1bcafee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664699"
---
# Get-AzureRmAutomationDscOnboardingMetaconfig

## Synopsis
Erstellt Meta-Configuration. MOF-Dateien.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmAutomationDscOnboardingMetaconfig** " erstellt APS-metakonfigurations-(Managed Object Format)-Dateien (MOF).
Mit diesem Cmdlet wird für jeden von Ihnen angegebenen Computernamen eine MOF-Datei erstellt.
Das Cmdlet erstellt einen Ordner für die MOF-Dateien.
Sie können das Set-DscLocalConfigurationManager-Cmdlet für diesen Ordner ausführen, um diese Computer als DSC-Knoten in ein Azure Automation-Konto einzuführen.

## Beispiele

### Beispiel 1: Onboard-Server für Automatisierungs-DSC
```
PS C:\>Get-AzureRmAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

Der erste Befehl erstellt DSC-metakonfigurations Dateien für zwei Server für das Automatisierungs Konto mit dem Namen Contoso17.
Der Befehl speichert diese Dateien auf einem Desktop.

Der zweite Befehl verwendet das Cmdlet " **DscLocalConfigurationManager** ", um die Meta-Konfiguration auf die angegebenen Computer anzuwenden, um Sie als DSC-Knoten an Bord zu übernehmen.

## Parameter

### -AutomationAccountName
Gibt den Namen eines Automatisierungs Kontos an.
Sie können an Bord der Computer, die der Parameter *Computername* für das Konto angibt, das dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Computername
Gibt ein Array von Namen von Computern an, für die dieses Cmdlet MOF-Dateien generiert.
Wenn Sie diesen Parameter nicht angeben, generiert das Cmdlet eine MOF-Datei für den aktuellen Computer (localhost).

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne dass Sie zur Bestätigung aufgefordert werden, und um vorhandene MOF-Dateien mit demselben Namen zu ersetzen.

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

### -OutputFolder
Gibt den Namen eines Ordners an, in dem das Cmdlet MOF-Dateien speichert.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.
Dieses Cmdlet erstellt MOF-Dateien für Onboard-Computer in der Ressourcengruppe, die dieser Parameter angibt.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. DscOnboardingMetaconfig

## Notizen

## Verwandte Links

