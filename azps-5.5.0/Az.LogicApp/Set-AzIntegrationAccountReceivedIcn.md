---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 146f1ba93a8df5f6a4396c30c9da451cdb89b9b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154785"
---
# Set-AzIntegrationAccountReceivedIcn

## SYNOPSIS
Aktualisiert das Integrationskonto, das die Interchange Control Number (ICN) in der Azure-Ressourcengruppe erhält.

## SYNTAX

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das Set-AzIntegrationAccountGeneratedIcn Cmdlet aktualisiert ein vorhandenes Integrationskonto mit der Empfangenen Interchange Control Number (ICN) und gibt ein Objekt zurück, das die Nummer des empfangenen Austauschsteuerelements für das Integrationskonto darstellt.
Verwenden Sie dieses Cmdlet, um den Nachrichtenverarbeitungsstatus eines Integrationskontos mit der Nummer des Austauschsteuerelements zu aktualisieren.
Sie können die Nummer eines Integrationskontos, für das das Austauschsteuerelement empfangen wurde, aktualisieren, indem Sie den Namen des Integrationskontos, den Namen der Ressourcengruppe, den Vertragsnamen, den Wert der Steuerelementnummer und den Status der Nachrichtenverarbeitung angeben.
Mit diesem Befehl können Sie kein neues Integrationskonto erstellen, das die Nummer des Austauschsteuerelements erhalten hat.
Um die dynamischen Parameter zu verwenden, geben Sie sie einfach in den Befehl ein, oder geben Sie ein Bindestrichzeichen(-) ein, um einen Parameternamen anzugeben, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchschreiben.
Wenn Sie einen erforderlichen Vorlagenparameter vermissen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.
Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.
Geben Sie den Parameter "-AgreementType" an, um anzugeben, ob X12- oder Edifact-Steuerelementnummern zurückgeben werden.

## BEISPIELE

### Beispiel 1
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

Mit diesem Befehl wird das Integrationskonto aktualisiert, das die X12-Austauschsteuerelementnummer für eine bestimmte Vereinbarung für ein Integrationskonto erhalten hat, und der Wert, bei dem der Status der Nachrichtenverarbeitung fehlgeschlagen ist.

### Beispiel 2
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

Mit diesem Befehl wird das Integrationskonto aktualisiert, das die Nummer des Edifact-Austauschsteuerelements für einen bestimmten Vertrag für ein Integrationskonto erhalten hat, und der Wert, bei dem der Status der Nachrichtenverarbeitung fehlgeschlagen ist.

## PARAMETERS

### -AgreementName
Der Name des Vertrags für das Integrationskonto.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AgreementType
Der Typ des Integrationskontovertrags (X12 oder Edifact).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ControlNumberValue
Der Wert für die Nummer des Integrationskontos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -IsMessageProcessingFailed
Status der Verarbeitung empfangener Nachrichten

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name des Integrationskontos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Integrationskontoressourcengruppe.

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

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)
