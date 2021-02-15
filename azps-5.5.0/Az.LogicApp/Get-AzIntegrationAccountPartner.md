---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: cf6d2f4da1803e5c9403803ea7231b55c13d7243
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159524"
---
# Get-AzIntegrationAccountPartner

## SYNOPSIS
Ruft Integrationskontopartner ab.

## SYNTAX

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzIntegrationAccountPartner"** ruft Integrationskontopartner aus einer Ressourcengruppe ab.
Geben Sie den Namen des Integrationskontos, den Namen der Ressourcengruppe und den Namen des Partners an.
Dieses Modul unterstützt dynamische Parameter.
Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.
Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.
Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.

## BEISPIELE

### Beispiel 1: Partner für ein Integrationskonto erhalten
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

Dieser Befehl ruft den Integrationskontopartner namens "IntegrationAccountPartner22" ab.

### Beispiel 2: Erhalten eines Integrationskontopartners mithilfe eines Integrationskontonamens
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

Dieser Befehl ruft die Integrationskontopartner für das Integrationskonto namens "IntegrationAccount31" ab.

## PARAMETERS

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

### -Name
Gibt den Namen eines Integrationskontos an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerName
Gibt den Namen des Integrationskontopartners an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzIntegrationAccountPartner](./New-AzIntegrationAccountPartner.md)

[Remove-AzIntegrationAccountPartner](./Remove-AzIntegrationAccountPartner.md)

[Set-AzIntegrationAccountPartner](./Set-AzIntegrationAccountPartner.md)


