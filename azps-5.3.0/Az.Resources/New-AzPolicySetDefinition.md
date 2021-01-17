---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459303"
---
# <span data-ttu-id="f57b1-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f57b1-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="f57b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f57b1-102">SYNOPSIS</span></span>
<span data-ttu-id="f57b1-103">Erstellt eine Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="f57b1-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="f57b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f57b1-104">SYNTAX</span></span>

### <span data-ttu-id="f57b1-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f57b1-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f57b1-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f57b1-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f57b1-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f57b1-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f57b1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f57b1-108">DESCRIPTION</span></span>
<span data-ttu-id="f57b1-109">Das **Cmdlet "New-AzPolicySetDefinition"** erstellt eine Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="f57b1-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="f57b1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f57b1-110">EXAMPLES</span></span>

### <span data-ttu-id="f57b1-111">Beispiel 1: Erstellen einer Richtliniensatzdefinition mit Metadaten mithilfe einer Datei mit Richtliniensatz</span><span class="sxs-lookup"><span data-stu-id="f57b1-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "Finance"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="f57b1-112">Dieser Befehl erstellt eine Richtliniensatzdefinition namens VMPolicySetDefinition mit Metadaten, die angeben, dass die Kategorie "Virtual Machine" ist, die die in der Datei "C:\VMPolicy.js" angegebenen Richtliniendefinitionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f57b1-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="f57b1-113">Beispielinhalt der VMPolicy.jswird oben bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f57b1-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="f57b1-114">Beispiel 2: Erstellen einer parametrisierten Richtliniensatzdefinition</span><span class="sxs-lookup"><span data-stu-id="f57b1-114">Example 2: Create a parameterized policy set definition</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "[parameters('buTagValue')]"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="f57b1-115">Mit diesem Befehl wird eine parameterisierte Richtliniensatzdefinition namens VMPolicySetDefinition erstellt, die die richtliniendefinitionen enthält, die in C:\VMPolicy.jssind.</span><span class="sxs-lookup"><span data-stu-id="f57b1-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="f57b1-116">Beispielinhalt der VMPolicy.jswird oben bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f57b1-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="f57b1-117">Beispiel 3: Erstellen einer Richtliniensatzdefinition mit Richtliniendefinitionsgruppen</span><span class="sxs-lookup"><span data-stu-id="f57b1-117">Example 3: Create a policy set definition with policy definition groups</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "groupNames": [ "group1" ]
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf",
      "groupNames": [ "group2" ]
   }
]
```

```
$groupsJson = ConvertTo-Json @{ name = "group1" }, @{ name = "group2" }
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="f57b1-118">Dieser Befehl erstellt eine Richtliniensatzdefinition namens VMPolicySetDefinition mit Gruppierung von Richtliniendefinitionen, die in C:\VMPolicy.jsangegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f57b1-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="f57b1-119">Beispielinhalt der VMPolicy.jswird oben bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f57b1-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="f57b1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f57b1-120">PARAMETERS</span></span>

### <span data-ttu-id="f57b1-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f57b1-121">-ApiVersion</span></span>
<span data-ttu-id="f57b1-122">Wenn dies festgelegt ist, wird die Version der zu verwendenden Ressourcenanbieter-API angegeben.</span><span class="sxs-lookup"><span data-stu-id="f57b1-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f57b1-123">Wenn keine Angabe erfolgt, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f57b1-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f57b1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f57b1-124">-DefaultProfile</span></span>
<span data-ttu-id="f57b1-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f57b1-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f57b1-126">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f57b1-126">-Description</span></span>
<span data-ttu-id="f57b1-127">Die Beschreibung für die Definition des Richtliniensets.</span><span class="sxs-lookup"><span data-stu-id="f57b1-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="f57b1-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f57b1-128">-DisplayName</span></span>
<span data-ttu-id="f57b1-129">Der Anzeigename für die Definition des Richtliniensets.</span><span class="sxs-lookup"><span data-stu-id="f57b1-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="f57b1-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="f57b1-130">-GroupDefinition</span></span>
<span data-ttu-id="f57b1-131">Die Richtliniendefinitionsgruppen für die neue Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="f57b1-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="f57b1-132">Dies kann entweder ein Pfad zu einer Datei sein, die die Gruppen enthält, oder die Gruppen als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f57b1-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="f57b1-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f57b1-133">-ManagementGroupName</span></span>
<span data-ttu-id="f57b1-134">Der Name der Verwaltungsgruppe der neuen Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="f57b1-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="f57b1-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f57b1-135">-Metadata</span></span>
<span data-ttu-id="f57b1-136">Die Metadaten für die Definition des Richtliniensets.</span><span class="sxs-lookup"><span data-stu-id="f57b1-136">The metadata for policy set definition.</span></span> <span data-ttu-id="f57b1-137">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f57b1-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="f57b1-138">-Name</span><span class="sxs-lookup"><span data-stu-id="f57b1-138">-Name</span></span>
<span data-ttu-id="f57b1-139">Der Name der Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="f57b1-139">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f57b1-140">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f57b1-140">-Parameter</span></span>
<span data-ttu-id="f57b1-141">Die Parameterdeklaration für die Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="f57b1-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="f57b1-142">Dies kann entweder ein Pfad zu einem Dateinamen mit der Parameterdeklaration oder die Parameterdeklaration als eine JSON-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="f57b1-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="f57b1-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f57b1-143">-PolicyDefinition</span></span>
<span data-ttu-id="f57b1-144">Die Richtliniendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f57b1-144">The policy definitions.</span></span> <span data-ttu-id="f57b1-145">Dies kann entweder ein Pfad zu einem Dateinamen mit den Richtliniendefinitionen oder die Richtliniendefinitionen als eine JSON-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="f57b1-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f57b1-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="f57b1-146">-Pre</span></span>
<span data-ttu-id="f57b1-147">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f57b1-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f57b1-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f57b1-148">-SubscriptionId</span></span>
<span data-ttu-id="f57b1-149">Die Abonnement-ID der Definition des neuen Richtliniensets.</span><span class="sxs-lookup"><span data-stu-id="f57b1-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="f57b1-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f57b1-150">-Confirm</span></span>
<span data-ttu-id="f57b1-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f57b1-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f57b1-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f57b1-152">-WhatIf</span></span>
<span data-ttu-id="f57b1-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f57b1-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f57b1-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f57b1-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f57b1-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f57b1-155">CommonParameters</span></span>
<span data-ttu-id="f57b1-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f57b1-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f57b1-157">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f57b1-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f57b1-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f57b1-158">INPUTS</span></span>

### <span data-ttu-id="f57b1-159">System.String</span><span class="sxs-lookup"><span data-stu-id="f57b1-159">System.String</span></span>

### <span data-ttu-id="f57b1-160">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f57b1-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f57b1-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f57b1-161">OUTPUTS</span></span>

### <span data-ttu-id="f57b1-162">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f57b1-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f57b1-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f57b1-163">NOTES</span></span>

## <span data-ttu-id="f57b1-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f57b1-164">RELATED LINKS</span></span>
