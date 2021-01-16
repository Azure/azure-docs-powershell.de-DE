---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297569"
---
# <span data-ttu-id="84932-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="84932-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="84932-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84932-102">SYNOPSIS</span></span>
<span data-ttu-id="84932-103">Erstellen oder Aktualisieren einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="84932-103">Create or update an association.</span></span>

## <span data-ttu-id="84932-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84932-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="84932-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84932-105">DESCRIPTION</span></span>
<span data-ttu-id="84932-106">Erstellen oder Aktualisieren einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="84932-106">Create or update an association.</span></span>

## <span data-ttu-id="84932-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="84932-107">EXAMPLES</span></span>

### <span data-ttu-id="84932-108">Beispiel 1: Erstellen einer benutzerdefinierten Anbieter zuordnung</span><span class="sxs-lookup"><span data-stu-id="84932-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="84932-109">Wenn Sie eine benutzerdefinierte Anbieterzuordnung erstellen, muss der zugeordnete Zielprovioder ordnungsgemäß mit einer Route für "Zuordnungen" konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="84932-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="84932-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84932-110">PARAMETERS</span></span>

### <span data-ttu-id="84932-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84932-111">-AsJob</span></span>
<span data-ttu-id="84932-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="84932-112">Run the command as a job</span></span>

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

### <span data-ttu-id="84932-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84932-113">-DefaultProfile</span></span>
<span data-ttu-id="84932-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84932-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84932-115">-Name</span><span class="sxs-lookup"><span data-stu-id="84932-115">-Name</span></span>
<span data-ttu-id="84932-116">Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="84932-116">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84932-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="84932-117">-NoWait</span></span>
<span data-ttu-id="84932-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="84932-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="84932-119">-Scope</span><span class="sxs-lookup"><span data-stu-id="84932-119">-Scope</span></span>
<span data-ttu-id="84932-120">Der Umfang der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="84932-120">The scope of the association.</span></span>
<span data-ttu-id="84932-121">Der Bereich kann eine beliebige gültige REST-Ressourceninstanz sein.</span><span class="sxs-lookup"><span data-stu-id="84932-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="84932-122">Verwenden Sie z. B. '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' für eine Ressource des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="84932-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84932-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="84932-123">-TargetResourceId</span></span>
<span data-ttu-id="84932-124">Die REST-Ressourceninstanz der Zielressource für diese Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="84932-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="84932-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84932-125">-Confirm</span></span>
<span data-ttu-id="84932-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84932-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84932-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="84932-127">-WhatIf</span></span>
<span data-ttu-id="84932-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84932-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84932-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84932-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84932-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84932-130">CommonParameters</span></span>
<span data-ttu-id="84932-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84932-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84932-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84932-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84932-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="84932-133">INPUTS</span></span>

## <span data-ttu-id="84932-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="84932-134">OUTPUTS</span></span>

### <span data-ttu-id="84932-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="84932-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="84932-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="84932-136">NOTES</span></span>

<span data-ttu-id="84932-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="84932-137">ALIASES</span></span>

## <span data-ttu-id="84932-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="84932-138">RELATED LINKS</span></span>

