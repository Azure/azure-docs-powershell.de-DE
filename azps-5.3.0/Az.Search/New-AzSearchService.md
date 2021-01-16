---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460780"
---
# <span data-ttu-id="4b57f-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4b57f-101">New-AzSearchService</span></span>

## <span data-ttu-id="4b57f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b57f-102">SYNOPSIS</span></span>
<span data-ttu-id="4b57f-103">Erstellt einen Azure Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="4b57f-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="4b57f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b57f-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b57f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b57f-105">DESCRIPTION</span></span>
<span data-ttu-id="4b57f-106">Das **Cmdlet "New-AzSearchService"** erstellt einen Azure Search-Dienst mit angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="4b57f-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="4b57f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b57f-107">EXAMPLES</span></span>

### <span data-ttu-id="4b57f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4b57f-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="4b57f-109">Der Befehl erstellt einen Azure Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="4b57f-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="4b57f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b57f-110">PARAMETERS</span></span>

### <span data-ttu-id="4b57f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b57f-111">-DefaultProfile</span></span>
<span data-ttu-id="4b57f-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b57f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b57f-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="4b57f-113">-HostingMode</span></span>
<span data-ttu-id="4b57f-114">Suchdiensthostingmodus.</span><span class="sxs-lookup"><span data-stu-id="4b57f-114">Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b57f-115">-Location</span><span class="sxs-lookup"><span data-stu-id="4b57f-115">-Location</span></span>
<span data-ttu-id="4b57f-116">Speicherort des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="4b57f-116">Search Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b57f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4b57f-117">-Name</span></span>
<span data-ttu-id="4b57f-118">Name des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="4b57f-118">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b57f-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="4b57f-119">-PartitionCount</span></span>
<span data-ttu-id="4b57f-120">Anzahl der Suchdienstpartitionen.</span><span class="sxs-lookup"><span data-stu-id="4b57f-120">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b57f-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="4b57f-121">-ReplicaCount</span></span>
<span data-ttu-id="4b57f-122">Anzahl der Suchdienstreplikate.</span><span class="sxs-lookup"><span data-stu-id="4b57f-122">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b57f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b57f-123">-ResourceGroupName</span></span>
<span data-ttu-id="4b57f-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4b57f-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b57f-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="4b57f-125">-Sku</span></span>
<span data-ttu-id="4b57f-126">Suchdienst-SKU.</span><span class="sxs-lookup"><span data-stu-id="4b57f-126">Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b57f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b57f-127">-Confirm</span></span>
<span data-ttu-id="4b57f-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b57f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b57f-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4b57f-129">-WhatIf</span></span>
<span data-ttu-id="4b57f-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b57f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b57f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b57f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b57f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b57f-132">CommonParameters</span></span>
<span data-ttu-id="4b57f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b57f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b57f-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b57f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b57f-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b57f-135">INPUTS</span></span>

### <span data-ttu-id="4b57f-136">Keine</span><span class="sxs-lookup"><span data-stu-id="4b57f-136">None</span></span>

## <span data-ttu-id="4b57f-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b57f-137">OUTPUTS</span></span>

### <span data-ttu-id="4b57f-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="4b57f-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="4b57f-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4b57f-139">NOTES</span></span>

## <span data-ttu-id="4b57f-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4b57f-140">RELATED LINKS</span></span>

[<span data-ttu-id="4b57f-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4b57f-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="4b57f-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4b57f-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="4b57f-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4b57f-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)