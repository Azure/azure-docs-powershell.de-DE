---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: fa02d7ffc23706564b8b6fe118f12525829b27f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009782"
---
# <span data-ttu-id="65900-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="65900-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="65900-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65900-102">SYNOPSIS</span></span>
<span data-ttu-id="65900-103">Aktualisiert die in der Azure-Ressourcengruppe generierte ICN (Interchange Control Number) des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="65900-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="65900-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65900-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65900-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65900-105">DESCRIPTION</span></span>
<span data-ttu-id="65900-106">Das Set-AzIntegrationAccountGeneratedIcn-Cmdlet aktualisiert eine vorhandene Integration-Konto generierte Interchange Control Number (ICN) und gibt ein Objekt zurück, das die vom Integrations Konto generierte Austauschkontrollnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="65900-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="65900-107">Verwenden Sie dieses Cmdlet, um eine vom Integrations Konto generierte Austauschkontrollnummer zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="65900-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="65900-108">Sie können eine vom Integrations Konto generierte Austauschkontrollnummer aktualisieren, indem Sie den Namen des Integrations Kontos, den Namen der Ressourcengruppe und den Namen der Vereinbarung angeben.</span><span class="sxs-lookup"><span data-stu-id="65900-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="65900-109">Mit diesem Befehl können Sie keine neue Integrations Konto generierte Austauschkontrollnummer erstellen.</span><span class="sxs-lookup"><span data-stu-id="65900-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="65900-110">Wenn Sie die dynamischen Parameter verwenden möchten, geben Sie Sie einfach in den Befehl ein, oder geben Sie einen Bindestrich (-) ein, um einen Parameternamen anzugeben, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="65900-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="65900-111">Wenn Sie einen erforderlichen Vorlagenparameter verpassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="65900-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="65900-112">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="65900-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="65900-113">Geben Sie den Parameter "-agreementtype" an, um anzugeben, ob X12-oder EDIFACT-Steuernummern zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="65900-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="65900-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65900-114">EXAMPLES</span></span>

### <span data-ttu-id="65900-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65900-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="65900-116">Dieser Befehl ruft die vom Integration Account generierte X12 Interchange Control-Nummer für eine bestimmte Integration-Kontovereinbarung ab, erhöht den Wert um 100 und schreibt dann den aktualisierten Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="65900-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="65900-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="65900-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="65900-118">Dieser Befehl ruft die EdifactIntegrationAccountAgreement-Austauschkontrollnummer des Integrations Kontos für eine bestimmte Integrations Kontovereinbarung ab, erhöht den Wert um 100 und schreibt dann den aktualisierten Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="65900-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="65900-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="65900-119">PARAMETERS</span></span>

### <span data-ttu-id="65900-120">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="65900-120">-AgreementName</span></span>
<span data-ttu-id="65900-121">Der Name des Integrations kontovertrags.</span><span class="sxs-lookup"><span data-stu-id="65900-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="65900-122">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="65900-122">-AgreementType</span></span>
<span data-ttu-id="65900-123">Der Typ des Integrations kontovertrags.</span><span class="sxs-lookup"><span data-stu-id="65900-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="65900-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="65900-124">-ControlNumber</span></span>
<span data-ttu-id="65900-125">Der generierte Steuerelement-Number New-Wert.</span><span class="sxs-lookup"><span data-stu-id="65900-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="65900-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65900-126">-DefaultProfile</span></span>
<span data-ttu-id="65900-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="65900-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65900-128">-Name</span><span class="sxs-lookup"><span data-stu-id="65900-128">-Name</span></span>
<span data-ttu-id="65900-129">Der Name des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="65900-129">The integration account name.</span></span>

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

### <span data-ttu-id="65900-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65900-130">-ResourceGroupName</span></span>
<span data-ttu-id="65900-131">Der Name der Ressourcengruppe der Integrations Konten.</span><span class="sxs-lookup"><span data-stu-id="65900-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="65900-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65900-132">-Confirm</span></span>
<span data-ttu-id="65900-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65900-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65900-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65900-134">-WhatIf</span></span>
<span data-ttu-id="65900-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65900-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65900-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65900-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65900-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65900-137">CommonParameters</span></span>
<span data-ttu-id="65900-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65900-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65900-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65900-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65900-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65900-140">INPUTS</span></span>

### <span data-ttu-id="65900-141">System. String</span><span class="sxs-lookup"><span data-stu-id="65900-141">System.String</span></span>

## <span data-ttu-id="65900-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65900-142">OUTPUTS</span></span>

### <span data-ttu-id="65900-143">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="65900-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="65900-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="65900-144">NOTES</span></span>

## <span data-ttu-id="65900-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65900-145">RELATED LINKS</span></span>

[<span data-ttu-id="65900-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="65900-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

