---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: e7a74fcc6d5e1a80282cfb365070df1b339aea45
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306912"
---
# <span data-ttu-id="80bee-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="80bee-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="80bee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80bee-102">SYNOPSIS</span></span>
<span data-ttu-id="80bee-103">Entfernen Sie den Abfrageschlüssel aus dem Azure Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="80bee-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="80bee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80bee-104">SYNTAX</span></span>

### <span data-ttu-id="80bee-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="80bee-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80bee-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80bee-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80bee-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80bee-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80bee-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80bee-108">DESCRIPTION</span></span>
<span data-ttu-id="80bee-109">Das **Cmdlet "Remove-AzSearchQueryKey"** entfernt den Abfrageschlüssel aus dem Azure Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="80bee-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="80bee-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="80bee-110">EXAMPLES</span></span>

### <span data-ttu-id="80bee-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="80bee-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="80bee-112">Im Beispiel wird der Abfrageschlüssel aus dem Azure Search-Dienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="80bee-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="80bee-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80bee-113">PARAMETERS</span></span>

### <span data-ttu-id="80bee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80bee-114">-DefaultProfile</span></span>
<span data-ttu-id="80bee-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80bee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80bee-116">-Force</span><span class="sxs-lookup"><span data-stu-id="80bee-116">-Force</span></span>
<span data-ttu-id="80bee-117">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="80bee-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="80bee-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="80bee-118">-KeyValue</span></span>
<span data-ttu-id="80bee-119">Suchdienstabfrageschlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="80bee-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="80bee-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="80bee-120">-ParentObject</span></span>
<span data-ttu-id="80bee-121">Suchdiensteingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="80bee-121">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80bee-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="80bee-122">-ParentResourceId</span></span>
<span data-ttu-id="80bee-123">Suchdienstressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="80bee-123">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80bee-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80bee-124">-PassThru</span></span>
<span data-ttu-id="80bee-125">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="80bee-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="80bee-126">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="80bee-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="80bee-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80bee-127">-ResourceGroupName</span></span>
<span data-ttu-id="80bee-128">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="80bee-128">Resource Group name.</span></span>

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

### <span data-ttu-id="80bee-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="80bee-129">-ServiceName</span></span>
<span data-ttu-id="80bee-130">Name des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="80bee-130">Search Service name.</span></span>

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

### <span data-ttu-id="80bee-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80bee-131">-Confirm</span></span>
<span data-ttu-id="80bee-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80bee-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80bee-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="80bee-133">-WhatIf</span></span>
<span data-ttu-id="80bee-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80bee-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80bee-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80bee-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80bee-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80bee-136">CommonParameters</span></span>
<span data-ttu-id="80bee-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80bee-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80bee-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80bee-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80bee-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="80bee-139">INPUTS</span></span>

### <span data-ttu-id="80bee-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="80bee-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="80bee-141">System.String</span><span class="sxs-lookup"><span data-stu-id="80bee-141">System.String</span></span>

## <span data-ttu-id="80bee-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="80bee-142">OUTPUTS</span></span>

### <span data-ttu-id="80bee-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="80bee-143">System.Boolean</span></span>

## <span data-ttu-id="80bee-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="80bee-144">NOTES</span></span>

## <span data-ttu-id="80bee-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="80bee-145">RELATED LINKS</span></span>

[<span data-ttu-id="80bee-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="80bee-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="80bee-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="80bee-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
