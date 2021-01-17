---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 9dfb3ff2f50df7a858ab8194ec86fa312501dcff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372461"
---
# <span data-ttu-id="49818-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="49818-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="49818-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49818-102">SYNOPSIS</span></span>
<span data-ttu-id="49818-103">Bricht eine in Bearbeitung ausgeführte Richtlinienbehebung ab.</span><span class="sxs-lookup"><span data-stu-id="49818-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="49818-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49818-104">SYNTAX</span></span>

### <span data-ttu-id="49818-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="49818-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49818-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="49818-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49818-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="49818-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49818-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49818-108">DESCRIPTION</span></span>
<span data-ttu-id="49818-109">Das **Cmdlet "Stop-AzPolicyRemediation"** bricht eine in Bearbeitung ausgeführte Richtlinienbehebung ab.</span><span class="sxs-lookup"><span data-stu-id="49818-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="49818-110">Aktive Bereitstellungen werden abgebrochen, und es werden keine neuen Bereitstellungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="49818-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="49818-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="49818-111">EXAMPLES</span></span>

### <span data-ttu-id="49818-112">Beispiel 1: Abbrechen einer Richtlinienbehebung im Bereich "Ressourcengruppe"</span><span class="sxs-lookup"><span data-stu-id="49818-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="49818-113">Dieser Befehl bricht die Wartung mit dem Namen "remediation1" in der Ressourcengruppe "myRG" ab.</span><span class="sxs-lookup"><span data-stu-id="49818-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="49818-114">Beispiel 2: Abbrechen der Wartung einer Verwaltungsgruppe über Piping</span><span class="sxs-lookup"><span data-stu-id="49818-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="49818-115">Dieser Befehl bricht die Wartung namens "remediation1" in der Verwaltungsgruppe "mg1" ab.</span><span class="sxs-lookup"><span data-stu-id="49818-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="49818-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49818-116">PARAMETERS</span></span>

### <span data-ttu-id="49818-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49818-117">-AsJob</span></span>
<span data-ttu-id="49818-118">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="49818-118">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49818-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49818-119">-DefaultProfile</span></span>
<span data-ttu-id="49818-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49818-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49818-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49818-121">-InputObject</span></span>
<span data-ttu-id="49818-122">Das Problembehebungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="49818-122">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49818-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="49818-123">-ManagementGroupName</span></span>
<span data-ttu-id="49818-124">ID der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="49818-124">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49818-125">-Name</span><span class="sxs-lookup"><span data-stu-id="49818-125">-Name</span></span>
<span data-ttu-id="49818-126">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="49818-126">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49818-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49818-127">-PassThru</span></span>
<span data-ttu-id="49818-128">Gibt "True" zurück, wenn der Befehl erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="49818-128">Return True if the command completes successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49818-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49818-129">-ResourceGroupName</span></span>
<span data-ttu-id="49818-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="49818-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49818-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49818-131">-ResourceId</span></span>
<span data-ttu-id="49818-132">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="49818-132">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49818-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="49818-133">-Scope</span></span>
<span data-ttu-id="49818-134">Umfang der Ressource.</span><span class="sxs-lookup"><span data-stu-id="49818-134">Scope of the resource.</span></span>
<span data-ttu-id="49818-135">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="49818-135">E.g.</span></span>
<span data-ttu-id="49818-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="49818-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49818-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49818-137">-Confirm</span></span>
<span data-ttu-id="49818-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49818-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49818-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="49818-139">-WhatIf</span></span>
<span data-ttu-id="49818-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49818-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49818-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49818-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49818-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49818-142">CommonParameters</span></span>
<span data-ttu-id="49818-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49818-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49818-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49818-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49818-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="49818-145">INPUTS</span></span>

### <span data-ttu-id="49818-146">System.String</span><span class="sxs-lookup"><span data-stu-id="49818-146">System.String</span></span>

### <span data-ttu-id="49818-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="49818-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="49818-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="49818-148">OUTPUTS</span></span>

### <span data-ttu-id="49818-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49818-149">System.Boolean</span></span>

## <span data-ttu-id="49818-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="49818-150">NOTES</span></span>

## <span data-ttu-id="49818-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="49818-151">RELATED LINKS</span></span>
