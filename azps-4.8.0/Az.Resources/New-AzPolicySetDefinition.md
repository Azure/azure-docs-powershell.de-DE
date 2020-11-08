---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166124"
---
# <span data-ttu-id="313ac-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="313ac-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="313ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="313ac-102">SYNOPSIS</span></span>
<span data-ttu-id="313ac-103">Erstellt eine Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="313ac-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="313ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="313ac-104">SYNTAX</span></span>

### <span data-ttu-id="313ac-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="313ac-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="313ac-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="313ac-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="313ac-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="313ac-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="313ac-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="313ac-108">DESCRIPTION</span></span>
<span data-ttu-id="313ac-109">Das Cmdlet **New-AzPolicySetDefinition** erstellt eine Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="313ac-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="313ac-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="313ac-110">EXAMPLES</span></span>

### <span data-ttu-id="313ac-111">Beispiel 1: Erstellen einer Richtliniensatz Definition mit Metadaten mithilfe einer Richtliniensatz Datei</span><span class="sxs-lookup"><span data-stu-id="313ac-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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

<span data-ttu-id="313ac-112">Dieser Befehl erstellt eine Richtliniensatz Definition mit dem Namen VMPolicySetDefinition mit Metadaten, die angibt, dass die Kategorie "virtueller Computer" ist, die die in C:\VMPolicy.json angegebenen Richtlinien Definitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="313ac-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="313ac-113">Der Beispielinhalt der VMPolicy.jsist oben angegeben.</span><span class="sxs-lookup"><span data-stu-id="313ac-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="313ac-114">Beispiel 2: Erstellen einer parametrisierten Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="313ac-114">Example 2: Create a parameterized policy set definition</span></span>
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

<span data-ttu-id="313ac-115">Dieser Befehl erstellt eine parametrisierte Richtliniensatz Definition mit dem Namen VMPolicySetDefinition, die die in C:\VMPolicy.json angegebenen Richtlinien Definitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="313ac-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="313ac-116">Der Beispielinhalt der VMPolicy.jsist oben angegeben.</span><span class="sxs-lookup"><span data-stu-id="313ac-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="313ac-117">Beispiel 3: Erstellen einer Richtliniensatz Definition mit Richtlinien Definitionsgruppen</span><span class="sxs-lookup"><span data-stu-id="313ac-117">Example 3: Create a policy set definition with policy definition groups</span></span>
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

<span data-ttu-id="313ac-118">Dieser Befehl erstellt eine Richtliniensatz Definition mit dem Namen VMPolicySetDefinition mit einer Gruppierung von Richtlinien Definitionen, die in C:\VMPolicy.json angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="313ac-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="313ac-119">Der Beispielinhalt der VMPolicy.jsist oben angegeben.</span><span class="sxs-lookup"><span data-stu-id="313ac-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="313ac-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="313ac-120">PARAMETERS</span></span>

### <span data-ttu-id="313ac-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="313ac-121">-ApiVersion</span></span>
<span data-ttu-id="313ac-122">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="313ac-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="313ac-123">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="313ac-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="313ac-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313ac-124">-DefaultProfile</span></span>
<span data-ttu-id="313ac-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="313ac-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="313ac-126">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="313ac-126">-Description</span></span>
<span data-ttu-id="313ac-127">Die Beschreibung für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="313ac-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="313ac-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="313ac-128">-DisplayName</span></span>
<span data-ttu-id="313ac-129">Der Anzeigename für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="313ac-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="313ac-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="313ac-130">-GroupDefinition</span></span>
<span data-ttu-id="313ac-131">Die Richtlinien Definitionsgruppen für die neue Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="313ac-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="313ac-132">Dies kann entweder ein Pfad zu einer Datei sein, die die Gruppen enthält, oder die Gruppen als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="313ac-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="313ac-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="313ac-133">-ManagementGroupName</span></span>
<span data-ttu-id="313ac-134">Der Name der Verwaltungsgruppe der neuen Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="313ac-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="313ac-135">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="313ac-135">-Metadata</span></span>
<span data-ttu-id="313ac-136">Die Metadaten für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="313ac-136">The metadata for policy set definition.</span></span> <span data-ttu-id="313ac-137">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="313ac-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="313ac-138">-Name</span><span class="sxs-lookup"><span data-stu-id="313ac-138">-Name</span></span>
<span data-ttu-id="313ac-139">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="313ac-139">The policy set definition name.</span></span>

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

### <span data-ttu-id="313ac-140">-Parameter</span><span class="sxs-lookup"><span data-stu-id="313ac-140">-Parameter</span></span>
<span data-ttu-id="313ac-141">Die Parameters-Deklaration für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="313ac-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="313ac-142">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="313ac-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="313ac-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="313ac-143">-PolicyDefinition</span></span>
<span data-ttu-id="313ac-144">Die Richtlinien Definitionen.</span><span class="sxs-lookup"><span data-stu-id="313ac-144">The policy definitions.</span></span> <span data-ttu-id="313ac-145">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Richtlinien Definitionen enthält, oder die Richtlinien Definitionen als JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="313ac-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="313ac-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="313ac-146">-Pre</span></span>
<span data-ttu-id="313ac-147">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="313ac-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="313ac-148">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="313ac-148">-SubscriptionId</span></span>
<span data-ttu-id="313ac-149">Die Abonnement-ID der neuen Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="313ac-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="313ac-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="313ac-150">-Confirm</span></span>
<span data-ttu-id="313ac-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="313ac-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="313ac-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="313ac-152">-WhatIf</span></span>
<span data-ttu-id="313ac-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="313ac-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="313ac-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="313ac-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="313ac-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313ac-155">CommonParameters</span></span>
<span data-ttu-id="313ac-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="313ac-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313ac-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="313ac-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313ac-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="313ac-158">INPUTS</span></span>

### <span data-ttu-id="313ac-159">System. String</span><span class="sxs-lookup"><span data-stu-id="313ac-159">System.String</span></span>

### <span data-ttu-id="313ac-160">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="313ac-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="313ac-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="313ac-161">OUTPUTS</span></span>

### <span data-ttu-id="313ac-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="313ac-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="313ac-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="313ac-163">NOTES</span></span>

## <span data-ttu-id="313ac-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="313ac-164">RELATED LINKS</span></span>
