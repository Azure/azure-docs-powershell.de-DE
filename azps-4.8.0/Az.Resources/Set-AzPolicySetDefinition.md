---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: cd8bc24a0cedac91ef18e19a80e1662fdcbac297
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166109"
---
# <span data-ttu-id="f9316-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f9316-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="f9316-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9316-102">SYNOPSIS</span></span>
<span data-ttu-id="f9316-103">Ändert eine Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="f9316-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="f9316-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9316-104">SYNTAX</span></span>

### <span data-ttu-id="f9316-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f9316-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9316-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9316-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9316-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9316-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9316-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9316-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9316-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9316-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9316-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9316-110">DESCRIPTION</span></span>
<span data-ttu-id="f9316-111">Das Cmdlet " **Satz-AzPolicySetDefinition** " ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="f9316-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="f9316-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9316-112">EXAMPLES</span></span>

### <span data-ttu-id="f9316-113">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="f9316-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="f9316-114">Der erste Befehl ruft eine Richtliniensatz Definition mithilfe des Get-AzPolicySetDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="f9316-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="f9316-115">Der Befehl speichert das Objekt in der $PolicySetDefinition Variablen.</span><span class="sxs-lookup"><span data-stu-id="f9316-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="f9316-116">Mit dem zweiten Befehl wird die Beschreibung der Richtliniensatz Definition aktualisiert, die durch die Eigenschaft " **Resourcen** " von $PolicySetDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="f9316-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="f9316-117">Beispiel 2: Aktualisieren der Metadaten einer Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="f9316-117">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="f9316-118">Dieser Befehl aktualisiert die Metadaten einer Richtliniensatz Definition mit dem Namen VMPolicySetDefinition, um anzugeben, dass die Kategorie "virtueller Computer" lautet.</span><span class="sxs-lookup"><span data-stu-id="f9316-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="f9316-119">Beispiel 3: Aktualisieren der Gruppen einer Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="f9316-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="f9316-120">Mit diesem Befehl werden die Gruppen einer Richtliniensatz Definition mit dem Namen VMPolicySetDefinition aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f9316-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="f9316-121">Beispiel 4: Aktualisieren der Gruppen einer Richtliniensatz Definition mithilfe einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="f9316-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="f9316-122">Dieser Befehl aktualisiert die Gruppen einer Richtliniensatz Definition mit dem Namen VMPolicySetDefinition mithilfe einer Hashtabelle, um die Gruppen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f9316-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="f9316-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9316-123">PARAMETERS</span></span>

### <span data-ttu-id="f9316-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f9316-124">-ApiVersion</span></span>
<span data-ttu-id="f9316-125">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9316-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f9316-126">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f9316-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f9316-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9316-127">-DefaultProfile</span></span>
<span data-ttu-id="f9316-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f9316-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9316-129">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9316-129">-Description</span></span>
<span data-ttu-id="f9316-130">Die Beschreibung für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="f9316-130">The description for policy set definition.</span></span>

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

### <span data-ttu-id="f9316-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f9316-131">-DisplayName</span></span>
<span data-ttu-id="f9316-132">Der Anzeigename für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="f9316-132">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="f9316-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="f9316-133">-GroupDefinition</span></span>
<span data-ttu-id="f9316-134">Die Richtlinien Definitionsgruppen der aktualisierten Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="f9316-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="f9316-135">Dies kann entweder ein Pfad zu einer Datei sein, die die Gruppen enthält, oder die Gruppen als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f9316-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="f9316-136">-ID</span><span class="sxs-lookup"><span data-stu-id="f9316-136">-Id</span></span>
<span data-ttu-id="f9316-137">Die vollqualifizierte Richtlinien Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="f9316-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="f9316-138">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="f9316-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="f9316-139">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9316-139">-InputObject</span></span>
<span data-ttu-id="f9316-140">Das zu aktualisierbare Richtliniensatz-Definitionsobjekt, das von einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f9316-140">The policy set definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="f9316-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f9316-141">-ManagementGroupName</span></span>
<span data-ttu-id="f9316-142">Der Name der Verwaltungsgruppe der Richtliniensatz Definition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9316-142">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="f9316-143">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="f9316-143">-Metadata</span></span>
<span data-ttu-id="f9316-144">Die Metadaten der aktualisierten Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="f9316-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="f9316-145">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f9316-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="f9316-146">-Name</span><span class="sxs-lookup"><span data-stu-id="f9316-146">-Name</span></span>
<span data-ttu-id="f9316-147">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="f9316-147">The policy set definition name.</span></span>

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

### <span data-ttu-id="f9316-148">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f9316-148">-Parameter</span></span>
<span data-ttu-id="f9316-149">Die Parameters-Deklaration der aktualisierten Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="f9316-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="f9316-150">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f9316-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="f9316-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f9316-151">-PolicyDefinition</span></span>
<span data-ttu-id="f9316-152">Die Richtlinien Definitionen.</span><span class="sxs-lookup"><span data-stu-id="f9316-152">The policy definitions.</span></span> <span data-ttu-id="f9316-153">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Richtlinien Definitionen enthält, oder die Richtlinien Definitionen als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f9316-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="f9316-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="f9316-154">-Pre</span></span>
<span data-ttu-id="f9316-155">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="f9316-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f9316-156">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f9316-156">-SubscriptionId</span></span>
<span data-ttu-id="f9316-157">Die Abonnement-ID der Richtliniensatz Definition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9316-157">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="f9316-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9316-158">-Confirm</span></span>
<span data-ttu-id="f9316-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9316-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9316-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9316-160">-WhatIf</span></span>
<span data-ttu-id="f9316-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9316-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9316-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9316-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9316-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9316-163">CommonParameters</span></span>
<span data-ttu-id="f9316-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9316-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9316-165">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9316-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9316-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9316-166">INPUTS</span></span>

### <span data-ttu-id="f9316-167">System. String</span><span class="sxs-lookup"><span data-stu-id="f9316-167">System.String</span></span>

### <span data-ttu-id="f9316-168">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f9316-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f9316-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9316-169">OUTPUTS</span></span>

### <span data-ttu-id="f9316-170">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f9316-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f9316-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9316-171">NOTES</span></span>

## <span data-ttu-id="f9316-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9316-172">RELATED LINKS</span></span>
