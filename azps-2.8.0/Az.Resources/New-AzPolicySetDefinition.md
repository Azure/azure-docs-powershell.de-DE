---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 838fe6f4ed7ff1e69a6bdf99a8816f00fc0ab019
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825007"
---
# <span data-ttu-id="e5619-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="e5619-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="e5619-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5619-102">SYNOPSIS</span></span>
<span data-ttu-id="e5619-103">Erstellt eine Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="e5619-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="e5619-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5619-104">SYNTAX</span></span>

### <span data-ttu-id="e5619-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5619-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5619-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5619-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5619-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5619-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5619-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5619-108">DESCRIPTION</span></span>
<span data-ttu-id="e5619-109">Das Cmdlet **New-AzPolicySetDefinition** erstellt eine Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="e5619-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="e5619-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5619-110">EXAMPLES</span></span>

### <span data-ttu-id="e5619-111">Beispiel 1: Erstellen einer Richtliniensatz Definition mit Metadaten mithilfe einer Richtliniensatz Datei</span><span class="sxs-lookup"><span data-stu-id="e5619-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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

<span data-ttu-id="e5619-112">Dieser Befehl erstellt eine Richtliniensatz Definition mit dem Namen VMPolicySetDefinition mit Metadaten, die angibt, dass die Kategorie "virtueller Computer" ist, die die in C:\VMPolicy.json angegebenen Richtlinien Definitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="e5619-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="e5619-113">Der Beispielinhalt der VMPolicy.jsist oben angegeben.</span><span class="sxs-lookup"><span data-stu-id="e5619-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="e5619-114">Beispiel 2: Erstellen einer parametrisierten Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="e5619-114">Example 2: Create a parameterized policy set definition</span></span>
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

<span data-ttu-id="e5619-115">Dieser Befehl erstellt eine parametrisierte Richtliniensatz Definition mit dem Namen VMPolicySetDefinition, die die in C:\VMPolicy.json angegebenen Richtlinien Definitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="e5619-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="e5619-116">Der Beispielinhalt der VMPolicy.jsist oben angegeben.</span><span class="sxs-lookup"><span data-stu-id="e5619-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="e5619-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5619-117">PARAMETERS</span></span>

### <span data-ttu-id="e5619-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e5619-118">-ApiVersion</span></span>
<span data-ttu-id="e5619-119">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e5619-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e5619-120">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e5619-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e5619-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5619-121">-DefaultProfile</span></span>
<span data-ttu-id="e5619-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e5619-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5619-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5619-123">-Description</span></span>
<span data-ttu-id="e5619-124">Die Beschreibung für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="e5619-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="e5619-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e5619-125">-DisplayName</span></span>
<span data-ttu-id="e5619-126">Der Anzeigename für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="e5619-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="e5619-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e5619-127">-ManagementGroupName</span></span>
<span data-ttu-id="e5619-128">Der Name der Verwaltungsgruppe der neuen Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="e5619-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="e5619-129">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="e5619-129">-Metadata</span></span>
<span data-ttu-id="e5619-130">Die Metadaten für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="e5619-130">The metadata for policy set definition.</span></span> <span data-ttu-id="e5619-131">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e5619-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="e5619-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e5619-132">-Name</span></span>
<span data-ttu-id="e5619-133">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="e5619-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="e5619-134">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e5619-134">-Parameter</span></span>
<span data-ttu-id="e5619-135">Die Parameters-Deklaration für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="e5619-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="e5619-136">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e5619-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="e5619-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e5619-137">-PolicyDefinition</span></span>
<span data-ttu-id="e5619-138">Die Richtlinien Definitionen.</span><span class="sxs-lookup"><span data-stu-id="e5619-138">The policy definitions.</span></span> <span data-ttu-id="e5619-139">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Richtlinien Definitionen enthält, oder die Richtlinien Definitionen als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e5619-139">This can either be a path to a file name containing the policy definitions, or the policy definitions as string.</span></span>

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

### <span data-ttu-id="e5619-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="e5619-140">-Pre</span></span>
<span data-ttu-id="e5619-141">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="e5619-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e5619-142">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e5619-142">-SubscriptionId</span></span>
<span data-ttu-id="e5619-143">Die Abonnement-ID der neuen Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="e5619-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="e5619-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5619-144">-Confirm</span></span>
<span data-ttu-id="e5619-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5619-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5619-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5619-146">-WhatIf</span></span>
<span data-ttu-id="e5619-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5619-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5619-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5619-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5619-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5619-149">CommonParameters</span></span>
<span data-ttu-id="e5619-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5619-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5619-151">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5619-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5619-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5619-152">INPUTS</span></span>

### <span data-ttu-id="e5619-153">System. String</span><span class="sxs-lookup"><span data-stu-id="e5619-153">System.String</span></span>

### <span data-ttu-id="e5619-154">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e5619-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e5619-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5619-155">OUTPUTS</span></span>

### <span data-ttu-id="e5619-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e5619-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e5619-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5619-157">NOTES</span></span>

## <span data-ttu-id="e5619-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5619-158">RELATED LINKS</span></span>
