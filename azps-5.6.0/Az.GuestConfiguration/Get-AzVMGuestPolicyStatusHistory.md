---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 9161b3c9c55c1014b64419a3644bf7ec80af8648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938131"
---
# <span data-ttu-id="7cd40-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="7cd40-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="7cd40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cd40-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd40-103">Ruft den Compliancestatus der Gastkonfigurationsrichtlinie für eine Initiative vom Typ "Gastkonfiguration" ab, die einer VM zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7cd40-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="7cd40-104">Eine Initiative ist eine Richtlinie des Definitionstyps "Initiative".</span><span class="sxs-lookup"><span data-stu-id="7cd40-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="7cd40-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cd40-105">SYNTAX</span></span>

### <span data-ttu-id="7cd40-106">InitiativeNameScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="7cd40-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cd40-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="7cd40-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cd40-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7cd40-108">DESCRIPTION</span></span>
<span data-ttu-id="7cd40-109">Das Get-AzVMGuestPolicyStatusHistory-Cmdlet ruft den Compliancestatusverlauf von Gastkonfigurationsrichtlinien für eine Initiative vom Typ "Gastkonfiguration" ab, die einer VM zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7cd40-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="7cd40-110">Eine Initiative ist eine Richtlinie des Definitionstyps "Initiative".</span><span class="sxs-lookup"><span data-stu-id="7cd40-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="7cd40-111">Verwenden Get-AzVMGuestPolicyStatus cmdlet, um Details zu einem einzelnen Compliancestatus mithilfe von ReportId zu erhalten, die in der Ausgabe des cmdlets Get-AzVMGuestPolicyStatusHistory finden.</span><span class="sxs-lookup"><span data-stu-id="7cd40-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="7cd40-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7cd40-112">EXAMPLES</span></span>

### <span data-ttu-id="7cd40-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7cd40-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="7cd40-114">Ruft den Compliancestatusverlauf nach Initiative-ID ab. Der ShowOnlyChange-Schalter zeigt nur historische Statusänderungen an.</span><span class="sxs-lookup"><span data-stu-id="7cd40-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="7cd40-115">Überspringt Status, die sich nicht zwischen zwei Complianceüberprüfungen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="7cd40-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="7cd40-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7cd40-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="7cd40-117">Ruft den Compliancestatusverlauf nach Dem Namen der Initiative ab.</span><span class="sxs-lookup"><span data-stu-id="7cd40-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="7cd40-118">Der ShowOnlyChange-Schalter zeigt nur historische Statusänderungen an.</span><span class="sxs-lookup"><span data-stu-id="7cd40-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="7cd40-119">Überspringt Status, die sich nicht zwischen zwei Complianceüberprüfungen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="7cd40-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="7cd40-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7cd40-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="7cd40-121">Ruft den Compliancestatusverlauf für alle der VM zugewiesenen Gastkonfigurationsrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="7cd40-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="7cd40-122">Der ShowOnlyChange-Schalter zeigt nur historische Statusänderungen an.</span><span class="sxs-lookup"><span data-stu-id="7cd40-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="7cd40-123">Überspringt Status, die sich nicht zwischen zwei Complianceüberprüfungen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="7cd40-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="7cd40-124">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="7cd40-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="7cd40-125">Ruft den Compliancestatusverlauf nach Initiative-ID ab.</span><span class="sxs-lookup"><span data-stu-id="7cd40-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="7cd40-126">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="7cd40-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="7cd40-127">Ruft den Compliancestatusverlauf nach Dem Namen der Initiative ab.</span><span class="sxs-lookup"><span data-stu-id="7cd40-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="7cd40-128">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="7cd40-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="7cd40-129">Ruft den Compliancestatusverlauf für alle der VM zugewiesenen Gastkonfigurationsrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="7cd40-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="7cd40-130">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="7cd40-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="7cd40-131">Holen Sie sich den Status der Gastkonfigurationsrichtlinie nach ReportId.</span><span class="sxs-lookup"><span data-stu-id="7cd40-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="7cd40-132">Die ReportId ist die ReportId-Eigenschaft, die in den Ergebnissen von Get-AzVMGuestPolicyStatusHistory zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="7cd40-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="7cd40-133">(weitere Beispiele finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="7cd40-133">(please refer other examples)</span></span>

## <span data-ttu-id="7cd40-134">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7cd40-134">PARAMETERS</span></span>

### <span data-ttu-id="7cd40-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd40-135">-DefaultProfile</span></span>
<span data-ttu-id="7cd40-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cd40-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cd40-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="7cd40-137">-InitiativeId</span></span>
<span data-ttu-id="7cd40-138">Definitions-ID einer Richtlinie, bei der der Definitionstyp "Initiative" und "Kategorie" "Gastkonfiguration" ist</span><span class="sxs-lookup"><span data-stu-id="7cd40-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd40-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="7cd40-139">-InitiativeName</span></span>
<span data-ttu-id="7cd40-140">Name einer Richtlinie, deren Definitionstyp "Initiative" und "Kategorie" "Gastkonfiguration" ist</span><span class="sxs-lookup"><span data-stu-id="7cd40-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="7cd40-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cd40-141">-ResourceGroupName</span></span>
<span data-ttu-id="7cd40-142">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7cd40-142">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd40-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="7cd40-143">-ShowOnlyChange</span></span>
<span data-ttu-id="7cd40-144">Zeigt Änderungen des verlaufshistorischen Status nur für Gastkonfigurationsrichtlinien an.</span><span class="sxs-lookup"><span data-stu-id="7cd40-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="7cd40-145">Überspringt Status, die sich nicht zwischen zwei Compliancestatusprüfungsläufen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="7cd40-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd40-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="7cd40-146">-VMName</span></span>
<span data-ttu-id="7cd40-147">VM-Name.</span><span class="sxs-lookup"><span data-stu-id="7cd40-147">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd40-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd40-148">CommonParameters</span></span>
<span data-ttu-id="7cd40-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cd40-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd40-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cd40-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd40-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7cd40-151">INPUTS</span></span>

### <span data-ttu-id="7cd40-152">Keine</span><span class="sxs-lookup"><span data-stu-id="7cd40-152">None</span></span>
## <span data-ttu-id="7cd40-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7cd40-153">OUTPUTS</span></span>

### <span data-ttu-id="7cd40-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="7cd40-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="7cd40-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7cd40-155">NOTES</span></span>

## <span data-ttu-id="7cd40-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7cd40-156">RELATED LINKS</span></span>
