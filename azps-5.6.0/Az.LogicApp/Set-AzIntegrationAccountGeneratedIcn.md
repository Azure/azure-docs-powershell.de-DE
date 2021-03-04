---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 4c91ced490226901a45e0eacb7caa204daa20558
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931019"
---
# <span data-ttu-id="7d1ca-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="7d1ca-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="7d1ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1ca-103">Aktualisiert das integration account generated interchange control number (ICN) in der Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="7d1ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d1ca-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d1ca-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="7d1ca-106">Das Set-AzIntegrationAccountGeneratedIcn-Cmdlet aktualisiert ein vorhandenes Integrationskonto generierte Interchange Control Number (ICN) und gibt ein -Objekt zurück, das die generierte Austauschsteuerelementnummer des Integrationskontos darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="7d1ca-107">Verwenden Sie dieses Cmdlet, um ein integration account generated interchange control number zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="7d1ca-108">Sie können ein integration account generated interchange control number aktualisieren, indem Sie den Namen des Integrationskontos, den Namen der Ressourcengruppe und den Vertragsnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="7d1ca-109">Sie können mit diesem Befehl kein neues Integrationskonto erstellen, das die Nummer des Austauschsteuerelements generiert hat.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="7d1ca-110">Wenn Sie die dynamischen Parameter verwenden möchten, geben Sie sie einfach in den Befehl ein, oder geben Sie ein Trennzeichen(-) ein, um einen Parameternamen anzugeben, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7d1ca-111">Wenn Sie einen erforderlichen Vorlagenparameter vermissen, werden Sie vom Cmdlet zum Wert aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="7d1ca-112">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="7d1ca-113">Geben Sie den Parameter "-AgreementType" an, um anzugeben, ob X12- oder Edifact-Steuerelementnummern</span><span class="sxs-lookup"><span data-stu-id="7d1ca-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="7d1ca-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7d1ca-114">EXAMPLES</span></span>

### <span data-ttu-id="7d1ca-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7d1ca-115">Example 1</span></span>
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

<span data-ttu-id="7d1ca-116">Dieser Befehl ruft die generierte X12-Austauschsteuerungsnummer für ein bestimmtes Integrationskonto ab, erhöht den Wert um 100 und schreibt dann den aktualisierten Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="7d1ca-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7d1ca-117">Example 2</span></span>
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

<span data-ttu-id="7d1ca-118">Dieser Befehl ruft die generierte EdifactIntegrationAccountAgreement Interchange Control Number für einen bestimmten Integrationskontovertrag ab, erhöht den Wert um 100 und schreibt dann den aktualisierten Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="7d1ca-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7d1ca-119">PARAMETERS</span></span>

### <span data-ttu-id="7d1ca-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="7d1ca-120">-AgreementName</span></span>
<span data-ttu-id="7d1ca-121">Der Name des Integrationskontovertrags.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="7d1ca-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="7d1ca-122">-AgreementType</span></span>
<span data-ttu-id="7d1ca-123">Der Typ des Integrationskontovertrags.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="7d1ca-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="7d1ca-124">-ControlNumber</span></span>
<span data-ttu-id="7d1ca-125">Der generierte Steuerelementnummer neuer Wert.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="7d1ca-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1ca-126">-DefaultProfile</span></span>
<span data-ttu-id="7d1ca-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7d1ca-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d1ca-128">-Name</span><span class="sxs-lookup"><span data-stu-id="7d1ca-128">-Name</span></span>
<span data-ttu-id="7d1ca-129">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-129">The integration account name.</span></span>

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

### <span data-ttu-id="7d1ca-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1ca-130">-ResourceGroupName</span></span>
<span data-ttu-id="7d1ca-131">Name der Ressourcengruppe des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="7d1ca-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7d1ca-132">-Confirm</span></span>
<span data-ttu-id="7d1ca-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d1ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d1ca-134">-WhatIf</span></span>
<span data-ttu-id="7d1ca-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d1ca-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d1ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1ca-137">CommonParameters</span></span>
<span data-ttu-id="7d1ca-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d1ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1ca-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d1ca-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1ca-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7d1ca-140">INPUTS</span></span>

### <span data-ttu-id="7d1ca-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7d1ca-141">System.String</span></span>

## <span data-ttu-id="7d1ca-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7d1ca-142">OUTPUTS</span></span>

### <span data-ttu-id="7d1ca-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="7d1ca-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="7d1ca-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7d1ca-144">NOTES</span></span>

## <span data-ttu-id="7d1ca-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7d1ca-145">RELATED LINKS</span></span>

[<span data-ttu-id="7d1ca-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="7d1ca-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

