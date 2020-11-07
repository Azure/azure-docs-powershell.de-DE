---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d0a1097407c9941b5be49b19ea7ba99e75b3fce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664329"
---
# <span data-ttu-id="b4aa3-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b4aa3-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="b4aa3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="b4aa3-103">Ruft Richtliniensatz Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4aa3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4aa3-104">SYNTAX</span></span>

### <span data-ttu-id="b4aa3-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4aa3-105">NameParameterSet (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4aa3-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4aa3-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4aa3-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4aa3-107">SubscriptionIdParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4aa3-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4aa3-108">IdParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4aa3-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4aa3-109">BuiltinFilterParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4aa3-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4aa3-110">CustomFilterParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4aa3-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4aa3-111">DESCRIPTION</span></span>
<span data-ttu-id="b4aa3-112">Das Cmdlet " **Get-AzureRmPolicySetDefinition** " Ruft eine Sammlung von Richtliniensatz Definitionen oder eine bestimmte Richtliniensatz Definition ab, die durch den Namen oder die ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-112">The **Get-AzureRmPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="b4aa3-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4aa3-113">EXAMPLES</span></span>

### <span data-ttu-id="b4aa3-114">Beispiel 1: Abrufen aller Richtliniensatz Definitionen</span><span class="sxs-lookup"><span data-stu-id="b4aa3-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="b4aa3-115">Dieser Befehl ruft alle Richtliniensatz Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="b4aa3-116">Beispiel 2: Abrufen der Richtliniensatz Definition aus dem aktuellen Abonnement nach Name</span><span class="sxs-lookup"><span data-stu-id="b4aa3-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="b4aa3-117">Dieser Befehl ruft die Richtliniensatz Definition mit dem Namen VMPolicySetDefinition aus dem aktuellen Standardabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="b4aa3-118">Beispiel 3: Abrufen der Richtliniensatz Definition aus dem Abonnement nach Name</span><span class="sxs-lookup"><span data-stu-id="b4aa3-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="b4aa3-119">Dieser Befehl ruft die Richtliniendefinition mit dem Namen VMPolicySetDefinition aus dem Abonnement mit der ID 3bf44b72-c631-427a-b8c8-53e2595398ca ab.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="b4aa3-120">Beispiel 4: Abrufen aller benutzerdefinierten Richtliniensatz-Definitionen aus der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="b4aa3-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="b4aa3-121">Dieser Befehl ruft alle benutzerdefinierten Richtliniensatz Definitionen aus der Verwaltungsgruppe mit dem Namen Dept42 ab.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

## <span data-ttu-id="b4aa3-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4aa3-122">PARAMETERS</span></span>

### <span data-ttu-id="b4aa3-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b4aa3-123">-ApiVersion</span></span>
<span data-ttu-id="b4aa3-124">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b4aa3-125">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b4aa3-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="b4aa3-126">-Builtin</span></span>
<span data-ttu-id="b4aa3-127">Begrenzt die Liste der Ergebnisse auf nur integrierte Richtliniensatz Definitionen.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-127">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="b4aa3-128">– Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="b4aa3-128">-Custom</span></span>
<span data-ttu-id="b4aa3-129">Begrenzt die Liste der Ergebnisse auf nur benutzerdefinierte Richtliniensatz Definitionen.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-129">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="b4aa3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4aa3-130">-DefaultProfile</span></span>
<span data-ttu-id="b4aa3-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b4aa3-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4aa3-132">-ID</span><span class="sxs-lookup"><span data-stu-id="b4aa3-132">-Id</span></span>
<span data-ttu-id="b4aa3-133">Die vollqualifizierte Richtliniensatz-Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-133">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="b4aa3-134">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b4aa3-134">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="b4aa3-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b4aa3-135">-ManagementGroupName</span></span>
<span data-ttu-id="b4aa3-136">Der Name der Verwaltungsgruppe der Richtliniensatz-Definition (en), die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-136">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="b4aa3-137">-Name</span><span class="sxs-lookup"><span data-stu-id="b4aa3-137">-Name</span></span>
<span data-ttu-id="b4aa3-138">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-138">The policy set definition name.</span></span>

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

### <span data-ttu-id="b4aa3-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="b4aa3-139">-Pre</span></span>
<span data-ttu-id="b4aa3-140">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-140">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b4aa3-141">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b4aa3-141">-SubscriptionId</span></span>
<span data-ttu-id="b4aa3-142">Die Abonnement-ID der Richtliniensatz-Definition (en), die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-142">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="b4aa3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4aa3-143">CommonParameters</span></span>
<span data-ttu-id="b4aa3-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4aa3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4aa3-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4aa3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4aa3-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4aa3-146">INPUTS</span></span>

### <span data-ttu-id="b4aa3-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b4aa3-147">System.String</span></span>

### <span data-ttu-id="b4aa3-148">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b4aa3-148">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b4aa3-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4aa3-149">OUTPUTS</span></span>

### <span data-ttu-id="b4aa3-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b4aa3-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b4aa3-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4aa3-151">NOTES</span></span>

## <span data-ttu-id="b4aa3-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4aa3-152">RELATED LINKS</span></span>
