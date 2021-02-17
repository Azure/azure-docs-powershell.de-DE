---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: c98270b4e69d80e18ba721de0a6379d40d21fc75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156356"
---
# <span data-ttu-id="f00b1-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="f00b1-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="f00b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f00b1-102">SYNOPSIS</span></span>
<span data-ttu-id="f00b1-103">Aktualisieren eines Vorfalls</span><span class="sxs-lookup"><span data-stu-id="f00b1-103">Update an Incident.</span></span>

## <span data-ttu-id="f00b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f00b1-104">SYNTAX</span></span>

### <span data-ttu-id="f00b1-105">IncidentId (Standard)</span><span class="sxs-lookup"><span data-stu-id="f00b1-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f00b1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f00b1-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f00b1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f00b1-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f00b1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f00b1-108">DESCRIPTION</span></span>
<span data-ttu-id="f00b1-109">Das **Cmdlet "Update-AzSentinelIncident"** aktualisiert den Vorfall im angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="f00b1-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="f00b1-110">Sie können  ein Vorfallobjekt als Parameter oder mithilfe des Pipelineoperators übergeben, oder Sie können die erforderlichen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f00b1-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="f00b1-111">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f00b1-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="f00b1-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f00b1-112">EXAMPLES</span></span>

### <span data-ttu-id="f00b1-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f00b1-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="f00b1-114">Der Befehl ruft den Vorfall nach *IncidentId ab* und legt die *Schweregradeigenschaft* auf *"Hoch" fest.*</span><span class="sxs-lookup"><span data-stu-id="f00b1-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="f00b1-115">Alle anderen Eigenschaften bleiben gleich.</span><span class="sxs-lookup"><span data-stu-id="f00b1-115">All other properties remain the same.</span></span>

## <span data-ttu-id="f00b1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f00b1-116">PARAMETERS</span></span>

### <span data-ttu-id="f00b1-117">-Classification</span><span class="sxs-lookup"><span data-stu-id="f00b1-117">-Classification</span></span>
<span data-ttu-id="f00b1-118">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="f00b1-118">Incident Classificaiton.</span></span>

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

### <span data-ttu-id="f00b1-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="f00b1-119">-ClassificationComment</span></span>
<span data-ttu-id="f00b1-120">Incident Classificaiton Comment.</span><span class="sxs-lookup"><span data-stu-id="f00b1-120">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="f00b1-121">-Classification 2010</span><span class="sxs-lookup"><span data-stu-id="f00b1-121">-ClassificationReason</span></span>
<span data-ttu-id="f00b1-122">Incident Classificaiton Reason.</span><span class="sxs-lookup"><span data-stu-id="f00b1-122">Incident Classificaiton Reason.</span></span>

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

### <span data-ttu-id="f00b1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f00b1-123">-DefaultProfile</span></span>
<span data-ttu-id="f00b1-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f00b1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f00b1-125">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f00b1-125">-Description</span></span>
<span data-ttu-id="f00b1-126">Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="f00b1-126">Description.</span></span>

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

### <span data-ttu-id="f00b1-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="f00b1-127">-IncidentID</span></span>
<span data-ttu-id="f00b1-128">Vorfall-ID.</span><span class="sxs-lookup"><span data-stu-id="f00b1-128">Incident Id.</span></span>

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

### <span data-ttu-id="f00b1-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f00b1-129">-InputObject</span></span>
<span data-ttu-id="f00b1-130">InputObject.</span><span class="sxs-lookup"><span data-stu-id="f00b1-130">InputObject.</span></span>

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

### <span data-ttu-id="f00b1-131">-Label</span><span class="sxs-lookup"><span data-stu-id="f00b1-131">-Label</span></span>
<span data-ttu-id="f00b1-132">Vorfallbeschriftungen.</span><span class="sxs-lookup"><span data-stu-id="f00b1-132">Incident Labels.</span></span>

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

### <span data-ttu-id="f00b1-133">-Owner</span><span class="sxs-lookup"><span data-stu-id="f00b1-133">-Owner</span></span>
<span data-ttu-id="f00b1-134">Vorfallbesitzer.</span><span class="sxs-lookup"><span data-stu-id="f00b1-134">Incident Owner.</span></span>

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

### <span data-ttu-id="f00b1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f00b1-135">-ResourceGroupName</span></span>
<span data-ttu-id="f00b1-136">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f00b1-136">Resource group name.</span></span>

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

### <span data-ttu-id="f00b1-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f00b1-137">-ResourceId</span></span>
<span data-ttu-id="f00b1-138">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f00b1-138">Resource Id.</span></span>

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

### <span data-ttu-id="f00b1-139">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="f00b1-139">-Severity</span></span>
<span data-ttu-id="f00b1-140">Schweregrad des Vorfalls.</span><span class="sxs-lookup"><span data-stu-id="f00b1-140">Incident Severity.</span></span>

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

### <span data-ttu-id="f00b1-141">-Status</span><span class="sxs-lookup"><span data-stu-id="f00b1-141">-Status</span></span>
<span data-ttu-id="f00b1-142">Vorfallstatus.</span><span class="sxs-lookup"><span data-stu-id="f00b1-142">Incident Status.</span></span>

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

### <span data-ttu-id="f00b1-143">-Title</span><span class="sxs-lookup"><span data-stu-id="f00b1-143">-Title</span></span>
<span data-ttu-id="f00b1-144">Vorfalltitel.</span><span class="sxs-lookup"><span data-stu-id="f00b1-144">Incident Title.</span></span>

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

### <span data-ttu-id="f00b1-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f00b1-145">-WorkspaceName</span></span>
<span data-ttu-id="f00b1-146">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="f00b1-146">Workspace Name.</span></span>

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

### <span data-ttu-id="f00b1-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f00b1-147">-Confirm</span></span>
<span data-ttu-id="f00b1-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f00b1-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f00b1-149">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f00b1-149">-WhatIf</span></span>
<span data-ttu-id="f00b1-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f00b1-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f00b1-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f00b1-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f00b1-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00b1-152">CommonParameters</span></span>
<span data-ttu-id="f00b1-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f00b1-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f00b1-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f00b1-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00b1-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f00b1-155">INPUTS</span></span>

### <span data-ttu-id="f00b1-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="f00b1-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="f00b1-157">System.String</span><span class="sxs-lookup"><span data-stu-id="f00b1-157">System.String</span></span>

### <span data-ttu-id="f00b1-158">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f00b1-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f00b1-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="f00b1-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="f00b1-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f00b1-160">OUTPUTS</span></span>

### <span data-ttu-id="f00b1-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="f00b1-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="f00b1-162">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f00b1-162">NOTES</span></span>

## <span data-ttu-id="f00b1-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f00b1-163">RELATED LINKS</span></span>
