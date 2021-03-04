---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 076679499cf64100bcded5a29e7bc158a81423ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927080"
---
# <span data-ttu-id="b170b-101">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="b170b-101">Set-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="b170b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b170b-102">SYNOPSIS</span></span>
<span data-ttu-id="b170b-103">Aktualisiert das integration account received interchange control number (ICN) in the Azure resource group.</span><span class="sxs-lookup"><span data-stu-id="b170b-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="b170b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b170b-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b170b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b170b-105">DESCRIPTION</span></span>
<span data-ttu-id="b170b-106">Das Set-AzIntegrationAccountGeneratedIcn-Cmdlet aktualisiert ein vorhandenes Integrationskonto, das die IcN (Interchange Control Number) erhalten hat, und gibt ein -Objekt zurück, das das empfangene Austauschsteuerelementnummer des Integrationskontos darstellt.</span><span class="sxs-lookup"><span data-stu-id="b170b-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="b170b-107">Verwenden Sie dieses Cmdlet, um den Status der Nachrichtenverarbeitungsnummer eines Integrationskontos zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b170b-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="b170b-108">Sie können ein integration account received interchange control number aktualisieren, indem Sie den Namen des Integrationskontos, den Ressourcengruppennamen, den Vertragsnamen, den Steuerelementnummerwert und den Status der Nachrichtenverarbeitung angeben.</span><span class="sxs-lookup"><span data-stu-id="b170b-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="b170b-109">Sie können mit diesem Befehl kein neues Integrationskonto erstellen, das die Nummer des Austauschsteuerelements erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="b170b-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="b170b-110">Wenn Sie die dynamischen Parameter verwenden möchten, geben Sie sie einfach in den Befehl ein, oder geben Sie ein Trennzeichen(-) ein, um einen Parameternamen anzugeben, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="b170b-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b170b-111">Wenn Sie einen erforderlichen Vorlagenparameter vermissen, werden Sie vom Cmdlet zum Wert aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b170b-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="b170b-112">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="b170b-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="b170b-113">Geben Sie den Parameter "-AgreementType" an, um anzugeben, ob X12- oder Edifact-Steuerelementnummern</span><span class="sxs-lookup"><span data-stu-id="b170b-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="b170b-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b170b-114">EXAMPLES</span></span>

### <span data-ttu-id="b170b-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b170b-115">Example 1</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="b170b-116">Mit diesem Befehl wird das Integrationskonto aktualisiert, das die X12-Austauschsteuerungsnummer für einen bestimmten Integrationskontovertrag erhalten hat, und den Wert, bei dem der Status der Nachrichtenverarbeitung fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="b170b-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="b170b-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b170b-117">Example 2</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="b170b-118">Mit diesem Befehl wird das integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b170b-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="b170b-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b170b-119">PARAMETERS</span></span>

### <span data-ttu-id="b170b-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="b170b-120">-AgreementName</span></span>
<span data-ttu-id="b170b-121">Der Name des Integrationskontovertrags.</span><span class="sxs-lookup"><span data-stu-id="b170b-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="b170b-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="b170b-122">-AgreementType</span></span>
<span data-ttu-id="b170b-123">Der Typ des Integrationskontovertrags (X12 oder Edifact).</span><span class="sxs-lookup"><span data-stu-id="b170b-123">The integration account agreement type (X12 or Edifact).</span></span>

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

### <span data-ttu-id="b170b-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="b170b-124">-ControlNumberValue</span></span>
<span data-ttu-id="b170b-125">Der Nummerwert des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="b170b-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="b170b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b170b-126">-DefaultProfile</span></span>
<span data-ttu-id="b170b-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b170b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b170b-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="b170b-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="b170b-129">Der Status der Verarbeitung empfangener Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="b170b-129">The received message processing status.</span></span>

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

### <span data-ttu-id="b170b-130">-Name</span><span class="sxs-lookup"><span data-stu-id="b170b-130">-Name</span></span>
<span data-ttu-id="b170b-131">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="b170b-131">The integration account name.</span></span>

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

### <span data-ttu-id="b170b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b170b-132">-ResourceGroupName</span></span>
<span data-ttu-id="b170b-133">Name der Ressourcengruppe des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="b170b-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="b170b-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b170b-134">-Confirm</span></span>
<span data-ttu-id="b170b-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b170b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b170b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b170b-136">-WhatIf</span></span>
<span data-ttu-id="b170b-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b170b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b170b-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b170b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b170b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b170b-139">CommonParameters</span></span>
<span data-ttu-id="b170b-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b170b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b170b-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b170b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b170b-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b170b-142">INPUTS</span></span>

### <span data-ttu-id="b170b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b170b-143">System.String</span></span>

## <span data-ttu-id="b170b-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b170b-144">OUTPUTS</span></span>

### <span data-ttu-id="b170b-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="b170b-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="b170b-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b170b-146">NOTES</span></span>

## <span data-ttu-id="b170b-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b170b-147">RELATED LINKS</span></span>

<span data-ttu-id="b170b-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="b170b-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span></span>
