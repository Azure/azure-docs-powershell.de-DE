---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 2a80173900c0faf062c3d4ba0c0a3b2029737bcf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307360"
---
# <span data-ttu-id="661a9-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="661a9-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="661a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="661a9-102">SYNOPSIS</span></span>
<span data-ttu-id="661a9-103">Dieses Cmdlet entfernt eine bestimmte empfangene Austauschsteuerelementnummer pro Vertrag und Steuerelementnummerwert.</span><span class="sxs-lookup"><span data-stu-id="661a9-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="661a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="661a9-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="661a9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="661a9-105">DESCRIPTION</span></span>
<span data-ttu-id="661a9-106">Dieses Cmdlet soll in Notfallwiederherstellungsszenarien verwendet werden, um eine empfangene Austauschsteuerelementnummer aus dem Integrationskonto zu entfernen, damit der B2B-Connector die Nachricht erneut verarbeiten kann, wenn die Duplikaterkennung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="661a9-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="661a9-107">In seltenen Fällen kann die Nummer des empfangenen Austauschsteuerelements kurz vor einem Notfall reserviert werden, bevor der B2B-Connector den Austausch als fehlerhaft ablehnt.</span><span class="sxs-lookup"><span data-stu-id="661a9-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="661a9-108">In solchen Fällen kann es sein, dass die Wiederherstellungswebsite den gleichen Austausch erneut verarbeiten soll, nachdem die Nutzlast korrigiert wurde.</span><span class="sxs-lookup"><span data-stu-id="661a9-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="661a9-109">Geben Sie den Parameter "-AgreementType" an, um anzugeben, ob X12- oder Edifact-Steuerelementnummern zurückgeben werden.</span><span class="sxs-lookup"><span data-stu-id="661a9-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="661a9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="661a9-110">EXAMPLES</span></span>

### <span data-ttu-id="661a9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="661a9-111">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="661a9-112">Versucht, eine empfangene X12-Austauschsteuerelementnummer zu erhalten, deren Inhalt kein gültiges Format hat.</span><span class="sxs-lookup"><span data-stu-id="661a9-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="661a9-113">Entfernt die empfangene X12-Austauschsteuerelementnummer.</span><span class="sxs-lookup"><span data-stu-id="661a9-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="661a9-114">Bestätigt, dass die empfangene X12 Interchange Control Number entfernt wurde, indem Sie versuchen, sie erneut zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="661a9-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="661a9-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="661a9-115">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="661a9-116">Versucht, eine empfangene Edifact-Interchange-Steuerelementnummer zu erhalten, deren Inhalt kein gültiges Format hat.</span><span class="sxs-lookup"><span data-stu-id="661a9-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="661a9-117">Entfernt die empfangene Edifact-Interchange-Steuerelementnummer.</span><span class="sxs-lookup"><span data-stu-id="661a9-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="661a9-118">Bestätigt, dass die empfangene Nummer des Edifact-Austauschsteuerelements entfernt wurde, indem Sie versuchen, sie erneut zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="661a9-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="661a9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="661a9-119">PARAMETERS</span></span>

### <span data-ttu-id="661a9-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="661a9-120">-AgreementName</span></span>
<span data-ttu-id="661a9-121">Der Name des Vertrags für das Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="661a9-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="661a9-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="661a9-122">-AgreementType</span></span>
<span data-ttu-id="661a9-123">Der Typ des Vertrags für das Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="661a9-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="661a9-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="661a9-124">-ControlNumberValue</span></span>
<span data-ttu-id="661a9-125">Der Wert für die Nummer des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="661a9-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="661a9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="661a9-126">-DefaultProfile</span></span>
<span data-ttu-id="661a9-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="661a9-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="661a9-128">-Name</span><span class="sxs-lookup"><span data-stu-id="661a9-128">-Name</span></span>
<span data-ttu-id="661a9-129">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="661a9-129">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661a9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="661a9-130">-ResourceGroupName</span></span>
<span data-ttu-id="661a9-131">Der Name der Integrationskontoressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="661a9-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="661a9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="661a9-132">-Confirm</span></span>
<span data-ttu-id="661a9-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="661a9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="661a9-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="661a9-134">-WhatIf</span></span>
<span data-ttu-id="661a9-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="661a9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="661a9-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="661a9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="661a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="661a9-137">CommonParameters</span></span>
<span data-ttu-id="661a9-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="661a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="661a9-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="661a9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="661a9-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="661a9-140">INPUTS</span></span>

### <span data-ttu-id="661a9-141">System.String</span><span class="sxs-lookup"><span data-stu-id="661a9-141">System.String</span></span>

## <span data-ttu-id="661a9-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="661a9-142">OUTPUTS</span></span>

### <span data-ttu-id="661a9-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="661a9-143">System.Void</span></span>

## <span data-ttu-id="661a9-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="661a9-144">NOTES</span></span>

## <span data-ttu-id="661a9-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="661a9-145">RELATED LINKS</span></span>

<span data-ttu-id="661a9-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="661a9-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

