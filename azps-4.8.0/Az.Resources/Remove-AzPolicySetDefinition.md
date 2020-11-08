---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 551e30077fe1ce836f98c18d3c00976adc779f64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165649"
---
# <span data-ttu-id="2e6ac-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="2e6ac-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="2e6ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e6ac-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6ac-103">Entfernt eine Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="2e6ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e6ac-104">SYNTAX</span></span>

### <span data-ttu-id="2e6ac-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2e6ac-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e6ac-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e6ac-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e6ac-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e6ac-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e6ac-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e6ac-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e6ac-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e6ac-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e6ac-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e6ac-110">DESCRIPTION</span></span>
<span data-ttu-id="2e6ac-111">Das Cmdlet **Remove-AzPolicySetDefinition** entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="2e6ac-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e6ac-112">EXAMPLES</span></span>

### <span data-ttu-id="2e6ac-113">Beispiel 1: Entfernen der Richtliniensatz Definition nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2e6ac-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="2e6ac-114">Der erste Befehl ruft eine Richtliniensatz Definition mithilfe des Get-AzPolicySetDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="2e6ac-115">Der Befehl speichert Sie in der $PolicySetDefinition-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="2e6ac-116">Mit dem zweiten Befehl wird die Richtliniensatz Definition entfernt, die durch die **Resourcen** -Eigenschaft $PolicySetDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="2e6ac-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e6ac-117">PARAMETERS</span></span>

### <span data-ttu-id="2e6ac-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2e6ac-118">-ApiVersion</span></span>
<span data-ttu-id="2e6ac-119">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2e6ac-120">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2e6ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6ac-121">-DefaultProfile</span></span>
<span data-ttu-id="2e6ac-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2e6ac-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e6ac-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2e6ac-123">-Force</span></span>
<span data-ttu-id="2e6ac-124">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2e6ac-125">-ID</span><span class="sxs-lookup"><span data-stu-id="2e6ac-125">-Id</span></span>
<span data-ttu-id="2e6ac-126">Die vollqualifizierte Richtliniensatz-Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="2e6ac-127">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="2e6ac-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="2e6ac-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2e6ac-128">-InputObject</span></span>
<span data-ttu-id="2e6ac-129">Das zu entfernende Richtliniensatz-Definitionsobjekt, das von einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="2e6ac-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="2e6ac-130">-ManagementGroupName</span></span>
<span data-ttu-id="2e6ac-131">Der Name der Verwaltungsgruppe der Richtliniensatz Definition, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-131">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="2e6ac-132">-Name</span><span class="sxs-lookup"><span data-stu-id="2e6ac-132">-Name</span></span>
<span data-ttu-id="2e6ac-133">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-133">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6ac-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="2e6ac-134">-Pre</span></span>
<span data-ttu-id="2e6ac-135">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2e6ac-136">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2e6ac-136">-SubscriptionId</span></span>
<span data-ttu-id="2e6ac-137">Die Abonnement-ID der Richtliniensatz Definition, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-137">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="2e6ac-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2e6ac-138">-Confirm</span></span>
<span data-ttu-id="2e6ac-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e6ac-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e6ac-140">-WhatIf</span></span>
<span data-ttu-id="2e6ac-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e6ac-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e6ac-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6ac-143">CommonParameters</span></span>
<span data-ttu-id="2e6ac-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6ac-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e6ac-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6ac-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e6ac-146">INPUTS</span></span>

### <span data-ttu-id="2e6ac-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2e6ac-147">System.String</span></span>

### <span data-ttu-id="2e6ac-148">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2e6ac-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2e6ac-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e6ac-149">OUTPUTS</span></span>

### <span data-ttu-id="2e6ac-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2e6ac-150">System.Boolean</span></span>

## <span data-ttu-id="2e6ac-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e6ac-151">NOTES</span></span>

## <span data-ttu-id="2e6ac-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e6ac-152">RELATED LINKS</span></span>
