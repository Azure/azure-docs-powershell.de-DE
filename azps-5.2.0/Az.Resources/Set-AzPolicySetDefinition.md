---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: cd8bc24a0cedac91ef18e19a80e1662fdcbac297
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305611"
---
# <span data-ttu-id="4b822-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="4b822-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="4b822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b822-102">SYNOPSIS</span></span>
<span data-ttu-id="4b822-103">Ändert die Definition eines Richtliniensets</span><span class="sxs-lookup"><span data-stu-id="4b822-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="4b822-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b822-104">SYNTAX</span></span>

### <span data-ttu-id="4b822-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b822-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b822-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b822-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b822-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b822-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b822-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b822-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b822-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b822-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b822-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b822-110">DESCRIPTION</span></span>
<span data-ttu-id="4b822-111">Das **Cmdlet "Set-AzPolicySetDefinition"** ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="4b822-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="4b822-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b822-112">EXAMPLES</span></span>

### <span data-ttu-id="4b822-113">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniensatzdefinition</span><span class="sxs-lookup"><span data-stu-id="4b822-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="4b822-114">Der erste Befehl ruft eine Richtliniensatzdefinition mithilfe des cmdlets Get-AzPolicySetDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="4b822-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="4b822-115">Der Befehl speichert dieses Objekt in der $PolicySetDefinition Variable.</span><span class="sxs-lookup"><span data-stu-id="4b822-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="4b822-116">Mit dem zweiten Befehl wird die Beschreibung der Richtliniensatzdefinition aktualisiert, die durch die **Eigenschaft "ResourceId"** des $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="4b822-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="4b822-117">Beispiel 2: Aktualisieren der Metadaten einer Richtliniensatzdefinition</span><span class="sxs-lookup"><span data-stu-id="4b822-117">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="4b822-118">Dieser Befehl aktualisiert die Metadaten einer Richtliniensatzdefinition namens VMPolicySetDefinition, um anzugeben, dass die Kategorie "Virtual Machine" ist.</span><span class="sxs-lookup"><span data-stu-id="4b822-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="4b822-119">Beispiel 3: Aktualisieren der Gruppen einer Richtliniensatzdefinition</span><span class="sxs-lookup"><span data-stu-id="4b822-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="4b822-120">Dieser Befehl aktualisiert die Gruppen einer Richtliniensatzdefinition namens VMPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="4b822-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="4b822-121">Beispiel 4: Aktualisieren der Gruppen einer Richtliniensatzdefinition mithilfe einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="4b822-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="4b822-122">Mit diesem Befehl werden die Gruppen einer Richtliniensatzdefinition namens VMPolicySetDefinition mit einer Hashtabelle aktualisiert, um die Gruppen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b822-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="4b822-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b822-123">PARAMETERS</span></span>

### <span data-ttu-id="4b822-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4b822-124">-ApiVersion</span></span>
<span data-ttu-id="4b822-125">Gibt im festgelegten Satz die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="4b822-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4b822-126">Wenn keine Angabe erfolgt, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4b822-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4b822-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b822-127">-DefaultProfile</span></span>
<span data-ttu-id="4b822-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4b822-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b822-129">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b822-129">-Description</span></span>
<span data-ttu-id="4b822-130">Die Beschreibung für die Definition des Richtliniensets.</span><span class="sxs-lookup"><span data-stu-id="4b822-130">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b822-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4b822-131">-DisplayName</span></span>
<span data-ttu-id="4b822-132">Der Anzeigename für die Definition des Richtliniensets.</span><span class="sxs-lookup"><span data-stu-id="4b822-132">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b822-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="4b822-133">-GroupDefinition</span></span>
<span data-ttu-id="4b822-134">Die Richtliniendefinitionsgruppen der aktualisierten Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="4b822-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="4b822-135">Dies kann entweder ein Pfad zu einer Datei sein, die die Gruppen enthält, oder die Gruppen als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4b822-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b822-136">-ID</span><span class="sxs-lookup"><span data-stu-id="4b822-136">-Id</span></span>
<span data-ttu-id="4b822-137">Die vollqualifizierte Richtliniendefinitions-ID einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="4b822-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="4b822-138">z. B. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="4b822-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="4b822-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b822-139">-InputObject</span></span>
<span data-ttu-id="4b822-140">Das zu aktualisierende Richtliniensatzdefinitionsobjekt, das von einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="4b822-140">The policy set definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="4b822-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4b822-141">-ManagementGroupName</span></span>
<span data-ttu-id="4b822-142">Der Name der Verwaltungsgruppe der zu aktualisierende Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="4b822-142">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="4b822-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4b822-143">-Metadata</span></span>
<span data-ttu-id="4b822-144">Die Metadaten der aktualisierten Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="4b822-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="4b822-145">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4b822-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b822-146">-Name</span><span class="sxs-lookup"><span data-stu-id="4b822-146">-Name</span></span>
<span data-ttu-id="4b822-147">Der Name der Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="4b822-147">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b822-148">-Parameter</span><span class="sxs-lookup"><span data-stu-id="4b822-148">-Parameter</span></span>
<span data-ttu-id="4b822-149">Die Parameterdeklaration der aktualisierten Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="4b822-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="4b822-150">Dies kann entweder ein Pfad zu einem Dateinamen oder URI mit der Parameterdeklaration oder die Parameterdeklaration als eine JSON-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="4b822-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b822-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4b822-151">-PolicyDefinition</span></span>
<span data-ttu-id="4b822-152">Die Richtliniendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4b822-152">The policy definitions.</span></span> <span data-ttu-id="4b822-153">Dies kann entweder ein Pfad zu einem Dateinamen mit den Richtliniendefinitionen oder die Richtliniendefinitionen als eine JSON-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="4b822-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b822-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="4b822-154">-Pre</span></span>
<span data-ttu-id="4b822-155">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b822-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4b822-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b822-156">-SubscriptionId</span></span>
<span data-ttu-id="4b822-157">Die Abonnement-ID der zu aktualisierende Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="4b822-157">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="4b822-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b822-158">-Confirm</span></span>
<span data-ttu-id="4b822-159">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b822-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b822-160">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4b822-160">-WhatIf</span></span>
<span data-ttu-id="4b822-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b822-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b822-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b822-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b822-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b822-163">CommonParameters</span></span>
<span data-ttu-id="4b822-164">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b822-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b822-165">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b822-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b822-166">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b822-166">INPUTS</span></span>

### <span data-ttu-id="4b822-167">System.String</span><span class="sxs-lookup"><span data-stu-id="4b822-167">System.String</span></span>

### <span data-ttu-id="4b822-168">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4b822-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4b822-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b822-169">OUTPUTS</span></span>

### <span data-ttu-id="4b822-170">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="4b822-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4b822-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4b822-171">NOTES</span></span>

## <span data-ttu-id="4b822-172">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4b822-172">RELATED LINKS</span></span>
