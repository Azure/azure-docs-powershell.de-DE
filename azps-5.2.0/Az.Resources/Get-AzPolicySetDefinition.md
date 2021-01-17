---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356556"
---
# <span data-ttu-id="934c6-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="934c6-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="934c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="934c6-102">SYNOPSIS</span></span>
<span data-ttu-id="934c6-103">Ruft Richtliniensatzdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="934c6-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="934c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="934c6-104">SYNTAX</span></span>

### <span data-ttu-id="934c6-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="934c6-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="934c6-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="934c6-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="934c6-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="934c6-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="934c6-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="934c6-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="934c6-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="934c6-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="934c6-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="934c6-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="934c6-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="934c6-111">DESCRIPTION</span></span>
<span data-ttu-id="934c6-112">Das **Cmdlet "Get-AzPolicySetDefinition"** ruft eine Sammlung von Richtliniensatzdefinitionen oder eine bestimmte, durch Name oder ID identifizierte Definition eines Richtliniensets ab.</span><span class="sxs-lookup"><span data-stu-id="934c6-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="934c6-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="934c6-113">EXAMPLES</span></span>

### <span data-ttu-id="934c6-114">Beispiel 1: Alle Richtliniensatzdefinitionen erhalten</span><span class="sxs-lookup"><span data-stu-id="934c6-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="934c6-115">Dieser Befehl ruft alle Richtliniensatzdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="934c6-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="934c6-116">Beispiel 2: Richtliniensatzdefinition aus dem aktuellen Abonnement nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="934c6-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="934c6-117">Dieser Befehl ruft die Richtliniensatzdefinition "VMPolicySetDefinition" aus dem aktuellen Standardabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="934c6-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="934c6-118">Beispiel 3: Richtliniensatzdefinition aus Abonnement nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="934c6-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="934c6-119">Dieser Befehl ruft die Richtliniendefinition "VMPolicySetDefinition" aus dem Abonnement mit id 3bf44b72-c631-427a-b8c8-53e2595398ca ab.</span><span class="sxs-lookup"><span data-stu-id="934c6-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="934c6-120">Beispiel 4: Alle benutzerdefinierten Richtliniensatzdefinitionen aus der Verwaltungsgruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="934c6-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="934c6-121">Dieser Befehl ruft alle benutzerdefinierten Richtliniensatzdefinitionen aus der Verwaltungsgruppe namens "Dept42" ab.</span><span class="sxs-lookup"><span data-stu-id="934c6-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="934c6-122">Beispiel 5: Erhalten von Richtliniensatzdefinitionen aus einer bestimmten Kategorie</span><span class="sxs-lookup"><span data-stu-id="934c6-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="934c6-123">Dieser Befehl ruft alle Richtliniensatzdefinitionen in der Kategorie "Virtual Machine" ab.</span><span class="sxs-lookup"><span data-stu-id="934c6-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="934c6-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="934c6-124">PARAMETERS</span></span>

### <span data-ttu-id="934c6-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="934c6-125">-ApiVersion</span></span>
<span data-ttu-id="934c6-126">Gibt im festgelegten Satz die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="934c6-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="934c6-127">Wenn keine Angabe erfolgt, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="934c6-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="934c6-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="934c6-128">-Builtin</span></span>
<span data-ttu-id="934c6-129">Beschränkt die Ergebnisliste auf integrierte Richtliniensatzdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="934c6-129">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="934c6-130">-Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="934c6-130">-Custom</span></span>
<span data-ttu-id="934c6-131">Beschränkt die Ergebnisliste auf benutzerdefinierte Richtliniensatzdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="934c6-131">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="934c6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="934c6-132">-DefaultProfile</span></span>
<span data-ttu-id="934c6-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="934c6-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="934c6-134">-ID</span><span class="sxs-lookup"><span data-stu-id="934c6-134">-Id</span></span>
<span data-ttu-id="934c6-135">Die vollqualifizierte Definitions-ID des Richtliniensets, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="934c6-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="934c6-136">z. B. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="934c6-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="934c6-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="934c6-137">-ManagementGroupName</span></span>
<span data-ttu-id="934c6-138">Der Name der Verwaltungsgruppe der zu erhaltende(n) Richtliniensatzdefinition(en).</span><span class="sxs-lookup"><span data-stu-id="934c6-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="934c6-139">-Name</span><span class="sxs-lookup"><span data-stu-id="934c6-139">-Name</span></span>
<span data-ttu-id="934c6-140">Der Name der Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="934c6-140">The policy set definition name.</span></span>

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

### <span data-ttu-id="934c6-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="934c6-141">-Pre</span></span>
<span data-ttu-id="934c6-142">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="934c6-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="934c6-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="934c6-143">-SubscriptionId</span></span>
<span data-ttu-id="934c6-144">Die Abonnement-ID der zu erhaltende(n) Richtliniensatzdefinition(en).</span><span class="sxs-lookup"><span data-stu-id="934c6-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="934c6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="934c6-145">CommonParameters</span></span>
<span data-ttu-id="934c6-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="934c6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="934c6-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="934c6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="934c6-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="934c6-148">INPUTS</span></span>

### <span data-ttu-id="934c6-149">System.String</span><span class="sxs-lookup"><span data-stu-id="934c6-149">System.String</span></span>

### <span data-ttu-id="934c6-150">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="934c6-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="934c6-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="934c6-151">OUTPUTS</span></span>

### <span data-ttu-id="934c6-152">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="934c6-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="934c6-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="934c6-153">NOTES</span></span>

## <span data-ttu-id="934c6-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="934c6-154">RELATED LINKS</span></span>
