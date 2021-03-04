---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: 03062015b1f9d14688488887ed226f1b697589ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950611"
---
# <span data-ttu-id="1b1c8-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="1b1c8-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="1b1c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b1c8-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1c8-103">Aktualisieren eines Vorfalls</span><span class="sxs-lookup"><span data-stu-id="1b1c8-103">Update an Incident.</span></span>

## <span data-ttu-id="1b1c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b1c8-104">SYNTAX</span></span>

### <span data-ttu-id="1b1c8-105">IncidentId (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b1c8-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b1c8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1b1c8-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b1c8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b1c8-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b1c8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b1c8-108">DESCRIPTION</span></span>
<span data-ttu-id="1b1c8-109">Das **Cmdlet Update-AzSentinelIncident** aktualisiert den Vorfall im angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="1b1c8-110">Sie können ein **Incident-Objekt** als Parameter oder mithilfe des Pipelineoperators übergeben oder alternativ die erforderlichen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="1b1c8-111">Sie können den Parameter *Bestätigen* und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="1b1c8-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b1c8-112">EXAMPLES</span></span>

### <span data-ttu-id="1b1c8-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1b1c8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="1b1c8-114">Der Befehl ruft die Incident by *IncidentId ab* und legt *die Schweregrad-Eigenschaft* auf *Hoch fest.*</span><span class="sxs-lookup"><span data-stu-id="1b1c8-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="1b1c8-115">Alle anderen Eigenschaften bleiben gleich.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-115">All other properties remain the same.</span></span>

## <span data-ttu-id="1b1c8-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1b1c8-116">PARAMETERS</span></span>

### <span data-ttu-id="1b1c8-117">-Classification</span><span class="sxs-lookup"><span data-stu-id="1b1c8-117">-Classification</span></span>
<span data-ttu-id="1b1c8-118">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-118">Incident Classificaiton.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="1b1c8-119">-ClassificationComment</span></span>
<span data-ttu-id="1b1c8-120">Incident Classificaiton Comment.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-120">Incident Classificaiton Comment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="1b1c8-121">-ClassificationReason</span></span>
<span data-ttu-id="1b1c8-122">Incident Classificaiton Reason.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-122">Incident Classificaiton Reason.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1c8-123">-DefaultProfile</span></span>
<span data-ttu-id="1b1c8-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-125">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b1c8-125">-Description</span></span>
<span data-ttu-id="1b1c8-126">Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-126">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="1b1c8-127">-IncidentID</span></span>
<span data-ttu-id="1b1c8-128">Vorfall-ID.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-128">Incident Id.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId, ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b1c8-129">-InputObject</span></span>
<span data-ttu-id="1b1c8-130">InputObject.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-130">InputObject.</span></span>

```yaml
Type: PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-131">-Label</span><span class="sxs-lookup"><span data-stu-id="1b1c8-131">-Label</span></span>
<span data-ttu-id="1b1c8-132">Vorfallbeschriftungen.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-132">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-133">-Besitzer</span><span class="sxs-lookup"><span data-stu-id="1b1c8-133">-Owner</span></span>
<span data-ttu-id="1b1c8-134">Vorfallbesitzer.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-134">Incident Owner.</span></span>

```yaml
Type: PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b1c8-135">-ResourceGroupName</span></span>
<span data-ttu-id="1b1c8-136">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b1c8-137">-ResourceId</span></span>
<span data-ttu-id="1b1c8-138">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-139">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="1b1c8-139">-Severity</span></span>
<span data-ttu-id="1b1c8-140">Schweregrad des Vorfalls.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-140">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-141">-Status</span><span class="sxs-lookup"><span data-stu-id="1b1c8-141">-Status</span></span>
<span data-ttu-id="1b1c8-142">Vorfallstatus.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-142">Incident Status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-143">-Title</span><span class="sxs-lookup"><span data-stu-id="1b1c8-143">-Title</span></span>
<span data-ttu-id="1b1c8-144">Vorfalltitel.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-144">Incident Title.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1b1c8-145">-WorkspaceName</span></span>
<span data-ttu-id="1b1c8-146">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-146">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1b1c8-147">-Confirm</span></span>
<span data-ttu-id="1b1c8-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b1c8-149">-WhatIf</span></span>
<span data-ttu-id="1b1c8-150">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b1c8-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1c8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1c8-152">CommonParameters</span></span>
<span data-ttu-id="1b1c8-153">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b1c8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1c8-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b1c8-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1c8-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b1c8-155">INPUTS</span></span>

### <span data-ttu-id="1b1c8-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="1b1c8-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="1b1c8-157">System.String</span><span class="sxs-lookup"><span data-stu-id="1b1c8-157">System.String</span></span>

### <span data-ttu-id="1b1c8-158">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="1b1c8-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1b1c8-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="1b1c8-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="1b1c8-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b1c8-160">OUTPUTS</span></span>

### <span data-ttu-id="1b1c8-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="1b1c8-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="1b1c8-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1b1c8-162">NOTES</span></span>

## <span data-ttu-id="1b1c8-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1b1c8-163">RELATED LINKS</span></span>
