---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175608"
---
# <span data-ttu-id="f58b4-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="f58b4-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="f58b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f58b4-102">SYNOPSIS</span></span>
<span data-ttu-id="f58b4-103">Ruft den Status der gastkonfigurations Richtlinien (detailliert) für eine Initiative des Typs "Gast Konfiguration" ab, die einem virtuellen Computer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f58b4-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="f58b4-104">Eine Initiative ist eine Richtlinie des Definitions Typs "Initiative".</span><span class="sxs-lookup"><span data-stu-id="f58b4-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="f58b4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f58b4-105">SYNTAX</span></span>

### <span data-ttu-id="f58b4-106">VmScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="f58b4-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f58b4-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="f58b4-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f58b4-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="f58b4-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f58b4-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="f58b4-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f58b4-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f58b4-110">DESCRIPTION</span></span>
<span data-ttu-id="f58b4-111">Das Get-AzVMGuestPolicyStatus-Cmdlet ruft den Status der gastkonfigurations Richtlinie für eine Initiative des Typs "Gast Konfiguration" ab, die einem virtuellen Computer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f58b4-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="f58b4-112">Eine Initiative ist eine Richtlinie des Definitions Typs "Initiative".</span><span class="sxs-lookup"><span data-stu-id="f58b4-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="f58b4-113">Dieses Cmdlet ruft den Konformitätsstatus der VM ab und begründet, warum Sie für die einzelnen Richtlinien in der Initiative nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="f58b4-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="f58b4-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f58b4-114">EXAMPLES</span></span>

### <span data-ttu-id="f58b4-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f58b4-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="f58b4-116">Abrufen allerneuesten Einstellungen für die Gast Konfiguration für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="f58b4-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="f58b4-117">Der Status umfasst den Kompatibilitätsstatus des virtuellen Computers für jede Richtlinie in allen Initiativen des Typs "Gast Konfiguration", Konformitäts Gründe, Zeitpunkt der Konformitätsprüfung, Ressourceninformationen, die auf die Compliance überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="f58b4-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="f58b4-118">Die Ergebnisse umfassen die neuesten Status, beinhalten keine vorherigen Verlaufsstatus.</span><span class="sxs-lookup"><span data-stu-id="f58b4-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="f58b4-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f58b4-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="f58b4-120">Besorgen Sie sich die neuesten Einstellungen für Gast Konfigurationsrichtlinien nach initiativ-ID. Der Status umfasst den Kompatibilitätsstatus des virtuellen Computers für jede Richtlinie in der Initiative, Compliance-Gründen, Zeitpunkt der Konformitätsprüfung, Ressourceninformationen, die auf Compliance überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="f58b4-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="f58b4-121">Die Ergebnisse beinhalten keine generierten vorherigen Status, sondern enthalten nur den neuesten Status für jede Richtlinie in der Initiative.</span><span class="sxs-lookup"><span data-stu-id="f58b4-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="f58b4-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f58b4-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="f58b4-123">Besorgen Sie sich die neuesten Einstellungen für Gast Konfigurationsrichtlinien nach initiativ Namen.</span><span class="sxs-lookup"><span data-stu-id="f58b4-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="f58b4-124">Der Status umfasst den Kompatibilitätsstatus des virtuellen Computers für jede Richtlinie in der Initiative, Compliance-Gründen, Zeitpunkt der Konformitätsprüfung, Ressourceninformationen, die auf Compliance überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="f58b4-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="f58b4-125">Die Ergebnisse beinhalten keine generierten vorherigen Status, sondern enthalten nur den neuesten Status für jede Richtlinie in der Initiative.</span><span class="sxs-lookup"><span data-stu-id="f58b4-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="f58b4-126">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="f58b4-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="f58b4-127">Abrufen des Gast Konfigurationsrichtlinien Status nach Berichts-Nr.</span><span class="sxs-lookup"><span data-stu-id="f58b4-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="f58b4-128">Die Berichts-Nr ist die Eigenschaft "Reporter", die in den Ergebnissen von Get-AzVMGuestPolicyStatus nach initiativ-oder initiativ Name zu finden ist (Weitere Beispiele finden Sie hier)</span><span class="sxs-lookup"><span data-stu-id="f58b4-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="f58b4-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="f58b4-129">PARAMETERS</span></span>

### <span data-ttu-id="f58b4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f58b4-130">-DefaultProfile</span></span>
<span data-ttu-id="f58b4-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f58b4-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f58b4-132">-Initiativ-Nr.</span><span class="sxs-lookup"><span data-stu-id="f58b4-132">-InitiativeId</span></span>
<span data-ttu-id="f58b4-133">Definitions-ID einer Richtlinie, bei der der Definitions Initiative und Kategorie ist Gast Konfiguration ist</span><span class="sxs-lookup"><span data-stu-id="f58b4-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="f58b4-134">-Initiativname</span><span class="sxs-lookup"><span data-stu-id="f58b4-134">-InitiativeName</span></span>
<span data-ttu-id="f58b4-135">Name einer Richtlinie, bei der der Definitions "Initiative" und "Kategorie" Gast Konfiguration ist</span><span class="sxs-lookup"><span data-stu-id="f58b4-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="f58b4-136">-Berichts-Nr</span><span class="sxs-lookup"><span data-stu-id="f58b4-136">-ReportId</span></span>
<span data-ttu-id="f58b4-137">Die ID eines Gast Konfigurationsrichtlinien Status.</span><span class="sxs-lookup"><span data-stu-id="f58b4-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="f58b4-138">Eine Richtlinie, bei der der Definitions Initiative und Kategorie ist, muss einem Bereich zugewiesen werden, um Status zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f58b4-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

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

### <span data-ttu-id="f58b4-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f58b4-139">-ResourceGroupName</span></span>
<span data-ttu-id="f58b4-140">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f58b4-140">Resource group name.</span></span>

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

### <span data-ttu-id="f58b4-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="f58b4-141">-VMName</span></span>
<span data-ttu-id="f58b4-142">VM-Name.</span><span class="sxs-lookup"><span data-stu-id="f58b4-142">VM name.</span></span>

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

### <span data-ttu-id="f58b4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f58b4-143">CommonParameters</span></span>
<span data-ttu-id="f58b4-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f58b4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f58b4-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f58b4-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f58b4-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f58b4-146">INPUTS</span></span>

### <span data-ttu-id="f58b4-147">Keine</span><span class="sxs-lookup"><span data-stu-id="f58b4-147">None</span></span>
## <span data-ttu-id="f58b4-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f58b4-148">OUTPUTS</span></span>

### <span data-ttu-id="f58b4-149">Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="f58b4-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="f58b4-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="f58b4-150">NOTES</span></span>

## <span data-ttu-id="f58b4-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f58b4-151">RELATED LINKS</span></span>
