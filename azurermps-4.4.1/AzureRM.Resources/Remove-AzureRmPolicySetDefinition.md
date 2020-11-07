---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d3b9d8af81f08786536abf0d26b3c4ba2f2d66bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663532"
---
# <span data-ttu-id="e3b55-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="e3b55-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="e3b55-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3b55-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b55-103">Entfernt eine Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="e3b55-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3b55-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3b55-104">SYNTAX</span></span>

### <span data-ttu-id="e3b55-105">Der Parametersatz für den Richtliniensatz-Definitionsnamen.</span><span class="sxs-lookup"><span data-stu-id="e3b55-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="e3b55-106">Standard</span><span class="sxs-lookup"><span data-stu-id="e3b55-106">(Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b55-107">Der Parametersatz für die Richtliniensatz-Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="e3b55-107">The policy set definition Id parameter set.</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3b55-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3b55-108">DESCRIPTION</span></span>
<span data-ttu-id="e3b55-109">Das Cmdlet **Remove-AzureRmPolicySetDefinition** entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="e3b55-109">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="e3b55-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3b55-110">EXAMPLES</span></span>

### <span data-ttu-id="e3b55-111">Beispiel 1: Entfernen der Richtliniensatz Definition nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e3b55-111">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="e3b55-112">Der erste Befehl ruft eine Richtliniensatz Definition mithilfe des Get-AzureRmPolicySetDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="e3b55-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="e3b55-113">Der Befehl speichert Sie in der $PolicySetDefinition-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e3b55-113">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="e3b55-114">Mit dem zweiten Befehl wird die Richtliniensatz Definition entfernt, die durch die **Resourcen** -Eigenschaft $PolicySetDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="e3b55-114">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="e3b55-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3b55-115">PARAMETERS</span></span>

### <span data-ttu-id="e3b55-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e3b55-116">-ApiVersion</span></span>
<span data-ttu-id="e3b55-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3b55-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e3b55-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e3b55-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e3b55-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e3b55-119">-Force</span></span>
<span data-ttu-id="e3b55-120">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="e3b55-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e3b55-121">-ID</span><span class="sxs-lookup"><span data-stu-id="e3b55-121">-Id</span></span>
<span data-ttu-id="e3b55-122">Die vollqualifizierte Richtliniensatz-Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="e3b55-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="e3b55-123">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="e3b55-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b55-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e3b55-124">-Name</span></span>
<span data-ttu-id="e3b55-125">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="e3b55-125">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b55-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="e3b55-126">-Pre</span></span>
<span data-ttu-id="e3b55-127">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="e3b55-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e3b55-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e3b55-128">-Confirm</span></span>
<span data-ttu-id="e3b55-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3b55-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3b55-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b55-130">-WhatIf</span></span>
<span data-ttu-id="e3b55-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3b55-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3b55-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3b55-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3b55-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b55-133">-DefaultProfile</span></span>
<span data-ttu-id="e3b55-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3b55-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3b55-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b55-135">CommonParameters</span></span>
<span data-ttu-id="e3b55-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b55-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b55-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b55-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b55-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3b55-138">INPUTS</span></span>

### <span data-ttu-id="e3b55-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e3b55-139">System.String</span></span>

## <span data-ttu-id="e3b55-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3b55-140">OUTPUTS</span></span>

### <span data-ttu-id="e3b55-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3b55-141">System.Boolean</span></span>

## <span data-ttu-id="e3b55-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3b55-142">NOTES</span></span>

## <span data-ttu-id="e3b55-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3b55-143">RELATED LINKS</span></span>

