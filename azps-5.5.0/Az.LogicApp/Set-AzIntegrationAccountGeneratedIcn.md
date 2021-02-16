---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: fa02d7ffc23706564b8b6fe118f12525829b27f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154801"
---
# <span data-ttu-id="21fa3-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="21fa3-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="21fa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="21fa3-103">Aktualisiert das von einem Integrationskonto generierte ICN (Interchange Control Number) in der Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="21fa3-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="21fa3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21fa3-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21fa3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21fa3-105">DESCRIPTION</span></span>
<span data-ttu-id="21fa3-106">Das Set-AzIntegrationAccountGeneratedIcn-Cmdlet aktualisiert ein vorhandenes, für ein Integrationskonto generiertes Interchange Control Number (ICN) und gibt ein Objekt zurück, das die generierte Austauschsteuerelementnummer des Integrationskontos darstellt.</span><span class="sxs-lookup"><span data-stu-id="21fa3-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="21fa3-107">Verwenden Sie dieses Cmdlet, um die generierte Austauschsteuerelementnummer eines Integrationskontos zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="21fa3-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="21fa3-108">Sie können die generierte Nummer eines Austauschsteuerelements für ein Integrationskonto aktualisieren, indem Sie den Namen des Integrationskontos, den Namen der Ressourcengruppe und den Namen des Vertrags angeben.</span><span class="sxs-lookup"><span data-stu-id="21fa3-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="21fa3-109">Sie können mit diesem Befehl kein neues Integrationskonto erstellen, das die Nummer des Austauschsteuerelements generiert hat.</span><span class="sxs-lookup"><span data-stu-id="21fa3-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="21fa3-110">Um die dynamischen Parameter zu verwenden, geben Sie sie einfach in den Befehl ein, oder geben Sie ein Bindestrichzeichen(-) ein, um einen Parameternamen anzugeben, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchschreiben.</span><span class="sxs-lookup"><span data-stu-id="21fa3-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="21fa3-111">Wenn Sie einen erforderlichen Vorlagenparameter vermissen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="21fa3-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="21fa3-112">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="21fa3-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="21fa3-113">Geben Sie den Parameter "-AgreementType" an, um anzugeben, ob X12- oder Edifact-Steuerelementnummern zurückgeben werden.</span><span class="sxs-lookup"><span data-stu-id="21fa3-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="21fa3-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21fa3-114">EXAMPLES</span></span>

### <span data-ttu-id="21fa3-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="21fa3-115">Example 1</span></span>
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

<span data-ttu-id="21fa3-116">Dieser Befehl ruft die generierte X12-Austauschsteuerelementnummer für eine bestimmte Vereinbarung für ein Integrationskonto ab, erhöht seinen Wert um 100 und schreibt dann den aktualisierten Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="21fa3-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="21fa3-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="21fa3-117">Example 2</span></span>
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

<span data-ttu-id="21fa3-118">Dieser Befehl ruft die generierte EdifactIntegrationAccountAgreement Interchange Control Number für einen bestimmten Vertrag für ein Integrationskonto ab, erhöht seinen Wert um 100 und schreibt dann den aktualisierten Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="21fa3-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="21fa3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21fa3-119">PARAMETERS</span></span>

### <span data-ttu-id="21fa3-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="21fa3-120">-AgreementName</span></span>
<span data-ttu-id="21fa3-121">Der Name des Vertrags für das Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="21fa3-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="21fa3-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="21fa3-122">-AgreementType</span></span>
<span data-ttu-id="21fa3-123">Der Typ des Vertrags für das Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="21fa3-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="21fa3-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="21fa3-124">-ControlNumber</span></span>
<span data-ttu-id="21fa3-125">Der generierte Steuerelementnummer neuer Wert.</span><span class="sxs-lookup"><span data-stu-id="21fa3-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="21fa3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21fa3-126">-DefaultProfile</span></span>
<span data-ttu-id="21fa3-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="21fa3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21fa3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="21fa3-128">-Name</span></span>
<span data-ttu-id="21fa3-129">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="21fa3-129">The integration account name.</span></span>

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

### <span data-ttu-id="21fa3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21fa3-130">-ResourceGroupName</span></span>
<span data-ttu-id="21fa3-131">Der Name der Integrationskontoressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="21fa3-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="21fa3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21fa3-132">-Confirm</span></span>
<span data-ttu-id="21fa3-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21fa3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21fa3-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="21fa3-134">-WhatIf</span></span>
<span data-ttu-id="21fa3-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21fa3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21fa3-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21fa3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21fa3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21fa3-137">CommonParameters</span></span>
<span data-ttu-id="21fa3-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21fa3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21fa3-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21fa3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21fa3-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21fa3-140">INPUTS</span></span>

### <span data-ttu-id="21fa3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="21fa3-141">System.String</span></span>

## <span data-ttu-id="21fa3-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21fa3-142">OUTPUTS</span></span>

### <span data-ttu-id="21fa3-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="21fa3-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="21fa3-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="21fa3-144">NOTES</span></span>

## <span data-ttu-id="21fa3-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="21fa3-145">RELATED LINKS</span></span>

[<span data-ttu-id="21fa3-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="21fa3-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

