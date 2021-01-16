---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 551e30077fe1ce836f98c18d3c00976adc779f64
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301624"
---
# <span data-ttu-id="aef82-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="aef82-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="aef82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aef82-102">SYNOPSIS</span></span>
<span data-ttu-id="aef82-103">Entfernt eine Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="aef82-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="aef82-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aef82-104">SYNTAX</span></span>

### <span data-ttu-id="aef82-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aef82-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aef82-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aef82-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aef82-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aef82-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aef82-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aef82-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aef82-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aef82-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aef82-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aef82-110">DESCRIPTION</span></span>
<span data-ttu-id="aef82-111">Das **Cmdlet "Remove-AzPolicySetDefinition"** entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="aef82-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="aef82-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aef82-112">EXAMPLES</span></span>

### <span data-ttu-id="aef82-113">Beispiel 1: Entfernen der Richtliniensatzdefinition nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="aef82-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="aef82-114">Der erste Befehl ruft eine Richtliniensatzdefinition mithilfe des cmdlets Get-AzPolicySetDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="aef82-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="aef82-115">Der Befehl speichert sie in der $PolicySetDefinition Variable.</span><span class="sxs-lookup"><span data-stu-id="aef82-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="aef82-116">Mit dem zweiten Befehl wird die definition des Richtliniensatzs entfernt, die durch die **Eigenschaft "ResourceId"** des $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="aef82-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="aef82-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aef82-117">PARAMETERS</span></span>

### <span data-ttu-id="aef82-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aef82-118">-ApiVersion</span></span>
<span data-ttu-id="aef82-119">Gibt im festgelegten Satz die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="aef82-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="aef82-120">Wenn keine Angabe erfolgt, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="aef82-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="aef82-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef82-121">-DefaultProfile</span></span>
<span data-ttu-id="aef82-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aef82-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aef82-123">-Force</span><span class="sxs-lookup"><span data-stu-id="aef82-123">-Force</span></span>
<span data-ttu-id="aef82-124">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="aef82-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="aef82-125">-ID</span><span class="sxs-lookup"><span data-stu-id="aef82-125">-Id</span></span>
<span data-ttu-id="aef82-126">Die vollqualifizierte Definitions-ID des Richtliniensets, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="aef82-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="aef82-127">z. B. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="aef82-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef82-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aef82-128">-InputObject</span></span>
<span data-ttu-id="aef82-129">Das zu entfernende Richtliniensatzdefinitionsobjekt, das von einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="aef82-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aef82-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="aef82-130">-ManagementGroupName</span></span>
<span data-ttu-id="aef82-131">Der Name der Verwaltungsgruppe der zu löschende Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="aef82-131">The name of the management group of the policy set definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef82-132">-Name</span><span class="sxs-lookup"><span data-stu-id="aef82-132">-Name</span></span>
<span data-ttu-id="aef82-133">Der Name der Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="aef82-133">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef82-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="aef82-134">-Pre</span></span>
<span data-ttu-id="aef82-135">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aef82-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="aef82-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aef82-136">-SubscriptionId</span></span>
<span data-ttu-id="aef82-137">Die Abonnement-ID der zu löschende Definition des Richtliniensets.</span><span class="sxs-lookup"><span data-stu-id="aef82-137">The subscription ID of the policy set definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef82-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aef82-138">-Confirm</span></span>
<span data-ttu-id="aef82-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aef82-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aef82-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aef82-140">-WhatIf</span></span>
<span data-ttu-id="aef82-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aef82-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aef82-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aef82-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aef82-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef82-143">CommonParameters</span></span>
<span data-ttu-id="aef82-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aef82-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef82-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aef82-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef82-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aef82-146">INPUTS</span></span>

### <span data-ttu-id="aef82-147">System.String</span><span class="sxs-lookup"><span data-stu-id="aef82-147">System.String</span></span>

### <span data-ttu-id="aef82-148">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aef82-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="aef82-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aef82-149">OUTPUTS</span></span>

### <span data-ttu-id="aef82-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aef82-150">System.Boolean</span></span>

## <span data-ttu-id="aef82-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aef82-151">NOTES</span></span>

## <span data-ttu-id="aef82-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aef82-152">RELATED LINKS</span></span>
