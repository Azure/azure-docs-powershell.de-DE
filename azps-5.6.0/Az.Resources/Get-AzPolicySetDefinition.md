---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 9ea6f37d21d35736116b2e9bf4fc3fcf20becf10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929392"
---
# <span data-ttu-id="9c3c9-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="9c3c9-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="9c3c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="9c3c9-103">Ruft Richtliniensatzdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="9c3c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c3c9-104">SYNTAX</span></span>

### <span data-ttu-id="9c3c9-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9c3c9-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c3c9-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c3c9-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c3c9-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c3c9-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c3c9-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c3c9-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c3c9-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c3c9-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c3c9-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c3c9-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c3c9-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c3c9-111">DESCRIPTION</span></span>
<span data-ttu-id="9c3c9-112">Das **Get-AzPolicySetDefinition-Cmdlet** ruft eine Sammlung von Richtliniensatzdefinitionen oder eine bestimmte Richtliniensatzdefinition ab, die durch Name oder ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="9c3c9-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9c3c9-113">EXAMPLES</span></span>

### <span data-ttu-id="9c3c9-114">Beispiel 1: Alle Richtliniensatzdefinitionen erhalten</span><span class="sxs-lookup"><span data-stu-id="9c3c9-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="9c3c9-115">Dieser Befehl ruft alle Richtliniensatzdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="9c3c9-116">Beispiel 2: Holen Sie sich die Richtliniensatzdefinition aus dem aktuellen Abonnement nach Name</span><span class="sxs-lookup"><span data-stu-id="9c3c9-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="9c3c9-117">Dieser Befehl ruft die Richtliniensatzdefinition mit dem Namen VMPolicySetDefinition aus dem aktuellen Standardabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="9c3c9-118">Beispiel 3: Holen Sie sich die Definition des Richtliniensatzs aus dem Abonnement nach Name.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="9c3c9-119">Dieser Befehl ruft die Richtliniendefinition vmPolicySetDefinition aus dem Abonnement mit der ID 3bf44b72-c631-427a-b8c8-53e2595398ca ab.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="9c3c9-120">Beispiel 4: Alle benutzerdefinierten Richtliniensatzdefinitionen aus der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="9c3c9-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="9c3c9-121">Dieser Befehl ruft alle benutzerdefinierten Richtliniensatzdefinitionen aus der Verwaltungsgruppe mit dem Namen Dept42 ab.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="9c3c9-122">Beispiel 5: Erhalten von Richtliniensatzdefinitionen aus einer bestimmten Kategorie</span><span class="sxs-lookup"><span data-stu-id="9c3c9-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="9c3c9-123">Dieser Befehl ruft alle Richtliniensatzdefinitionen in der Kategorie "Virtueller Computer" ab.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="9c3c9-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9c3c9-124">PARAMETERS</span></span>

### <span data-ttu-id="9c3c9-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9c3c9-125">-ApiVersion</span></span>
<span data-ttu-id="9c3c9-126">Wenn festgelegt, gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9c3c9-127">Wenn nicht angegeben, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9c3c9-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="9c3c9-128">-Builtin</span></span>
<span data-ttu-id="9c3c9-129">Beschränkt die Ergebnisliste auf nur integrierte Richtliniensatzdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-129">Limits list of results to only built-in policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c3c9-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="9c3c9-130">-Custom</span></span>
<span data-ttu-id="9c3c9-131">Beschränkt die Ergebnisliste auf benutzerdefinierte Richtliniensatzdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-131">Limits list of results to only custom policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c3c9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c3c9-132">-DefaultProfile</span></span>
<span data-ttu-id="9c3c9-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9c3c9-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c3c9-134">-ID</span><span class="sxs-lookup"><span data-stu-id="9c3c9-134">-Id</span></span>
<span data-ttu-id="9c3c9-135">Die vollqualifizierte Richtliniensatzdefinitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="9c3c9-136">z. B. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="9c3c9-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="9c3c9-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="9c3c9-137">-ManagementGroupName</span></span>
<span data-ttu-id="9c3c9-138">Der Name der Verwaltungsgruppe der zu erhaltende Richtliniensatzdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3c9-139">-Name</span><span class="sxs-lookup"><span data-stu-id="9c3c9-139">-Name</span></span>
<span data-ttu-id="9c3c9-140">Der Definitionsname des Richtliniensatzs.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-140">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3c9-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="9c3c9-141">-Pre</span></span>
<span data-ttu-id="9c3c9-142">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9c3c9-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c3c9-143">-SubscriptionId</span></span>
<span data-ttu-id="9c3c9-144">Die Abonnement-ID der zu erhaltende Richtliniensatzdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3c9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c3c9-145">CommonParameters</span></span>
<span data-ttu-id="9c3c9-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c3c9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c3c9-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c3c9-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c3c9-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9c3c9-148">INPUTS</span></span>

### <span data-ttu-id="9c3c9-149">System.String</span><span class="sxs-lookup"><span data-stu-id="9c3c9-149">System.String</span></span>

### <span data-ttu-id="9c3c9-150">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9c3c9-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9c3c9-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9c3c9-151">OUTPUTS</span></span>

### <span data-ttu-id="9c3c9-152">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="9c3c9-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9c3c9-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9c3c9-153">NOTES</span></span>

## <span data-ttu-id="9c3c9-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9c3c9-154">RELATED LINKS</span></span>
