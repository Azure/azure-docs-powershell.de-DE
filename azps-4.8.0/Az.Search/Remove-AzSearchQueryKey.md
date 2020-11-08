---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: e7a74fcc6d5e1a80282cfb365070df1b339aea45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166100"
---
# <span data-ttu-id="126ca-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="126ca-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="126ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="126ca-102">SYNOPSIS</span></span>
<span data-ttu-id="126ca-103">Entfernen Sie den Abfrage Schlüssel aus dem Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="126ca-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="126ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="126ca-104">SYNTAX</span></span>

### <span data-ttu-id="126ca-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="126ca-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="126ca-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="126ca-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="126ca-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="126ca-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="126ca-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="126ca-108">DESCRIPTION</span></span>
<span data-ttu-id="126ca-109">Das Cmdlet **Remove-AzSearchQueryKey** entfernt den Abfrage Schlüssel aus dem Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="126ca-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="126ca-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="126ca-110">EXAMPLES</span></span>

### <span data-ttu-id="126ca-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="126ca-111">Example 1</span></span>
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

<span data-ttu-id="126ca-112">Im Beispiel wird der Abfrage Schlüssel aus dem Azure-Suchdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="126ca-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="126ca-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="126ca-113">PARAMETERS</span></span>

### <span data-ttu-id="126ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="126ca-114">-DefaultProfile</span></span>
<span data-ttu-id="126ca-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="126ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="126ca-116">-Force</span><span class="sxs-lookup"><span data-stu-id="126ca-116">-Force</span></span>
<span data-ttu-id="126ca-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="126ca-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="126ca-118">-Keywert</span><span class="sxs-lookup"><span data-stu-id="126ca-118">-KeyValue</span></span>
<span data-ttu-id="126ca-119">Suchdienst Abfrage-Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="126ca-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="126ca-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="126ca-120">-ParentObject</span></span>
<span data-ttu-id="126ca-121">Suchdienst Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="126ca-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="126ca-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="126ca-122">-ParentResourceId</span></span>
<span data-ttu-id="126ca-123">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="126ca-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="126ca-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="126ca-124">-PassThru</span></span>
<span data-ttu-id="126ca-125">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="126ca-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="126ca-126">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="126ca-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="126ca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="126ca-127">-ResourceGroupName</span></span>
<span data-ttu-id="126ca-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="126ca-128">Resource Group name.</span></span>

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

### <span data-ttu-id="126ca-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="126ca-129">-ServiceName</span></span>
<span data-ttu-id="126ca-130">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="126ca-130">Search Service name.</span></span>

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

### <span data-ttu-id="126ca-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="126ca-131">-Confirm</span></span>
<span data-ttu-id="126ca-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="126ca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="126ca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="126ca-133">-WhatIf</span></span>
<span data-ttu-id="126ca-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="126ca-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="126ca-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="126ca-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="126ca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="126ca-136">CommonParameters</span></span>
<span data-ttu-id="126ca-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="126ca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="126ca-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="126ca-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="126ca-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="126ca-139">INPUTS</span></span>

### <span data-ttu-id="126ca-140">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="126ca-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="126ca-141">System. String</span><span class="sxs-lookup"><span data-stu-id="126ca-141">System.String</span></span>

## <span data-ttu-id="126ca-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="126ca-142">OUTPUTS</span></span>

### <span data-ttu-id="126ca-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="126ca-143">System.Boolean</span></span>

## <span data-ttu-id="126ca-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="126ca-144">NOTES</span></span>

## <span data-ttu-id="126ca-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="126ca-145">RELATED LINKS</span></span>

[<span data-ttu-id="126ca-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="126ca-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="126ca-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="126ca-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
