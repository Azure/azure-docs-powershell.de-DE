---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301150"
---
# <span data-ttu-id="62ec7-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="62ec7-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="62ec7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="62ec7-103">Ruft Richtliniensatz Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="62ec7-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="62ec7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="62ec7-104">SYNTAX</span></span>

### <span data-ttu-id="62ec7-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="62ec7-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62ec7-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="62ec7-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62ec7-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62ec7-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62ec7-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62ec7-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62ec7-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="62ec7-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62ec7-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="62ec7-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62ec7-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62ec7-111">DESCRIPTION</span></span>
<span data-ttu-id="62ec7-112">Das Cmdlet " **Get-AzPolicySetDefinition** " Ruft eine Sammlung von Richtliniensatz Definitionen oder eine bestimmte Richtliniensatz Definition ab, die durch den Namen oder die ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="62ec7-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="62ec7-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62ec7-113">EXAMPLES</span></span>

### <span data-ttu-id="62ec7-114">Beispiel 1: Abrufen aller Richtliniensatz Definitionen</span><span class="sxs-lookup"><span data-stu-id="62ec7-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="62ec7-115">Dieser Befehl ruft alle Richtliniensatz Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="62ec7-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="62ec7-116">Beispiel 2: Abrufen der Richtliniensatz Definition aus dem aktuellen Abonnement nach Name</span><span class="sxs-lookup"><span data-stu-id="62ec7-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="62ec7-117">Dieser Befehl ruft die Richtliniensatz Definition mit dem Namen VMPolicySetDefinition aus dem aktuellen Standardabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="62ec7-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="62ec7-118">Beispiel 3: Abrufen der Richtliniensatz Definition aus dem Abonnement nach Name</span><span class="sxs-lookup"><span data-stu-id="62ec7-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="62ec7-119">Dieser Befehl ruft die Richtliniendefinition mit dem Namen VMPolicySetDefinition aus dem Abonnement mit der ID 3bf44b72-c631-427a-b8c8-53e2595398ca ab.</span><span class="sxs-lookup"><span data-stu-id="62ec7-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="62ec7-120">Beispiel 4: Abrufen aller benutzerdefinierten Richtliniensatz-Definitionen aus der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="62ec7-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="62ec7-121">Dieser Befehl ruft alle benutzerdefinierten Richtliniensatz Definitionen aus der Verwaltungsgruppe mit dem Namen Dept42 ab.</span><span class="sxs-lookup"><span data-stu-id="62ec7-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="62ec7-122">Beispiel 5: Abrufen von Richtliniensatz Definitionen aus einer bestimmten Kategorie</span><span class="sxs-lookup"><span data-stu-id="62ec7-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="62ec7-123">Dieser Befehl ruft alle Richtliniensatz Definitionen in der Kategorie "virtueller Computer" ab.</span><span class="sxs-lookup"><span data-stu-id="62ec7-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="62ec7-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="62ec7-124">PARAMETERS</span></span>

### <span data-ttu-id="62ec7-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="62ec7-125">-ApiVersion</span></span>
<span data-ttu-id="62ec7-126">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="62ec7-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="62ec7-127">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="62ec7-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="62ec7-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="62ec7-128">-Builtin</span></span>
<span data-ttu-id="62ec7-129">Begrenzt die Liste der Ergebnisse auf nur integrierte Richtliniensatz Definitionen.</span><span class="sxs-lookup"><span data-stu-id="62ec7-129">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="62ec7-130">– Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="62ec7-130">-Custom</span></span>
<span data-ttu-id="62ec7-131">Begrenzt die Liste der Ergebnisse auf nur benutzerdefinierte Richtliniensatz Definitionen.</span><span class="sxs-lookup"><span data-stu-id="62ec7-131">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="62ec7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ec7-132">-DefaultProfile</span></span>
<span data-ttu-id="62ec7-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="62ec7-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62ec7-134">-ID</span><span class="sxs-lookup"><span data-stu-id="62ec7-134">-Id</span></span>
<span data-ttu-id="62ec7-135">Die vollqualifizierte Richtliniensatz-Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="62ec7-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="62ec7-136">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="62ec7-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="62ec7-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="62ec7-137">-ManagementGroupName</span></span>
<span data-ttu-id="62ec7-138">Der Name der Verwaltungsgruppe der Richtliniensatz-Definition (en), die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="62ec7-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="62ec7-139">-Name</span><span class="sxs-lookup"><span data-stu-id="62ec7-139">-Name</span></span>
<span data-ttu-id="62ec7-140">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="62ec7-140">The policy set definition name.</span></span>

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

### <span data-ttu-id="62ec7-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="62ec7-141">-Pre</span></span>
<span data-ttu-id="62ec7-142">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="62ec7-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="62ec7-143">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="62ec7-143">-SubscriptionId</span></span>
<span data-ttu-id="62ec7-144">Die Abonnement-ID der Richtliniensatz-Definition (en), die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="62ec7-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="62ec7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ec7-145">CommonParameters</span></span>
<span data-ttu-id="62ec7-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ec7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ec7-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62ec7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ec7-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62ec7-148">INPUTS</span></span>

### <span data-ttu-id="62ec7-149">System. String</span><span class="sxs-lookup"><span data-stu-id="62ec7-149">System.String</span></span>

### <span data-ttu-id="62ec7-150">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="62ec7-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="62ec7-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62ec7-151">OUTPUTS</span></span>

### <span data-ttu-id="62ec7-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="62ec7-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="62ec7-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="62ec7-153">NOTES</span></span>

## <span data-ttu-id="62ec7-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62ec7-154">RELATED LINKS</span></span>
