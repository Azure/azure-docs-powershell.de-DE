---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 0e1011fb8e2aaec7a77f735c961fa6ec2ede9dd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946457"
---
# <span data-ttu-id="eeb3d-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="eeb3d-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="eeb3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeb3d-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb3d-103">Entfernen Sie einen Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-103">Remove an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="eeb3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eeb3d-104">SYNTAX</span></span>

### <span data-ttu-id="eeb3d-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="eeb3d-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb3d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeb3d-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb3d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeb3d-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeb3d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eeb3d-108">DESCRIPTION</span></span>
<span data-ttu-id="eeb3d-109">Das **Cmdlet Remove-AzSearchService** entfernt einen Azure Cognitive Search-Dienst mit angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-109">The **Remove-AzSearchService** cmdlet removes an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="eeb3d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eeb3d-110">EXAMPLES</span></span>

### <span data-ttu-id="eeb3d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eeb3d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="eeb3d-112">Im Beispiel wird ein Azure Cognitive Search-Dienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-112">The example removes an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="eeb3d-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eeb3d-113">PARAMETERS</span></span>

### <span data-ttu-id="eeb3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb3d-114">-DefaultProfile</span></span>
<span data-ttu-id="eeb3d-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeb3d-116">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="eeb3d-116">-Force</span></span>
<span data-ttu-id="eeb3d-117">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eeb3d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eeb3d-118">-InputObject</span></span>
<span data-ttu-id="eeb3d-119">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-119">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="eeb3d-120">-Name</span></span>
<span data-ttu-id="eeb3d-121">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-121">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eeb3d-122">-PassThru</span></span>
<span data-ttu-id="eeb3d-123">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="eeb3d-124">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="eeb3d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeb3d-125">-ResourceGroupName</span></span>
<span data-ttu-id="eeb3d-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eeb3d-127">-ResourceId</span></span>
<span data-ttu-id="eeb3d-128">Azure Cognitive Search Service Resource Id.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-128">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3d-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eeb3d-129">-Confirm</span></span>
<span data-ttu-id="eeb3d-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb3d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb3d-131">-WhatIf</span></span>
<span data-ttu-id="eeb3d-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb3d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb3d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb3d-134">CommonParameters</span></span>
<span data-ttu-id="eeb3d-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb3d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb3d-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eeb3d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb3d-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eeb3d-137">INPUTS</span></span>

### <span data-ttu-id="eeb3d-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="eeb3d-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="eeb3d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="eeb3d-139">System.String</span></span>

## <span data-ttu-id="eeb3d-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eeb3d-140">OUTPUTS</span></span>

### <span data-ttu-id="eeb3d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eeb3d-141">System.Boolean</span></span>

## <span data-ttu-id="eeb3d-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eeb3d-142">NOTES</span></span>

## <span data-ttu-id="eeb3d-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eeb3d-143">RELATED LINKS</span></span>

[<span data-ttu-id="eeb3d-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="eeb3d-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="eeb3d-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="eeb3d-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="eeb3d-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="eeb3d-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)
