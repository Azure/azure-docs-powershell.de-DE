---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469708"
---
# <span data-ttu-id="1e736-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="1e736-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="1e736-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e736-102">SYNOPSIS</span></span>
<span data-ttu-id="1e736-103">Ruft den Statusverlauf der Compliance der Gastkonfigurationsrichtlinie für eine Initiative vom Typ "Guest Configuration" ab, die einer VM zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1e736-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="1e736-104">Eine Initiative ist eine Richtlinie vom Typ "Initiative".</span><span class="sxs-lookup"><span data-stu-id="1e736-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="1e736-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e736-105">SYNTAX</span></span>

### <span data-ttu-id="1e736-106">InitiativeNameScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="1e736-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e736-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="1e736-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e736-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e736-108">DESCRIPTION</span></span>
<span data-ttu-id="1e736-109">Das Get-AzVMGuestPolicyStatusHistory cmdlet ruft den Compliancestatus der Gastkonfigurationsrichtlinien für eine Initiative vom Typ "Guest Configuration" ab, die einer VM zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1e736-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="1e736-110">Eine Initiative ist eine Richtlinie vom Typ "Initiative".</span><span class="sxs-lookup"><span data-stu-id="1e736-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="1e736-111">Verwenden Get-AzVMGuestPolicyStatus cmdlet, um Details zu einem einzelnen Compliancestatus mithilfe der ReportId anzuzeigen, die in der Ausgabe des Get-AzVMGuestPolicyStatusHistory gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="1e736-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="1e736-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1e736-112">EXAMPLES</span></span>

### <span data-ttu-id="1e736-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1e736-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="1e736-114">Ruft den Compliancestatusverlauf nach Initiative-ID ab. Der Schalter "ShowOnlyChange" zeigt nur Verlaufsstatusänderungen an.</span><span class="sxs-lookup"><span data-stu-id="1e736-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="1e736-115">Überspringt Status, die sich nicht zwischen zwei Complianceprüfungen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="1e736-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="1e736-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1e736-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="1e736-117">Ruft den Compliancestatusverlauf nach Initiativename ab.</span><span class="sxs-lookup"><span data-stu-id="1e736-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="1e736-118">Der Schalter "ShowOnlyChange" zeigt nur Verlaufsstatusänderungen an.</span><span class="sxs-lookup"><span data-stu-id="1e736-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="1e736-119">Überspringt Status, die sich nicht zwischen zwei Complianceprüfungen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="1e736-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="1e736-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1e736-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="1e736-121">Ruft den Compliancestatusverlauf für alle Gastkonfigurationsrichtlinien ab, die der VM zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="1e736-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="1e736-122">Der Schalter "ShowOnlyChange" zeigt nur Verlaufsstatusänderungen an.</span><span class="sxs-lookup"><span data-stu-id="1e736-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="1e736-123">Überspringt Status, die sich nicht zwischen zwei Complianceprüfungen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="1e736-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="1e736-124">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="1e736-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="1e736-125">Ruft den Compliancestatusverlauf nach Initiative-ID ab.</span><span class="sxs-lookup"><span data-stu-id="1e736-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="1e736-126">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="1e736-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="1e736-127">Ruft den Compliancestatusverlauf nach Initiativename ab.</span><span class="sxs-lookup"><span data-stu-id="1e736-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="1e736-128">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="1e736-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="1e736-129">Ruft den Compliancestatusverlauf für alle Gastkonfigurationsrichtlinien ab, die der VM zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="1e736-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="1e736-130">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="1e736-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="1e736-131">Erhalten Sie den Status der Gastkonfigurationsrichtlinie nach ReportId.</span><span class="sxs-lookup"><span data-stu-id="1e736-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="1e736-132">Die ReportId ist die ReportId-Eigenschaft, die in den Ergebnissen von "Get-AzVMGuestPolicyStatusHistory" zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="1e736-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="1e736-133">(weitere Beispiele finden Sie hier)</span><span class="sxs-lookup"><span data-stu-id="1e736-133">(please refer other examples)</span></span>

## <span data-ttu-id="1e736-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e736-134">PARAMETERS</span></span>

### <span data-ttu-id="1e736-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e736-135">-DefaultProfile</span></span>
<span data-ttu-id="1e736-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e736-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e736-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="1e736-137">-InitiativeId</span></span>
<span data-ttu-id="1e736-138">Definitions-ID einer Richtlinie, bei der der Definitionstyp "Initiative" und die Kategorie "Gastkonfiguration" ist</span><span class="sxs-lookup"><span data-stu-id="1e736-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="1e736-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="1e736-139">-InitiativeName</span></span>
<span data-ttu-id="1e736-140">Name einer Richtlinie, bei der der Definitionstyp "Initiative" und die Kategorie "Gastkonfiguration" ist</span><span class="sxs-lookup"><span data-stu-id="1e736-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="1e736-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e736-141">-ResourceGroupName</span></span>
<span data-ttu-id="1e736-142">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="1e736-142">Resource group name.</span></span>

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

### <span data-ttu-id="1e736-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="1e736-143">-ShowOnlyChange</span></span>
<span data-ttu-id="1e736-144">Zeigt historische Statusänderungen nur für Gastkonfigurationsrichtlinien an.</span><span class="sxs-lookup"><span data-stu-id="1e736-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="1e736-145">Überspringt Status, die sich nicht zwischen zwei Ausgeführten der Compliancestatusanzeige geändert haben.</span><span class="sxs-lookup"><span data-stu-id="1e736-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

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

### <span data-ttu-id="1e736-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="1e736-146">-VMName</span></span>
<span data-ttu-id="1e736-147">VM-Name.</span><span class="sxs-lookup"><span data-stu-id="1e736-147">VM name.</span></span>

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

### <span data-ttu-id="1e736-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e736-148">CommonParameters</span></span>
<span data-ttu-id="1e736-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e736-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e736-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e736-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e736-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1e736-151">INPUTS</span></span>

### <span data-ttu-id="1e736-152">Keine</span><span class="sxs-lookup"><span data-stu-id="1e736-152">None</span></span>
## <span data-ttu-id="1e736-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1e736-153">OUTPUTS</span></span>

### <span data-ttu-id="1e736-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="1e736-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="1e736-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1e736-155">NOTES</span></span>

## <span data-ttu-id="1e736-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1e736-156">RELATED LINKS</span></span>
