---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: e01e5e244bd34e3e18aa287e0f2f5709c5e208ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165611"
---
# <span data-ttu-id="78f96-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="78f96-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="78f96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78f96-102">SYNOPSIS</span></span>
<span data-ttu-id="78f96-103">Erstellen Sie einen neuen Abfrage Schlüssel für den Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="78f96-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="78f96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78f96-104">SYNTAX</span></span>

### <span data-ttu-id="78f96-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="78f96-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f96-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78f96-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f96-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78f96-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78f96-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78f96-108">DESCRIPTION</span></span>
<span data-ttu-id="78f96-109">Das Cmdlet **New-AzSearchQueryKey** erstellt einen neuen Abfrage Schlüssel für den Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="78f96-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="78f96-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78f96-110">EXAMPLES</span></span>

### <span data-ttu-id="78f96-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78f96-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="78f96-112">Im Beispiel wird ein neuer Abfrage Schlüssel für den Azure-Suchdienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="78f96-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="78f96-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="78f96-113">PARAMETERS</span></span>

### <span data-ttu-id="78f96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f96-114">-DefaultProfile</span></span>
<span data-ttu-id="78f96-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78f96-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78f96-116">-Name</span><span class="sxs-lookup"><span data-stu-id="78f96-116">-Name</span></span>
<span data-ttu-id="78f96-117">Name des Suchdienst Abfrage Schlüssels</span><span class="sxs-lookup"><span data-stu-id="78f96-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="78f96-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="78f96-118">-ParentObject</span></span>
<span data-ttu-id="78f96-119">Suchdienst Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="78f96-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="78f96-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="78f96-120">-ParentResourceId</span></span>
<span data-ttu-id="78f96-121">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="78f96-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="78f96-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f96-122">-ResourceGroupName</span></span>
<span data-ttu-id="78f96-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78f96-123">Resource Group name.</span></span>

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

### <span data-ttu-id="78f96-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="78f96-124">-ServiceName</span></span>
<span data-ttu-id="78f96-125">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="78f96-125">Search Service name.</span></span>

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

### <span data-ttu-id="78f96-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78f96-126">-Confirm</span></span>
<span data-ttu-id="78f96-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78f96-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f96-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f96-128">-WhatIf</span></span>
<span data-ttu-id="78f96-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78f96-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78f96-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78f96-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78f96-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f96-131">CommonParameters</span></span>
<span data-ttu-id="78f96-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f96-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f96-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78f96-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f96-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78f96-134">INPUTS</span></span>

### <span data-ttu-id="78f96-135">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="78f96-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="78f96-136">System. String</span><span class="sxs-lookup"><span data-stu-id="78f96-136">System.String</span></span>

## <span data-ttu-id="78f96-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78f96-137">OUTPUTS</span></span>

### <span data-ttu-id="78f96-138">Microsoft. Azure. Commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="78f96-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="78f96-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="78f96-139">NOTES</span></span>

## <span data-ttu-id="78f96-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78f96-140">RELATED LINKS</span></span>

[<span data-ttu-id="78f96-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="78f96-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="78f96-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="78f96-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
