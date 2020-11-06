---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
ms.openlocfilehash: 417e1a546777824df86b72f3740079ac91835192
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500129"
---
# <span data-ttu-id="5deb9-101">New-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="5deb9-101">New-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="5deb9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5deb9-102">SYNOPSIS</span></span>
<span data-ttu-id="5deb9-103">Erstellen Sie einen neuen Abfrage Schlüssel für den Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="5deb9-103">Create a new query key for the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5deb9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5deb9-104">SYNTAX</span></span>

### <span data-ttu-id="5deb9-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5deb9-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5deb9-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5deb9-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5deb9-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5deb9-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentResourceId] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5deb9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5deb9-108">DESCRIPTION</span></span>
<span data-ttu-id="5deb9-109">Das Cmdlet **New-AzureRmSearchQueryKey** erstellt einen neuen Abfrage Schlüssel für den Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="5deb9-109">The **New-AzureRmSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="5deb9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5deb9-110">EXAMPLES</span></span>

### <span data-ttu-id="5deb9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5deb9-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="5deb9-112">Im Beispiel wird ein neuer Abfrage Schlüssel für den Azure-Suchdienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="5deb9-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="5deb9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5deb9-113">PARAMETERS</span></span>

### <span data-ttu-id="5deb9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5deb9-114">-DefaultProfile</span></span>
<span data-ttu-id="5deb9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5deb9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5deb9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5deb9-116">-Name</span></span>
<span data-ttu-id="5deb9-117">Name des Suchdienst Abfrage Schlüssels</span><span class="sxs-lookup"><span data-stu-id="5deb9-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="5deb9-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5deb9-118">-ParentObject</span></span>
<span data-ttu-id="5deb9-119">Suchdienst Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="5deb9-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="5deb9-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5deb9-120">-ParentResourceId</span></span>
<span data-ttu-id="5deb9-121">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="5deb9-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="5deb9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5deb9-122">-ResourceGroupName</span></span>
<span data-ttu-id="5deb9-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5deb9-123">Resource Group name.</span></span>

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

### <span data-ttu-id="5deb9-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5deb9-124">-ServiceName</span></span>
<span data-ttu-id="5deb9-125">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="5deb9-125">Search Service name.</span></span>

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

### <span data-ttu-id="5deb9-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5deb9-126">-Confirm</span></span>
<span data-ttu-id="5deb9-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5deb9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5deb9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5deb9-128">-WhatIf</span></span>
<span data-ttu-id="5deb9-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5deb9-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5deb9-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5deb9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5deb9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5deb9-131">CommonParameters</span></span>
<span data-ttu-id="5deb9-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5deb9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5deb9-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5deb9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5deb9-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5deb9-134">INPUTS</span></span>

### <span data-ttu-id="5deb9-135">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="5deb9-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="5deb9-136">Parameter: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5deb9-136">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="5deb9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5deb9-137">System.String</span></span>

## <span data-ttu-id="5deb9-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5deb9-138">OUTPUTS</span></span>

### <span data-ttu-id="5deb9-139">Microsoft. Azure. Commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="5deb9-139">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="5deb9-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="5deb9-140">NOTES</span></span>

## <span data-ttu-id="5deb9-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5deb9-141">RELATED LINKS</span></span>

[<span data-ttu-id="5deb9-142">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="5deb9-142">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)

[<span data-ttu-id="5deb9-143">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="5deb9-143">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
