---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: a09dae99d7a2b6e08dd255cc19b859aec89808f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496929"
---
# <span data-ttu-id="70ea4-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="70ea4-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="70ea4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="70ea4-103">Ändert eine Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="70ea4-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70ea4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70ea4-104">SYNTAX</span></span>

### <span data-ttu-id="70ea4-105">Der Parametersatz für den Richtliniensatz-Definitionsnamen.</span><span class="sxs-lookup"><span data-stu-id="70ea4-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="70ea4-106">Standard</span><span class="sxs-lookup"><span data-stu-id="70ea4-106">(Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70ea4-107">Der Parametersatz für die Richtliniensatz-Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="70ea4-107">The policy set definition Id parameter set.</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70ea4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70ea4-108">DESCRIPTION</span></span>
<span data-ttu-id="70ea4-109">Das Cmdlet " **Satz-AzureRmPolicySetDefinition** " ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="70ea4-109">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="70ea4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70ea4-110">EXAMPLES</span></span>

### <span data-ttu-id="70ea4-111">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="70ea4-111">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="70ea4-112">Der erste Befehl ruft eine Richtliniensatz Definition mithilfe des Get-AzureRmPolicySetDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="70ea4-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="70ea4-113">Der Befehl speichert das Objekt in der $PolicySetDefinition Variablen.</span><span class="sxs-lookup"><span data-stu-id="70ea4-113">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="70ea4-114">Mit dem zweiten Befehl wird die Beschreibung der Richtliniensatz Definition aktualisiert, die durch die Eigenschaft " **Resourcen** " von $PolicySetDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="70ea4-114">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="70ea4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="70ea4-115">PARAMETERS</span></span>

### <span data-ttu-id="70ea4-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="70ea4-116">-ApiVersion</span></span>
<span data-ttu-id="70ea4-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70ea4-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="70ea4-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="70ea4-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="70ea4-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70ea4-119">-Description</span></span>
<span data-ttu-id="70ea4-120">Die Beschreibung für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="70ea4-120">The description for policy set definition.</span></span>

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

### <span data-ttu-id="70ea4-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="70ea4-121">-DisplayName</span></span>
<span data-ttu-id="70ea4-122">Der Anzeigename für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="70ea4-122">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="70ea4-123">-ID</span><span class="sxs-lookup"><span data-stu-id="70ea4-123">-Id</span></span>
<span data-ttu-id="70ea4-124">Die vollqualifizierte Richtlinien Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="70ea4-124">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="70ea4-125">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="70ea4-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="70ea4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="70ea4-126">-Name</span></span>
<span data-ttu-id="70ea4-127">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="70ea4-127">The policy set definition name.</span></span>

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

### <span data-ttu-id="70ea4-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="70ea4-128">-PolicyDefinition</span></span>
<span data-ttu-id="70ea4-129">Die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="70ea4-129">The policy set definition.</span></span> <span data-ttu-id="70ea4-130">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Richtlinien Definitionen enthält, oder die Richtliniensatz Definition als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="70ea4-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="70ea4-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="70ea4-131">-Pre</span></span>
<span data-ttu-id="70ea4-132">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="70ea4-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="70ea4-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="70ea4-133">-Confirm</span></span>
<span data-ttu-id="70ea4-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70ea4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70ea4-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ea4-135">-DefaultProfile</span></span>
<span data-ttu-id="70ea4-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70ea4-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70ea4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70ea4-137">-WhatIf</span></span>
<span data-ttu-id="70ea4-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70ea4-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70ea4-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70ea4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70ea4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ea4-140">CommonParameters</span></span>
<span data-ttu-id="70ea4-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ea4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ea4-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70ea4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ea4-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70ea4-143">INPUTS</span></span>

### <span data-ttu-id="70ea4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="70ea4-144">System.String</span></span>

## <span data-ttu-id="70ea4-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70ea4-145">OUTPUTS</span></span>

### <span data-ttu-id="70ea4-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="70ea4-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="70ea4-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="70ea4-147">NOTES</span></span>

## <span data-ttu-id="70ea4-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70ea4-148">RELATED LINKS</span></span>

