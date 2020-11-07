---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 3479a3d720554f0c062e2410d0c4b838f655909a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664211"
---
# <span data-ttu-id="75ff4-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="75ff4-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="75ff4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="75ff4-103">Entfernt eine verwaltete Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="75ff4-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75ff4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75ff4-104">SYNTAX</span></span>

### <span data-ttu-id="75ff4-105">RemoveByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="75ff4-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ff4-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="75ff4-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75ff4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75ff4-107">DESCRIPTION</span></span>
<span data-ttu-id="75ff4-108">Das Cmdlet " **Remove-AzureRmManagedApplicationDefinition** " entfernt eine verwaltete Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="75ff4-108">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="75ff4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75ff4-109">EXAMPLES</span></span>

### <span data-ttu-id="75ff4-110">Beispiel 1: Entfernen der Definition einer verwalteten Anwendung nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="75ff4-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="75ff4-111">Der erste Befehl ruft eine verwaltete Anwendungsdefinition mit dem Namen myAppDef mithilfe des Get-AzureRmManagedApplicationDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="75ff4-111">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="75ff4-112">Der Befehl speichert Sie in der $ApplicationDefinition-Variablen.</span><span class="sxs-lookup"><span data-stu-id="75ff4-112">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="75ff4-113">Mit dem zweiten Befehl wird die verwaltete Anwendungsdefinition entfernt, die durch die Eigenschaft " **Resourcen** " von $ApplicationDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="75ff4-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="75ff4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="75ff4-114">PARAMETERS</span></span>

### <span data-ttu-id="75ff4-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="75ff4-115">-ApiVersion</span></span>
<span data-ttu-id="75ff4-116">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="75ff4-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="75ff4-117">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="75ff4-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="75ff4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ff4-118">-DefaultProfile</span></span>
<span data-ttu-id="75ff4-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75ff4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75ff4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="75ff4-120">-Force</span></span>
<span data-ttu-id="75ff4-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="75ff4-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="75ff4-122">-ID</span><span class="sxs-lookup"><span data-stu-id="75ff4-122">-Id</span></span>
<span data-ttu-id="75ff4-123">Die vollqualifizierte Definitions-ID der verwalteten Anwendung einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="75ff4-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="75ff4-124">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="75ff4-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="75ff4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="75ff4-125">-Name</span></span>
<span data-ttu-id="75ff4-126">Der Definitionsname der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="75ff4-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="75ff4-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="75ff4-127">-Pre</span></span>
<span data-ttu-id="75ff4-128">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="75ff4-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="75ff4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75ff4-129">-ResourceGroupName</span></span>
<span data-ttu-id="75ff4-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="75ff4-130">The resource group name.</span></span>

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

### <span data-ttu-id="75ff4-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75ff4-131">-Confirm</span></span>
<span data-ttu-id="75ff4-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75ff4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75ff4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75ff4-133">-WhatIf</span></span>
<span data-ttu-id="75ff4-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75ff4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75ff4-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75ff4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75ff4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ff4-136">CommonParameters</span></span>
<span data-ttu-id="75ff4-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75ff4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ff4-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75ff4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ff4-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75ff4-139">INPUTS</span></span>

### <span data-ttu-id="75ff4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="75ff4-140">System.String</span></span>

## <span data-ttu-id="75ff4-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75ff4-141">OUTPUTS</span></span>

### <span data-ttu-id="75ff4-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="75ff4-142">System.Boolean</span></span>

## <span data-ttu-id="75ff4-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="75ff4-143">NOTES</span></span>

## <span data-ttu-id="75ff4-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75ff4-144">RELATED LINKS</span></span>
