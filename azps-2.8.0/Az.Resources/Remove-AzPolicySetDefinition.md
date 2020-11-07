---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 5141b4b0c7639580fbb8037193f91ac41464e233
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824947"
---
# <span data-ttu-id="6cda5-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="6cda5-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="6cda5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cda5-102">SYNOPSIS</span></span>
<span data-ttu-id="6cda5-103">Entfernt eine Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="6cda5-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="6cda5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cda5-104">SYNTAX</span></span>

### <span data-ttu-id="6cda5-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6cda5-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cda5-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cda5-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cda5-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cda5-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cda5-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cda5-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cda5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cda5-109">DESCRIPTION</span></span>
<span data-ttu-id="6cda5-110">Das Cmdlet **Remove-AzPolicySetDefinition** entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="6cda5-110">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="6cda5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cda5-111">EXAMPLES</span></span>

### <span data-ttu-id="6cda5-112">Beispiel 1: Entfernen der Richtliniensatz Definition nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6cda5-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="6cda5-113">Der erste Befehl ruft eine Richtliniensatz Definition mithilfe des Get-AzPolicySetDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="6cda5-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="6cda5-114">Der Befehl speichert Sie in der $PolicySetDefinition-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6cda5-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="6cda5-115">Mit dem zweiten Befehl wird die Richtliniensatz Definition entfernt, die durch die **Resourcen** -Eigenschaft $PolicySetDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="6cda5-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="6cda5-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cda5-116">PARAMETERS</span></span>

### <span data-ttu-id="6cda5-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6cda5-117">-ApiVersion</span></span>
<span data-ttu-id="6cda5-118">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6cda5-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6cda5-119">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6cda5-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6cda5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cda5-120">-DefaultProfile</span></span>
<span data-ttu-id="6cda5-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6cda5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cda5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6cda5-122">-Force</span></span>
<span data-ttu-id="6cda5-123">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="6cda5-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6cda5-124">-ID</span><span class="sxs-lookup"><span data-stu-id="6cda5-124">-Id</span></span>
<span data-ttu-id="6cda5-125">Die vollqualifizierte Richtliniensatz-Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="6cda5-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="6cda5-126">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="6cda5-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="6cda5-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="6cda5-127">-ManagementGroupName</span></span>
<span data-ttu-id="6cda5-128">Der Name der Verwaltungsgruppe der Richtliniensatz Definition, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cda5-128">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="6cda5-129">-Name</span><span class="sxs-lookup"><span data-stu-id="6cda5-129">-Name</span></span>
<span data-ttu-id="6cda5-130">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="6cda5-130">The policy set definition name.</span></span>

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

### <span data-ttu-id="6cda5-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="6cda5-131">-Pre</span></span>
<span data-ttu-id="6cda5-132">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="6cda5-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6cda5-133">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="6cda5-133">-SubscriptionId</span></span>
<span data-ttu-id="6cda5-134">Die Abonnement-ID der Richtliniensatz Definition, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cda5-134">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="6cda5-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6cda5-135">-Confirm</span></span>
<span data-ttu-id="6cda5-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6cda5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cda5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cda5-137">-WhatIf</span></span>
<span data-ttu-id="6cda5-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6cda5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cda5-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cda5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cda5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cda5-140">CommonParameters</span></span>
<span data-ttu-id="6cda5-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cda5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cda5-142">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cda5-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cda5-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cda5-143">INPUTS</span></span>

### <span data-ttu-id="6cda5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6cda5-144">System.String</span></span>

### <span data-ttu-id="6cda5-145">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6cda5-145">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6cda5-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cda5-146">OUTPUTS</span></span>

### <span data-ttu-id="6cda5-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6cda5-147">System.Boolean</span></span>

## <span data-ttu-id="6cda5-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cda5-148">NOTES</span></span>

## <span data-ttu-id="6cda5-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cda5-149">RELATED LINKS</span></span>
