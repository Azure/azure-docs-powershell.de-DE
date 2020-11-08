---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: e7a74fcc6d5e1a80282cfb365070df1b339aea45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178394"
---
# <span data-ttu-id="e6019-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="e6019-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="e6019-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6019-102">SYNOPSIS</span></span>
<span data-ttu-id="e6019-103">Entfernen Sie den Abfrage Schlüssel aus dem Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="e6019-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="e6019-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6019-104">SYNTAX</span></span>

### <span data-ttu-id="e6019-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6019-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6019-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6019-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6019-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6019-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6019-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6019-108">DESCRIPTION</span></span>
<span data-ttu-id="e6019-109">Das Cmdlet **Remove-AzSearchQueryKey** entfernt den Abfrage Schlüssel aus dem Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="e6019-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="e6019-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6019-110">EXAMPLES</span></span>

### <span data-ttu-id="e6019-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e6019-111">Example 1</span></span>
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

<span data-ttu-id="e6019-112">Im Beispiel wird der Abfrage Schlüssel aus dem Azure-Suchdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="e6019-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="e6019-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6019-113">PARAMETERS</span></span>

### <span data-ttu-id="e6019-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6019-114">-DefaultProfile</span></span>
<span data-ttu-id="e6019-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e6019-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6019-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e6019-116">-Force</span></span>
<span data-ttu-id="e6019-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="e6019-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e6019-118">-Keywert</span><span class="sxs-lookup"><span data-stu-id="e6019-118">-KeyValue</span></span>
<span data-ttu-id="e6019-119">Suchdienst Abfrage-Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="e6019-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="e6019-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e6019-120">-ParentObject</span></span>
<span data-ttu-id="e6019-121">Suchdienst Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="e6019-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="e6019-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e6019-122">-ParentResourceId</span></span>
<span data-ttu-id="e6019-123">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="e6019-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="e6019-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6019-124">-PassThru</span></span>
<span data-ttu-id="e6019-125">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="e6019-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="e6019-126">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e6019-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e6019-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6019-127">-ResourceGroupName</span></span>
<span data-ttu-id="e6019-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e6019-128">Resource Group name.</span></span>

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

### <span data-ttu-id="e6019-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e6019-129">-ServiceName</span></span>
<span data-ttu-id="e6019-130">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="e6019-130">Search Service name.</span></span>

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

### <span data-ttu-id="e6019-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e6019-131">-Confirm</span></span>
<span data-ttu-id="e6019-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6019-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6019-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6019-133">-WhatIf</span></span>
<span data-ttu-id="e6019-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6019-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6019-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6019-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6019-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6019-136">CommonParameters</span></span>
<span data-ttu-id="e6019-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6019-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6019-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6019-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6019-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6019-139">INPUTS</span></span>

### <span data-ttu-id="e6019-140">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="e6019-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="e6019-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e6019-141">System.String</span></span>

## <span data-ttu-id="e6019-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6019-142">OUTPUTS</span></span>

### <span data-ttu-id="e6019-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6019-143">System.Boolean</span></span>

## <span data-ttu-id="e6019-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6019-144">NOTES</span></span>

## <span data-ttu-id="e6019-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6019-145">RELATED LINKS</span></span>

[<span data-ttu-id="e6019-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="e6019-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="e6019-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="e6019-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
