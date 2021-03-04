---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: ae1cc96cd617ec74a69fc2c95ec50973e688ebe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941003"
---
# <span data-ttu-id="c7660-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c7660-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="c7660-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7660-102">SYNOPSIS</span></span>
<span data-ttu-id="c7660-103">Erstellt eine Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="c7660-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="c7660-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7660-104">SYNTAX</span></span>

### <span data-ttu-id="c7660-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7660-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7660-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7660-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7660-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7660-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7660-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7660-108">DESCRIPTION</span></span>
<span data-ttu-id="c7660-109">Das **Cmdlet New-AzPolicySetDefinition** erstellt eine Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="c7660-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="c7660-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c7660-110">EXAMPLES</span></span>

### <span data-ttu-id="c7660-111">Beispiel 1: Erstellen einer Richtliniensatzdefinition mit Metadaten mithilfe einer Richtliniensatzdatei</span><span class="sxs-lookup"><span data-stu-id="c7660-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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

<span data-ttu-id="c7660-112">Mit diesem Befehl wird eine Richtliniensatzdefinition mit dem Namen VMPolicySetDefinition mit Metadaten erstellt, die angeben, dass die Kategorie "Virtueller Computer" ist, die die in der Datei C:\VMPolicy.jsenthält.</span><span class="sxs-lookup"><span data-stu-id="c7660-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="c7660-113">Der Beispielinhalt der VMPolicy.jsist oben angegeben.</span><span class="sxs-lookup"><span data-stu-id="c7660-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="c7660-114">Beispiel 2: Erstellen einer parameterisierten Richtliniensatzdefinition</span><span class="sxs-lookup"><span data-stu-id="c7660-114">Example 2: Create a parameterized policy set definition</span></span>
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

<span data-ttu-id="c7660-115">Mit diesem Befehl wird eine parameterisierte Richtliniensatzdefinition namens VMPolicySetDefinition erstellt, die die richtliniendefinitionen enthält, die in C:\VMPolicy.jsfestgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="c7660-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="c7660-116">Der Beispielinhalt der VMPolicy.jsist oben angegeben.</span><span class="sxs-lookup"><span data-stu-id="c7660-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="c7660-117">Beispiel 3: Erstellen einer Richtliniensatzdefinition mit Richtliniendefinitionsgruppen</span><span class="sxs-lookup"><span data-stu-id="c7660-117">Example 3: Create a policy set definition with policy definition groups</span></span>
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

<span data-ttu-id="c7660-118">Mit diesem Befehl wird eine Richtliniensatzdefinition mit dem Namen VMPolicySetDefinition mit Gruppierung von Richtliniendefinitionen erstellt, die in C:\VMPolicy.jsfestgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="c7660-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="c7660-119">Der Beispielinhalt der VMPolicy.jsist oben angegeben.</span><span class="sxs-lookup"><span data-stu-id="c7660-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="c7660-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c7660-120">PARAMETERS</span></span>

### <span data-ttu-id="c7660-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c7660-121">-ApiVersion</span></span>
<span data-ttu-id="c7660-122">Wenn festgelegt, gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="c7660-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c7660-123">Wenn nicht angegeben, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c7660-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c7660-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7660-124">-DefaultProfile</span></span>
<span data-ttu-id="c7660-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c7660-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7660-126">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7660-126">-Description</span></span>
<span data-ttu-id="c7660-127">Die Beschreibung für die Definition des Richtliniensatzs.</span><span class="sxs-lookup"><span data-stu-id="c7660-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="c7660-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c7660-128">-DisplayName</span></span>
<span data-ttu-id="c7660-129">Der Anzeigename für die Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="c7660-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="c7660-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="c7660-130">-GroupDefinition</span></span>
<span data-ttu-id="c7660-131">Die Richtliniendefinitionsgruppen für die neue Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="c7660-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="c7660-132">Dies kann entweder ein Pfad zu einer Datei sein, die die Gruppen enthält, oder die Gruppen als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c7660-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="c7660-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c7660-133">-ManagementGroupName</span></span>
<span data-ttu-id="c7660-134">Der Name der Verwaltungsgruppe der neuen Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="c7660-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="c7660-135">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="c7660-135">-Metadata</span></span>
<span data-ttu-id="c7660-136">Die Metadaten für die Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="c7660-136">The metadata for policy set definition.</span></span> <span data-ttu-id="c7660-137">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c7660-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="c7660-138">-Name</span><span class="sxs-lookup"><span data-stu-id="c7660-138">-Name</span></span>
<span data-ttu-id="c7660-139">Der Definitionsname des Richtliniensatzs.</span><span class="sxs-lookup"><span data-stu-id="c7660-139">The policy set definition name.</span></span>

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

### <span data-ttu-id="c7660-140">-Parameter</span><span class="sxs-lookup"><span data-stu-id="c7660-140">-Parameter</span></span>
<span data-ttu-id="c7660-141">Die Parameterdeklaration für die Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="c7660-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="c7660-142">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Parameterdeklaration enthält, oder die Parameterdeklaration als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c7660-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="c7660-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c7660-143">-PolicyDefinition</span></span>
<span data-ttu-id="c7660-144">Die Richtliniendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c7660-144">The policy definitions.</span></span> <span data-ttu-id="c7660-145">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Richtliniendefinitionen enthält, oder die Richtliniendefinitionen als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c7660-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="c7660-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="c7660-146">-Pre</span></span>
<span data-ttu-id="c7660-147">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7660-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c7660-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7660-148">-SubscriptionId</span></span>
<span data-ttu-id="c7660-149">Die Abonnement-ID der neuen Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="c7660-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="c7660-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7660-150">-Confirm</span></span>
<span data-ttu-id="c7660-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7660-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7660-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7660-152">-WhatIf</span></span>
<span data-ttu-id="c7660-153">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7660-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7660-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7660-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7660-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7660-155">CommonParameters</span></span>
<span data-ttu-id="c7660-156">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7660-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7660-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7660-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7660-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c7660-158">INPUTS</span></span>

### <span data-ttu-id="c7660-159">System.String</span><span class="sxs-lookup"><span data-stu-id="c7660-159">System.String</span></span>

### <span data-ttu-id="c7660-160">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c7660-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c7660-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c7660-161">OUTPUTS</span></span>

### <span data-ttu-id="c7660-162">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c7660-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c7660-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c7660-163">NOTES</span></span>

## <span data-ttu-id="c7660-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c7660-164">RELATED LINKS</span></span>
