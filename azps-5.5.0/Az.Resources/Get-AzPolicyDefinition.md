---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 52de80f1ad3cf84a7aa309b5e97b7fa24e9419b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153716"
---
# <span data-ttu-id="6f954-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f954-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="6f954-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f954-102">SYNOPSIS</span></span>
<span data-ttu-id="6f954-103">Ruft Richtliniendefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="6f954-103">Gets policy definitions.</span></span>

## <span data-ttu-id="6f954-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f954-104">SYNTAX</span></span>

### <span data-ttu-id="6f954-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f954-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f954-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f954-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f954-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f954-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f954-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f954-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f954-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f954-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f954-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f954-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f954-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f954-111">DESCRIPTION</span></span>
<span data-ttu-id="6f954-112">Das **Cmdlet "Get-AzPolicyDefinition"** ruft eine Sammlung von Richtliniendefinitionen oder eine bestimmte Richtliniendefinition ab, die durch Name oder ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6f954-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="6f954-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f954-113">EXAMPLES</span></span>

### <span data-ttu-id="6f954-114">Beispiel 1: Alle Richtliniendefinitionen erhalten</span><span class="sxs-lookup"><span data-stu-id="6f954-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="6f954-115">Dieser Befehl ruft alle Richtliniendefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="6f954-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="6f954-116">Beispiel 2: Richtliniendefinition aus dem aktuellen Abonnement nach Name</span><span class="sxs-lookup"><span data-stu-id="6f954-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="6f954-117">Dieser Befehl ruft die Richtliniendefinition "VMPolicyDefinition" aus dem aktuellen Standardabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="6f954-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="6f954-118">Beispiel 3: Erhalten der Richtliniendefinition aus der Verwaltungsgruppe nach Name</span><span class="sxs-lookup"><span data-stu-id="6f954-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="6f954-119">Dieser Befehl ruft die Richtliniendefinition "VMPolicyDefinition" aus der Verwaltungsgruppe mit dem Namen "Dept42" ab.</span><span class="sxs-lookup"><span data-stu-id="6f954-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="6f954-120">Beispiel 4: Alle integrierten Richtliniendefinitionen aus dem Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="6f954-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="6f954-121">Dieser Befehl ruft alle integrierten Richtliniendefinitionen aus dem Abonnement mit der ID 3bf44b72-c631-427a-b8c8-53e2595398ca ab.</span><span class="sxs-lookup"><span data-stu-id="6f954-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="6f954-122">Beispiel 5: Erhalten von Richtliniendefinitionen aus einer bestimmten Kategorie</span><span class="sxs-lookup"><span data-stu-id="6f954-122">Example 5: Get policy definitions from a given category</span></span>
```
PS C:\> Get-AzPolicyDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="6f954-123">Dieser Befehl ruft alle Richtliniendefinitionen in der Kategorie "Virtual Machine" ab.</span><span class="sxs-lookup"><span data-stu-id="6f954-123">This command gets all policy definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="6f954-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f954-124">PARAMETERS</span></span>

### <span data-ttu-id="6f954-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6f954-125">-ApiVersion</span></span>
<span data-ttu-id="6f954-126">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="6f954-126">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6f954-127">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="6f954-127">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6f954-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="6f954-128">-Builtin</span></span>
<span data-ttu-id="6f954-129">Beschränkt die Ergebnisliste auf integrierte Richtliniendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6f954-129">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="6f954-130">-Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="6f954-130">-Custom</span></span>
<span data-ttu-id="6f954-131">Beschränkt die Ergebnisliste auf benutzerdefinierte Richtliniendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6f954-131">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="6f954-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f954-132">-DefaultProfile</span></span>
<span data-ttu-id="6f954-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6f954-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f954-134">-ID</span><span class="sxs-lookup"><span data-stu-id="6f954-134">-Id</span></span>
<span data-ttu-id="6f954-135">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6f954-135">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6f954-136">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="6f954-136">-ManagementGroupName</span></span>
<span data-ttu-id="6f954-137">Der Name der Verwaltungsgruppe der zu erhaltende(n) Richtliniendefinition(en).</span><span class="sxs-lookup"><span data-stu-id="6f954-137">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="6f954-138">-Name</span><span class="sxs-lookup"><span data-stu-id="6f954-138">-Name</span></span>
<span data-ttu-id="6f954-139">Gibt den Namen der Richtliniendefinition an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6f954-139">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6f954-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="6f954-140">-Pre</span></span>
<span data-ttu-id="6f954-141">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f954-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6f954-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f954-142">-SubscriptionId</span></span>
<span data-ttu-id="6f954-143">Die Abonnement-ID der richtliniendefinition(n), die Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="6f954-143">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="6f954-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f954-144">CommonParameters</span></span>
<span data-ttu-id="6f954-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f954-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f954-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f954-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f954-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f954-147">INPUTS</span></span>

### <span data-ttu-id="6f954-148">System.String</span><span class="sxs-lookup"><span data-stu-id="6f954-148">System.String</span></span>

### <span data-ttu-id="6f954-149">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6f954-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6f954-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f954-150">OUTPUTS</span></span>

### <span data-ttu-id="6f954-151">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="6f954-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6f954-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6f954-152">NOTES</span></span>

## <span data-ttu-id="6f954-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6f954-153">RELATED LINKS</span></span>

[<span data-ttu-id="6f954-154">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f954-154">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="6f954-155">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f954-155">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="6f954-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f954-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


