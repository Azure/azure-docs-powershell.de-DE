---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 2e2474b784d66c3c3c34bc9ea9abc2b0959ea500
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819983"
---
# <span data-ttu-id="3d165-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="3d165-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="3d165-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d165-102">SYNOPSIS</span></span>
<span data-ttu-id="3d165-103">Ruft den Kompatibilitätsstatus des Gast Konfigurationsrichtlinien für eine Initiative des Typs "Gast Konfiguration" ab, die einem virtuellen Computer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3d165-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="3d165-104">Eine Initiative ist eine Richtlinie des Definitions Typs "Initiative".</span><span class="sxs-lookup"><span data-stu-id="3d165-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="3d165-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d165-105">SYNTAX</span></span>

### <span data-ttu-id="3d165-106">InitiativeNameScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d165-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d165-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="3d165-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d165-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d165-108">DESCRIPTION</span></span>
<span data-ttu-id="3d165-109">Das Get-AzVMGuestPolicyStatusHistory-Cmdlet ruft den Kompatibilitätsstatus Verlauf von Gast Konfigurationsrichtlinien für eine Initiative des Typs "Gast Konfiguration" ab, die einem virtuellen Computer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3d165-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="3d165-110">Eine Initiative ist eine Richtlinie des Definitions Typs "Initiative".</span><span class="sxs-lookup"><span data-stu-id="3d165-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="3d165-111">Verwenden Sie Get-AzVMGuestPolicyStatus-Cmdlet, um Details zu einem einzelnen Kompatibilitätsstatus mithilfe der Berichts-Nr abzurufen, die in der Ausgabe des Get-AzVMGuestPolicyStatusHistory-Cmdlets zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="3d165-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="3d165-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d165-112">EXAMPLES</span></span>

### <span data-ttu-id="3d165-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d165-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="3d165-114">Ruft den Konformitätsstatus Verlauf nach initiativ-ID ab. ShowOnlyChange-Schalter zeigt nur Verlaufsstatus Änderungen an.</span><span class="sxs-lookup"><span data-stu-id="3d165-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="3d165-115">Überspringt Status, die sich zwischen zwei Kompatibilitätsprüfungen nicht geändert haben.</span><span class="sxs-lookup"><span data-stu-id="3d165-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="3d165-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3d165-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="3d165-117">Ruft den Konformitätsstatus Verlauf nach initiativ Name ab.</span><span class="sxs-lookup"><span data-stu-id="3d165-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="3d165-118">ShowOnlyChange-Schalter zeigt nur Änderungen des Verlaufsstatus an.</span><span class="sxs-lookup"><span data-stu-id="3d165-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="3d165-119">Überspringt Status, die sich zwischen zwei Kompatibilitätsprüfungen nicht geändert haben.</span><span class="sxs-lookup"><span data-stu-id="3d165-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="3d165-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3d165-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="3d165-121">Ruft den Kompatibilitätsstatus Verlauf für alle Guest-Konfigurationsrichtlinien ab, die dem virtuellen Computer zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="3d165-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="3d165-122">ShowOnlyChange-Schalter zeigt nur Änderungen des Verlaufsstatus an.</span><span class="sxs-lookup"><span data-stu-id="3d165-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="3d165-123">Überspringt Status, die sich zwischen zwei Kompatibilitätsprüfungen nicht geändert haben.</span><span class="sxs-lookup"><span data-stu-id="3d165-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="3d165-124">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="3d165-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="3d165-125">Ruft den Konformitätsstatus Verlauf nach initiativ-ID ab.</span><span class="sxs-lookup"><span data-stu-id="3d165-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="3d165-126">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="3d165-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="3d165-127">Ruft den Konformitätsstatus Verlauf nach initiativ Name ab.</span><span class="sxs-lookup"><span data-stu-id="3d165-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="3d165-128">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="3d165-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="3d165-129">Ruft den Kompatibilitätsstatus Verlauf für alle Guest-Konfigurationsrichtlinien ab, die dem virtuellen Computer zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="3d165-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="3d165-130">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="3d165-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="3d165-131">Abrufen des Gast Konfigurationsrichtlinien Status nach Berichts-Nr.</span><span class="sxs-lookup"><span data-stu-id="3d165-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="3d165-132">Die Berichts-Nr ist die Eigenschaft "Reporter", die in den Ergebnissen von Get-AzVMGuestPolicyStatusHistory zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="3d165-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="3d165-133">(Weitere Beispiele finden Sie hier)</span><span class="sxs-lookup"><span data-stu-id="3d165-133">(please refer other examples)</span></span>

## <span data-ttu-id="3d165-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d165-134">PARAMETERS</span></span>

### <span data-ttu-id="3d165-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d165-135">-DefaultProfile</span></span>
<span data-ttu-id="3d165-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d165-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d165-137">-Initiativ-Nr.</span><span class="sxs-lookup"><span data-stu-id="3d165-137">-InitiativeId</span></span>
<span data-ttu-id="3d165-138">Definitions-ID einer Richtlinie, bei der der Definitions Initiative und Kategorie ist Gast Konfiguration ist</span><span class="sxs-lookup"><span data-stu-id="3d165-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="3d165-139">-Initiativname</span><span class="sxs-lookup"><span data-stu-id="3d165-139">-InitiativeName</span></span>
<span data-ttu-id="3d165-140">Name einer Richtlinie, bei der der Definitions "Initiative" und "Kategorie" Gast Konfiguration ist</span><span class="sxs-lookup"><span data-stu-id="3d165-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="3d165-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d165-141">-ResourceGroupName</span></span>
<span data-ttu-id="3d165-142">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3d165-142">Resource group name.</span></span>

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

### <span data-ttu-id="3d165-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="3d165-143">-ShowOnlyChange</span></span>
<span data-ttu-id="3d165-144">Zeigt Änderungen des Verlaufsstatus nur für Gast Konfigurationsrichtlinien an.</span><span class="sxs-lookup"><span data-stu-id="3d165-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="3d165-145">Überspringt Status, die sich zwischen zwei Kompatibilitätsstatus-Überwachungs Läufen nicht geändert haben.</span><span class="sxs-lookup"><span data-stu-id="3d165-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

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

### <span data-ttu-id="3d165-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="3d165-146">-VMName</span></span>
<span data-ttu-id="3d165-147">VM-Name.</span><span class="sxs-lookup"><span data-stu-id="3d165-147">VM name.</span></span>

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

### <span data-ttu-id="3d165-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d165-148">CommonParameters</span></span>
<span data-ttu-id="3d165-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d165-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d165-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d165-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d165-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d165-151">INPUTS</span></span>

### <span data-ttu-id="3d165-152">Keine</span><span class="sxs-lookup"><span data-stu-id="3d165-152">None</span></span>
## <span data-ttu-id="3d165-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d165-153">OUTPUTS</span></span>

### <span data-ttu-id="3d165-154">Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="3d165-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="3d165-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d165-155">NOTES</span></span>

## <span data-ttu-id="3d165-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d165-156">RELATED LINKS</span></span>
