---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 16a27c7756a25c4b8e4270a0c363f8a04528d12c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476593"
---
# <span data-ttu-id="23d64-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="23d64-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="23d64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23d64-102">SYNOPSIS</span></span>
<span data-ttu-id="23d64-103">Ändert eine Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="23d64-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23d64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23d64-104">SYNTAX</span></span>

### <span data-ttu-id="23d64-105">SetByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="23d64-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23d64-106">SetById</span><span class="sxs-lookup"><span data-stu-id="23d64-106">SetById</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23d64-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23d64-107">DESCRIPTION</span></span>
<span data-ttu-id="23d64-108">Das Cmdlet " **Satz-AzureRmPolicySetDefinition** " ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="23d64-108">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="23d64-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23d64-109">EXAMPLES</span></span>

### <span data-ttu-id="23d64-110">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="23d64-110">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="23d64-111">Der erste Befehl ruft eine Richtliniensatz Definition mithilfe des Get-AzureRmPolicySetDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="23d64-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="23d64-112">Der Befehl speichert das Objekt in der $PolicySetDefinition Variablen.</span><span class="sxs-lookup"><span data-stu-id="23d64-112">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="23d64-113">Mit dem zweiten Befehl wird die Beschreibung der Richtliniensatz Definition aktualisiert, die durch die Eigenschaft " **Resourcen** " von $PolicySetDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="23d64-113">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="23d64-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="23d64-114">PARAMETERS</span></span>

### <span data-ttu-id="23d64-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="23d64-115">-ApiVersion</span></span>
<span data-ttu-id="23d64-116">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="23d64-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="23d64-117">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="23d64-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="23d64-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d64-118">-DefaultProfile</span></span>
<span data-ttu-id="23d64-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="23d64-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23d64-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23d64-120">-Description</span></span>
<span data-ttu-id="23d64-121">Die Beschreibung für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="23d64-121">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d64-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="23d64-122">-DisplayName</span></span>
<span data-ttu-id="23d64-123">Der Anzeigename für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="23d64-123">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d64-124">-ID</span><span class="sxs-lookup"><span data-stu-id="23d64-124">-Id</span></span>
<span data-ttu-id="23d64-125">Die vollqualifizierte Richtlinien Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="23d64-125">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="23d64-126">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="23d64-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d64-127">-Name</span><span class="sxs-lookup"><span data-stu-id="23d64-127">-Name</span></span>
<span data-ttu-id="23d64-128">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="23d64-128">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d64-129">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23d64-129">-PolicyDefinition</span></span>
<span data-ttu-id="23d64-130">Die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="23d64-130">The policy set definition.</span></span> <span data-ttu-id="23d64-131">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Richtlinien Definitionen enthält, oder die Richtliniensatz Definition als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="23d64-131">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d64-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="23d64-132">-Pre</span></span>
<span data-ttu-id="23d64-133">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="23d64-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="23d64-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="23d64-134">-Confirm</span></span>
<span data-ttu-id="23d64-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23d64-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23d64-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23d64-136">-WhatIf</span></span>
<span data-ttu-id="23d64-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23d64-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23d64-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23d64-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23d64-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d64-139">CommonParameters</span></span>
<span data-ttu-id="23d64-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23d64-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d64-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23d64-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d64-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23d64-142">INPUTS</span></span>

### <span data-ttu-id="23d64-143">System. String</span><span class="sxs-lookup"><span data-stu-id="23d64-143">System.String</span></span>

## <span data-ttu-id="23d64-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23d64-144">OUTPUTS</span></span>

### <span data-ttu-id="23d64-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="23d64-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="23d64-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="23d64-146">NOTES</span></span>

## <span data-ttu-id="23d64-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23d64-147">RELATED LINKS</span></span>
