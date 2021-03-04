---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 259b0abd120fb27eee1ca80da61266f4c890423f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928912"
---
# <span data-ttu-id="2ff17-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2ff17-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="2ff17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ff17-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff17-103">Erstellt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="2ff17-103">Creates a policy definition.</span></span>

## <span data-ttu-id="2ff17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ff17-104">SYNTAX</span></span>

### <span data-ttu-id="2ff17-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ff17-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ff17-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ff17-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ff17-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ff17-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ff17-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ff17-108">DESCRIPTION</span></span>
<span data-ttu-id="2ff17-109">Das **Cmdlet New-AzPolicyDefinition** erstellt eine Richtliniendefinition, die eine Richtlinienregel im JSON-Format (JavaScript Object Notation) enthält.</span><span class="sxs-lookup"><span data-stu-id="2ff17-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="2ff17-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ff17-110">EXAMPLES</span></span>

### <span data-ttu-id="2ff17-111">Beispiel 1: Erstellen einer Richtliniendefinition mithilfe einer Richtliniendatei</span><span class="sxs-lookup"><span data-stu-id="2ff17-111">Example 1: Create a policy definition by using a policy file</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": ["eastus", "westus", "centralus"]
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="2ff17-112">Mit diesem Befehl wird eine Richtliniendefinition mit dem Namen LocationDefinition erstellt, die die richtlinienregel enthält, die in C:\LocationPolicy.jsfestgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2ff17-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="2ff17-113">Beispielinhalt für LocationPolicy.jsdatei wird oben bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2ff17-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="2ff17-114">Beispiel 2: Erstellen einer parameterisierten Richtliniendefinition mithilfe von Inlineparametern</span><span class="sxs-lookup"><span data-stu-id="2ff17-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": "[parameters('listOfAllowedLocations')]"
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="2ff17-115">Mit diesem Befehl wird eine Richtliniendefinition mit dem Namen LocationDefinition erstellt, die die richtlinienregel enthält, die in C:\LocationPolicy.jsfestgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2ff17-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="2ff17-116">Die Parameterdefinition für die Richtlinienregel wird inline bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2ff17-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="2ff17-117">Beispiel 3: Erstellen einer Richtliniendefinition inline in einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="2ff17-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="2ff17-118">Mit diesem Befehl wird eine Richtliniendefinition mit dem Namen VMPolicyDefinition in der Verwaltungsgruppe Dept42 erstellt.</span><span class="sxs-lookup"><span data-stu-id="2ff17-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="2ff17-119">Der Befehl gibt die Richtlinie als Zeichenfolge im gültigen JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="2ff17-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="2ff17-120">Beispiel 4: Erstellen einer Richtliniendefinition inline mit Metadaten</span><span class="sxs-lookup"><span data-stu-id="2ff17-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="2ff17-121">Mit diesem Befehl wird eine Richtliniendefinition mit dem Namen VMPolicyDefinition mit Metadaten erstellt, die angeben, dass die Kategorie "Virtueller Computer" ist.</span><span class="sxs-lookup"><span data-stu-id="2ff17-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="2ff17-122">Der Befehl gibt die Richtlinie als Zeichenfolge im gültigen JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="2ff17-122">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="2ff17-123">Beispiel 5: Erstellen einer Richtliniendefinition inline mit Modus</span><span class="sxs-lookup"><span data-stu-id="2ff17-123">Example 5: Create a policy definition inline with mode</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'TagsPolicyDefinition' -Policy '{"if":{"value":"[less(length(field(''tags'')), 3)]","equals":true},"then":{"effect":"deny"}}' -Mode Indexed


Name               : TagsPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
ResourceName       : TagsPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=TagsPolicyDefinition; policyType=Custom; mode=Indexed; metadata=; parameters=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
```

<span data-ttu-id="2ff17-124">Mit diesem Befehl wird eine Richtliniendefinition mit dem Namen TagsPolicyDefinition mit dem Modus "Indiziert" erstellt, der angibt, dass die Richtlinie nur für Ressourcentypen ausgewertet werden sollte, die Tags und Speicherort unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2ff17-124">This command creates a policy definition named TagsPolicyDefinition with mode "Indexed" indicating the policy should be evaluated only for resource types that support tags and location.</span></span>

## <span data-ttu-id="2ff17-125">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2ff17-125">PARAMETERS</span></span>

### <span data-ttu-id="2ff17-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2ff17-126">-ApiVersion</span></span>
<span data-ttu-id="2ff17-127">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="2ff17-127">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2ff17-128">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="2ff17-128">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2ff17-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff17-129">-DefaultProfile</span></span>
<span data-ttu-id="2ff17-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2ff17-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ff17-131">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ff17-131">-Description</span></span>
<span data-ttu-id="2ff17-132">Gibt eine Beschreibung für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="2ff17-132">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="2ff17-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2ff17-133">-DisplayName</span></span>
<span data-ttu-id="2ff17-134">Gibt einen Anzeigenamen für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="2ff17-134">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="2ff17-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="2ff17-135">-ManagementGroupName</span></span>
<span data-ttu-id="2ff17-136">Der Name der Verwaltungsgruppe der neuen Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="2ff17-136">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="2ff17-137">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="2ff17-137">-Metadata</span></span>
<span data-ttu-id="2ff17-138">Die Metadaten für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="2ff17-138">The metadata for policy definition.</span></span> <span data-ttu-id="2ff17-139">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2ff17-139">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="2ff17-140">-Modus</span><span class="sxs-lookup"><span data-stu-id="2ff17-140">-Mode</span></span>
<span data-ttu-id="2ff17-141">Der Modus der Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="2ff17-141">The mode of the policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: All
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff17-142">-Name</span><span class="sxs-lookup"><span data-stu-id="2ff17-142">-Name</span></span>
<span data-ttu-id="2ff17-143">Gibt einen Namen für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="2ff17-143">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="2ff17-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="2ff17-144">-Parameter</span></span>
<span data-ttu-id="2ff17-145">Die Parameterdeklaration für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="2ff17-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="2ff17-146">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Parameterdeklaration enthält, oder die Parameterdeklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2ff17-146">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="2ff17-147">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="2ff17-147">-Policy</span></span>
<span data-ttu-id="2ff17-148">Gibt eine Richtlinienregel für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="2ff17-148">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="2ff17-149">Sie können den Pfad einer JSON-Datei oder eine Zeichenfolge angeben, die die Richtlinie im JSON-Format enthält.</span><span class="sxs-lookup"><span data-stu-id="2ff17-149">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="2ff17-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="2ff17-150">-Pre</span></span>
<span data-ttu-id="2ff17-151">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ff17-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2ff17-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ff17-152">-SubscriptionId</span></span>
<span data-ttu-id="2ff17-153">Die Abonnement-ID der neuen Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="2ff17-153">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="2ff17-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff17-154">CommonParameters</span></span>
<span data-ttu-id="2ff17-155">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ff17-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff17-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ff17-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff17-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ff17-157">INPUTS</span></span>

### <span data-ttu-id="2ff17-158">System.String</span><span class="sxs-lookup"><span data-stu-id="2ff17-158">System.String</span></span>

### <span data-ttu-id="2ff17-159">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2ff17-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2ff17-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ff17-160">OUTPUTS</span></span>

### <span data-ttu-id="2ff17-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="2ff17-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2ff17-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2ff17-162">NOTES</span></span>

## <span data-ttu-id="2ff17-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2ff17-163">RELATED LINKS</span></span>

[<span data-ttu-id="2ff17-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2ff17-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="2ff17-165">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2ff17-165">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="2ff17-166">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2ff17-166">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


