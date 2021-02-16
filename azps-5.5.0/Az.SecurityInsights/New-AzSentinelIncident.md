---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: b3618f178ea5dee54991c037da78ac51f2ed4502
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168956"
---
# <span data-ttu-id="5b63c-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="5b63c-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="5b63c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b63c-102">SYNOPSIS</span></span>
<span data-ttu-id="5b63c-103">Erstellen eines Vorfalls</span><span class="sxs-lookup"><span data-stu-id="5b63c-103">Create an Incident.</span></span>

## <span data-ttu-id="5b63c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b63c-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b63c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b63c-105">DESCRIPTION</span></span>
<span data-ttu-id="5b63c-106">Das **Cmdlet "New-AzSentinelIncident"** erstellt einen Vorfall aus dem angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="5b63c-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="5b63c-107">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="5b63c-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="5b63c-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5b63c-108">EXAMPLES</span></span>

### <span data-ttu-id="5b63c-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b63c-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="5b63c-110">In diesem Beispiel wird ein **Vorfall** im angegebenen Arbeitsbereich erstellt und dann in der variablen $Incident gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5b63c-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="5b63c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b63c-111">PARAMETERS</span></span>

### <span data-ttu-id="5b63c-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="5b63c-112">-ClassificationComment</span></span>
<span data-ttu-id="5b63c-113">Incident Classificaiton Comment.</span><span class="sxs-lookup"><span data-stu-id="5b63c-113">Incident Classificaiton Comment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b63c-114">-Classification 2010</span><span class="sxs-lookup"><span data-stu-id="5b63c-114">-ClassificationReason</span></span>
<span data-ttu-id="5b63c-115">Incident Classificaiton Reason.</span><span class="sxs-lookup"><span data-stu-id="5b63c-115">Incident Classificaiton Reason.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b63c-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="5b63c-116">-Classificaton</span></span>
<span data-ttu-id="5b63c-117">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="5b63c-117">Incident Classificaiton.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b63c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b63c-118">-DefaultProfile</span></span>
<span data-ttu-id="5b63c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b63c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b63c-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b63c-120">-Description</span></span>
<span data-ttu-id="5b63c-121">Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="5b63c-121">Description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b63c-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="5b63c-122">-IncidentId</span></span>
<span data-ttu-id="5b63c-123">Vorfall-ID.</span><span class="sxs-lookup"><span data-stu-id="5b63c-123">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b63c-124">-Label</span><span class="sxs-lookup"><span data-stu-id="5b63c-124">-Label</span></span>
<span data-ttu-id="5b63c-125">Vorfallbeschriftungen.</span><span class="sxs-lookup"><span data-stu-id="5b63c-125">Incident Labels.</span></span>

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

### <span data-ttu-id="5b63c-126">-Owner</span><span class="sxs-lookup"><span data-stu-id="5b63c-126">-Owner</span></span>
<span data-ttu-id="5b63c-127">Vorfallbesitzer.</span><span class="sxs-lookup"><span data-stu-id="5b63c-127">Incident Owner.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b63c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b63c-128">-ResourceGroupName</span></span>
<span data-ttu-id="5b63c-129">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="5b63c-129">Resource group name.</span></span>

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

### <span data-ttu-id="5b63c-130">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="5b63c-130">-Severity</span></span>
<span data-ttu-id="5b63c-131">Schweregrad des Vorfalls.</span><span class="sxs-lookup"><span data-stu-id="5b63c-131">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b63c-132">-Status</span><span class="sxs-lookup"><span data-stu-id="5b63c-132">-Status</span></span>
<span data-ttu-id="5b63c-133">Vorfallstatus.</span><span class="sxs-lookup"><span data-stu-id="5b63c-133">Incident Status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b63c-134">-Title</span><span class="sxs-lookup"><span data-stu-id="5b63c-134">-Title</span></span>
<span data-ttu-id="5b63c-135">Vorfalltitel.</span><span class="sxs-lookup"><span data-stu-id="5b63c-135">Incident Title.</span></span>

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

### <span data-ttu-id="5b63c-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5b63c-136">-WorkspaceName</span></span>
<span data-ttu-id="5b63c-137">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="5b63c-137">Workspace Name.</span></span>

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

### <span data-ttu-id="5b63c-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b63c-138">-Confirm</span></span>
<span data-ttu-id="5b63c-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b63c-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b63c-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5b63c-140">-WhatIf</span></span>
<span data-ttu-id="5b63c-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b63c-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b63c-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b63c-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b63c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b63c-143">CommonParameters</span></span>
<span data-ttu-id="5b63c-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b63c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b63c-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b63c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b63c-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5b63c-146">INPUTS</span></span>

### <span data-ttu-id="5b63c-147">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="5b63c-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="5b63c-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="5b63c-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="5b63c-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5b63c-149">OUTPUTS</span></span>

### <span data-ttu-id="5b63c-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="5b63c-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="5b63c-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5b63c-151">NOTES</span></span>

## <span data-ttu-id="5b63c-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5b63c-152">RELATED LINKS</span></span>
