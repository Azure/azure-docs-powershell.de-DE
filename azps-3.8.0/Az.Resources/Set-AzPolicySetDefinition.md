---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 8a8559058b0bb5e1b33d93451bed35182a44783b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996436"
---
# <span data-ttu-id="15d6f-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="15d6f-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="15d6f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="15d6f-103">Ändert eine Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="15d6f-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="15d6f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15d6f-104">SYNTAX</span></span>

### <span data-ttu-id="15d6f-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="15d6f-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15d6f-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="15d6f-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15d6f-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15d6f-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15d6f-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15d6f-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15d6f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15d6f-109">DESCRIPTION</span></span>
<span data-ttu-id="15d6f-110">Das Cmdlet " **Satz-AzPolicySetDefinition** " ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="15d6f-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="15d6f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15d6f-111">EXAMPLES</span></span>

### <span data-ttu-id="15d6f-112">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="15d6f-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="15d6f-113">Der erste Befehl ruft eine Richtliniensatz Definition mithilfe des Get-AzPolicySetDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="15d6f-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="15d6f-114">Der Befehl speichert das Objekt in der $PolicySetDefinition Variablen.</span><span class="sxs-lookup"><span data-stu-id="15d6f-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="15d6f-115">Mit dem zweiten Befehl wird die Beschreibung der Richtliniensatz Definition aktualisiert, die durch die Eigenschaft " **Resourcen** " von $PolicySetDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="15d6f-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="15d6f-116">Beispiel 2: Aktualisieren der Metadaten einer Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="15d6f-116">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="15d6f-117">Dieser Befehl aktualisiert die Metadaten einer Richtliniensatz Definition mit dem Namen VMPolicySetDefinition, um anzugeben, dass die Kategorie "virtueller Computer" lautet.</span><span class="sxs-lookup"><span data-stu-id="15d6f-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="15d6f-118">Beispiel 3: Aktualisieren der Gruppen einer Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="15d6f-118">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="15d6f-119">Mit diesem Befehl werden die Gruppen einer Richtliniensatz Definition mit dem Namen VMPolicySetDefinition aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="15d6f-119">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="15d6f-120">Beispiel 4: Aktualisieren der Gruppen einer Richtliniensatz Definition mithilfe einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="15d6f-120">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="15d6f-121">Dieser Befehl aktualisiert die Gruppen einer Richtliniensatz Definition mit dem Namen VMPolicySetDefinition mithilfe einer Hashtabelle, um die Gruppen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="15d6f-121">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="15d6f-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="15d6f-122">PARAMETERS</span></span>

### <span data-ttu-id="15d6f-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="15d6f-123">-ApiVersion</span></span>
<span data-ttu-id="15d6f-124">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="15d6f-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="15d6f-125">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="15d6f-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="15d6f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d6f-126">-DefaultProfile</span></span>
<span data-ttu-id="15d6f-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="15d6f-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15d6f-128">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15d6f-128">-Description</span></span>
<span data-ttu-id="15d6f-129">Die Beschreibung für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="15d6f-129">The description for policy set definition.</span></span>

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

### <span data-ttu-id="15d6f-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="15d6f-130">-DisplayName</span></span>
<span data-ttu-id="15d6f-131">Der Anzeigename für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="15d6f-131">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="15d6f-132">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="15d6f-132">-GroupDefinition</span></span>
<span data-ttu-id="15d6f-133">Die Richtlinien Definitionsgruppen der aktualisierten Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="15d6f-133">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="15d6f-134">Dies kann entweder ein Pfad zu einer Datei sein, die die Gruppen enthält, oder die Gruppen als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="15d6f-134">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="15d6f-135">-ID</span><span class="sxs-lookup"><span data-stu-id="15d6f-135">-Id</span></span>
<span data-ttu-id="15d6f-136">Die vollqualifizierte Richtlinien Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="15d6f-136">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="15d6f-137">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="15d6f-137">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="15d6f-138">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="15d6f-138">-ManagementGroupName</span></span>
<span data-ttu-id="15d6f-139">Der Name der Verwaltungsgruppe der Richtliniensatz Definition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="15d6f-139">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="15d6f-140">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="15d6f-140">-Metadata</span></span>
<span data-ttu-id="15d6f-141">Die Metadaten der aktualisierten Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="15d6f-141">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="15d6f-142">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="15d6f-142">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="15d6f-143">-Name</span><span class="sxs-lookup"><span data-stu-id="15d6f-143">-Name</span></span>
<span data-ttu-id="15d6f-144">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="15d6f-144">The policy set definition name.</span></span>

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

### <span data-ttu-id="15d6f-145">-Parameter</span><span class="sxs-lookup"><span data-stu-id="15d6f-145">-Parameter</span></span>
<span data-ttu-id="15d6f-146">Die Parameters-Deklaration der aktualisierten Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="15d6f-146">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="15d6f-147">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="15d6f-147">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="15d6f-148">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="15d6f-148">-PolicyDefinition</span></span>
<span data-ttu-id="15d6f-149">Die Richtlinien Definitionen.</span><span class="sxs-lookup"><span data-stu-id="15d6f-149">The policy definitions.</span></span> <span data-ttu-id="15d6f-150">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Richtlinien Definitionen enthält, oder die Richtlinien Definitionen als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="15d6f-150">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="15d6f-151">-Pre</span><span class="sxs-lookup"><span data-stu-id="15d6f-151">-Pre</span></span>
<span data-ttu-id="15d6f-152">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="15d6f-152">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="15d6f-153">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="15d6f-153">-SubscriptionId</span></span>
<span data-ttu-id="15d6f-154">Die Abonnement-ID der Richtliniensatz Definition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="15d6f-154">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="15d6f-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15d6f-155">-Confirm</span></span>
<span data-ttu-id="15d6f-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15d6f-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15d6f-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15d6f-157">-WhatIf</span></span>
<span data-ttu-id="15d6f-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15d6f-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15d6f-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15d6f-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15d6f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d6f-160">CommonParameters</span></span>
<span data-ttu-id="15d6f-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15d6f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d6f-162">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15d6f-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d6f-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15d6f-163">INPUTS</span></span>

### <span data-ttu-id="15d6f-164">System. String</span><span class="sxs-lookup"><span data-stu-id="15d6f-164">System.String</span></span>

### <span data-ttu-id="15d6f-165">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="15d6f-165">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="15d6f-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15d6f-166">OUTPUTS</span></span>

### <span data-ttu-id="15d6f-167">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="15d6f-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="15d6f-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="15d6f-168">NOTES</span></span>

## <span data-ttu-id="15d6f-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15d6f-169">RELATED LINKS</span></span>
