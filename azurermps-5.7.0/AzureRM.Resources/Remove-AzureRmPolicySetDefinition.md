---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: fa96d686d66f9ef94322896974dc4dd3b81ad154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498849"
---
# <span data-ttu-id="24bdd-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="24bdd-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="24bdd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="24bdd-103">Entfernt eine Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="24bdd-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24bdd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24bdd-104">SYNTAX</span></span>

### <span data-ttu-id="24bdd-105">RemoveByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="24bdd-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24bdd-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="24bdd-106">RemoveById</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24bdd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24bdd-107">DESCRIPTION</span></span>
<span data-ttu-id="24bdd-108">Das Cmdlet **Remove-AzureRmPolicySetDefinition** entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="24bdd-108">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="24bdd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24bdd-109">EXAMPLES</span></span>

### <span data-ttu-id="24bdd-110">Beispiel 1: Entfernen der Richtliniensatz Definition nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="24bdd-110">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="24bdd-111">Der erste Befehl ruft eine Richtliniensatz Definition mithilfe des Get-AzureRmPolicySetDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="24bdd-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="24bdd-112">Der Befehl speichert Sie in der $PolicySetDefinition-Variablen.</span><span class="sxs-lookup"><span data-stu-id="24bdd-112">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="24bdd-113">Mit dem zweiten Befehl wird die Richtliniensatz Definition entfernt, die durch die **Resourcen** -Eigenschaft $PolicySetDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="24bdd-113">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="24bdd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="24bdd-114">PARAMETERS</span></span>

### <span data-ttu-id="24bdd-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="24bdd-115">-ApiVersion</span></span>
<span data-ttu-id="24bdd-116">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="24bdd-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="24bdd-117">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="24bdd-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bdd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24bdd-118">-DefaultProfile</span></span>
<span data-ttu-id="24bdd-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="24bdd-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bdd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="24bdd-120">-Force</span></span>
<span data-ttu-id="24bdd-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="24bdd-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bdd-122">-ID</span><span class="sxs-lookup"><span data-stu-id="24bdd-122">-Id</span></span>
<span data-ttu-id="24bdd-123">Die vollqualifizierte Richtliniensatz-Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="24bdd-123">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="24bdd-124">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="24bdd-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bdd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="24bdd-125">-Name</span></span>
<span data-ttu-id="24bdd-126">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="24bdd-126">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bdd-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="24bdd-127">-Pre</span></span>
<span data-ttu-id="24bdd-128">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="24bdd-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bdd-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="24bdd-129">-Confirm</span></span>
<span data-ttu-id="24bdd-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24bdd-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bdd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24bdd-131">-WhatIf</span></span>
<span data-ttu-id="24bdd-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24bdd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24bdd-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24bdd-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bdd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24bdd-134">CommonParameters</span></span>
<span data-ttu-id="24bdd-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24bdd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24bdd-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24bdd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24bdd-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24bdd-137">INPUTS</span></span>

### <span data-ttu-id="24bdd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="24bdd-138">System.String</span></span>

## <span data-ttu-id="24bdd-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24bdd-139">OUTPUTS</span></span>

### <span data-ttu-id="24bdd-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="24bdd-140">System.Boolean</span></span>

## <span data-ttu-id="24bdd-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="24bdd-141">NOTES</span></span>

## <span data-ttu-id="24bdd-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24bdd-142">RELATED LINKS</span></span>
