---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 62b8dff0b2d5fc52b080b35e4a205ad2bb00ea52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459163"
---
# <span data-ttu-id="05be0-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="05be0-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="05be0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05be0-102">SYNOPSIS</span></span>
<span data-ttu-id="05be0-103">Entfernen Sie einen Azure Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="05be0-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="05be0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05be0-104">SYNTAX</span></span>

### <span data-ttu-id="05be0-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="05be0-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05be0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05be0-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05be0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05be0-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05be0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05be0-108">DESCRIPTION</span></span>
<span data-ttu-id="05be0-109">Das **Cmdlet "Remove-AzSearchService"** entfernt einen Azure Search-Dienst mit angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="05be0-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="05be0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="05be0-110">EXAMPLES</span></span>

### <span data-ttu-id="05be0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="05be0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="05be0-112">Im Beispiel wird ein Azure Search-Dienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="05be0-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="05be0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05be0-113">PARAMETERS</span></span>

### <span data-ttu-id="05be0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05be0-114">-DefaultProfile</span></span>
<span data-ttu-id="05be0-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05be0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05be0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="05be0-116">-Force</span></span>
<span data-ttu-id="05be0-117">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="05be0-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="05be0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05be0-118">-InputObject</span></span>
<span data-ttu-id="05be0-119">Suchdiensteingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="05be0-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="05be0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="05be0-120">-Name</span></span>
<span data-ttu-id="05be0-121">Name des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="05be0-121">Search Service name.</span></span>

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

### <span data-ttu-id="05be0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05be0-122">-PassThru</span></span>
<span data-ttu-id="05be0-123">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="05be0-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="05be0-124">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="05be0-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="05be0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05be0-125">-ResourceGroupName</span></span>
<span data-ttu-id="05be0-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="05be0-126">Resource Group name.</span></span>

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

### <span data-ttu-id="05be0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05be0-127">-ResourceId</span></span>
<span data-ttu-id="05be0-128">Suchdienstressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="05be0-128">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="05be0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05be0-129">-Confirm</span></span>
<span data-ttu-id="05be0-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05be0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05be0-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="05be0-131">-WhatIf</span></span>
<span data-ttu-id="05be0-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05be0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05be0-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05be0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05be0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05be0-134">CommonParameters</span></span>
<span data-ttu-id="05be0-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05be0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05be0-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05be0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05be0-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="05be0-137">INPUTS</span></span>

### <span data-ttu-id="05be0-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="05be0-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="05be0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="05be0-139">System.String</span></span>

## <span data-ttu-id="05be0-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="05be0-140">OUTPUTS</span></span>

### <span data-ttu-id="05be0-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="05be0-141">System.Boolean</span></span>

## <span data-ttu-id="05be0-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="05be0-142">NOTES</span></span>

## <span data-ttu-id="05be0-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="05be0-143">RELATED LINKS</span></span>

[<span data-ttu-id="05be0-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="05be0-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="05be0-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="05be0-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="05be0-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="05be0-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

