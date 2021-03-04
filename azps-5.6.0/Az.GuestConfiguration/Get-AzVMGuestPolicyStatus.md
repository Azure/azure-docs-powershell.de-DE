---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 3edb92ae8c46ab67e0e22ee808e38dad7101bfdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938136"
---
# <span data-ttu-id="66a81-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="66a81-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="66a81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66a81-102">SYNOPSIS</span></span>
<span data-ttu-id="66a81-103">Ruft gastkonfigurationsrichtlinienstatus (detailliert) für eine Initiative vom Typ "Gastkonfiguration" ab, die einer VM zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="66a81-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="66a81-104">Eine Initiative ist eine Richtlinie des Definitionstyps "Initiative".</span><span class="sxs-lookup"><span data-stu-id="66a81-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="66a81-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66a81-105">SYNTAX</span></span>

### <span data-ttu-id="66a81-106">VmScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="66a81-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66a81-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="66a81-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66a81-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="66a81-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66a81-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="66a81-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66a81-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66a81-110">DESCRIPTION</span></span>
<span data-ttu-id="66a81-111">Das Get-AzVMGuestPolicyStatus-Cmdlet ruft Gastkonfigurationsrichtlinienstatus für eine Initiative vom Typ "Gastkonfiguration" ab, die einer VM zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="66a81-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="66a81-112">Eine Initiative ist eine Richtlinie des Definitionstyps "Initiative".</span><span class="sxs-lookup"><span data-stu-id="66a81-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="66a81-113">Dieses Cmdlet erhält den Compliancestatus der VM und die Gründe, warum es für die einzelnen Richtlinien in der Initiative nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="66a81-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="66a81-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66a81-114">EXAMPLES</span></span>

### <span data-ttu-id="66a81-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66a81-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="66a81-116">Erhalten Sie alle aktuellen Status der Gastkonfigurationsrichtlinien für eine VM.</span><span class="sxs-lookup"><span data-stu-id="66a81-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="66a81-117">Der Status umfasst den Compliancestatus der VM für jede Richtlinie in allen Initiativen vom Typ "Gastkonfiguration", Compliancegründe, Uhrzeit der Complianceüberprüfung, Ressourceninformationen, die auf Compliance überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="66a81-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="66a81-118">Die Ergebnisse enthalten die neuesten Status und keine vorherigen historischen Status.</span><span class="sxs-lookup"><span data-stu-id="66a81-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="66a81-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="66a81-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="66a81-120">Holen Sie sich die neuesten Status der Gastkonfigurationsrichtlinien nach Initiative-ID. Der Status umfasst den Compliancestatus der VM für jede Richtlinie in der Initiative, Compliancegründe, Uhrzeit der Complianceüberprüfung, Ressourceninformationen, die auf Compliance überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="66a81-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="66a81-121">Die Ergebnisse enthalten keine zuvor generierten Status, sondern nur den neuesten Status für jede Richtlinie in der Initiative.</span><span class="sxs-lookup"><span data-stu-id="66a81-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="66a81-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="66a81-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="66a81-123">Holen Sie sich die neuesten Status der Gastkonfigurationsrichtlinien nach Dem Namen der Initiative.</span><span class="sxs-lookup"><span data-stu-id="66a81-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="66a81-124">Der Status umfasst den Compliancestatus der VM für jede Richtlinie in der Initiative, Compliancegründe, Uhrzeit der Complianceüberprüfung, Ressourceninformationen, die auf Compliance überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="66a81-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="66a81-125">Die Ergebnisse enthalten keine zuvor generierten Status, sondern nur den neuesten Status für jede Richtlinie in der Initiative.</span><span class="sxs-lookup"><span data-stu-id="66a81-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="66a81-126">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="66a81-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="66a81-127">Holen Sie sich den Status der Gastkonfigurationsrichtlinie nach ReportId.</span><span class="sxs-lookup"><span data-stu-id="66a81-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="66a81-128">Die ReportId ist die ReportId-Eigenschaft, die in den Ergebnissen von Get-AzVMGuestPolicyStatus von initiativeId oder Initiative name zu finden ist (weitere Beispiele finden Sie hier).</span><span class="sxs-lookup"><span data-stu-id="66a81-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="66a81-129">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="66a81-129">PARAMETERS</span></span>

### <span data-ttu-id="66a81-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a81-130">-DefaultProfile</span></span>
<span data-ttu-id="66a81-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66a81-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66a81-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="66a81-132">-InitiativeId</span></span>
<span data-ttu-id="66a81-133">Definitions-ID einer Richtlinie, bei der der Definitionstyp "Initiative" und "Kategorie" "Gastkonfiguration" ist</span><span class="sxs-lookup"><span data-stu-id="66a81-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a81-134">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="66a81-134">-InitiativeName</span></span>
<span data-ttu-id="66a81-135">Name einer Richtlinie, deren Definitionstyp "Initiative" und "Kategorie" "Gastkonfiguration" ist</span><span class="sxs-lookup"><span data-stu-id="66a81-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a81-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="66a81-136">-ReportId</span></span>
<span data-ttu-id="66a81-137">Id eines Richtlinienstatus der Gastkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="66a81-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="66a81-138">Eine Richtlinie, bei der der Definitionstyp "Initiative" und die Kategorie "Gastkonfiguration" ist, muss einem Bereich zugewiesen werden, um Status zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="66a81-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a81-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a81-139">-ResourceGroupName</span></span>
<span data-ttu-id="66a81-140">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="66a81-140">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a81-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="66a81-141">-VMName</span></span>
<span data-ttu-id="66a81-142">VM-Name.</span><span class="sxs-lookup"><span data-stu-id="66a81-142">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a81-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a81-143">CommonParameters</span></span>
<span data-ttu-id="66a81-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a81-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a81-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a81-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a81-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66a81-146">INPUTS</span></span>

### <span data-ttu-id="66a81-147">Keine</span><span class="sxs-lookup"><span data-stu-id="66a81-147">None</span></span>
## <span data-ttu-id="66a81-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66a81-148">OUTPUTS</span></span>

### <span data-ttu-id="66a81-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="66a81-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="66a81-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="66a81-150">NOTES</span></span>

## <span data-ttu-id="66a81-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="66a81-151">RELATED LINKS</span></span>
