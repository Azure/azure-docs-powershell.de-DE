---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 67c5ccb24267825313612cc539f243551ad1894e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659480"
---
# <span data-ttu-id="bca7b-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="bca7b-101">New-AzSearchService</span></span>

## <span data-ttu-id="bca7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bca7b-102">SYNOPSIS</span></span>
<span data-ttu-id="bca7b-103">Erstellt einen Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="bca7b-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="bca7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bca7b-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bca7b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bca7b-105">DESCRIPTION</span></span>
<span data-ttu-id="bca7b-106">Das Cmdlet **New-AzSearchService** erstellt einen Azure-Suchdienst mit angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="bca7b-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="bca7b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bca7b-107">EXAMPLES</span></span>

### <span data-ttu-id="bca7b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bca7b-108">Example 1</span></span>
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

<span data-ttu-id="bca7b-109">Der Befehl erstellt einen Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="bca7b-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="bca7b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bca7b-110">PARAMETERS</span></span>

### <span data-ttu-id="bca7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca7b-111">-DefaultProfile</span></span>
<span data-ttu-id="bca7b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bca7b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bca7b-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="bca7b-113">-HostingMode</span></span>
<span data-ttu-id="bca7b-114">Search Service Hosting-Modus.</span><span class="sxs-lookup"><span data-stu-id="bca7b-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="bca7b-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="bca7b-115">-Location</span></span>
<span data-ttu-id="bca7b-116">Suchdienst Standort.</span><span class="sxs-lookup"><span data-stu-id="bca7b-116">Search Service location.</span></span>

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

### <span data-ttu-id="bca7b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bca7b-117">-Name</span></span>
<span data-ttu-id="bca7b-118">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="bca7b-118">Search Service name.</span></span>

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

### <span data-ttu-id="bca7b-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="bca7b-119">-PartitionCount</span></span>
<span data-ttu-id="bca7b-120">Anzahl der Suchdienst Partitionen</span><span class="sxs-lookup"><span data-stu-id="bca7b-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="bca7b-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="bca7b-121">-ReplicaCount</span></span>
<span data-ttu-id="bca7b-122">Anzahl der Suchdienst Replikate</span><span class="sxs-lookup"><span data-stu-id="bca7b-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="bca7b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bca7b-123">-ResourceGroupName</span></span>
<span data-ttu-id="bca7b-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bca7b-124">Resource Group name.</span></span>

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

### <span data-ttu-id="bca7b-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="bca7b-125">-Sku</span></span>
<span data-ttu-id="bca7b-126">Suchdienst-SKU.</span><span class="sxs-lookup"><span data-stu-id="bca7b-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="bca7b-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bca7b-127">-Confirm</span></span>
<span data-ttu-id="bca7b-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bca7b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bca7b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bca7b-129">-WhatIf</span></span>
<span data-ttu-id="bca7b-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bca7b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bca7b-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bca7b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bca7b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca7b-132">CommonParameters</span></span>
<span data-ttu-id="bca7b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bca7b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca7b-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bca7b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca7b-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bca7b-135">INPUTS</span></span>

### <span data-ttu-id="bca7b-136">Keine</span><span class="sxs-lookup"><span data-stu-id="bca7b-136">None</span></span>

## <span data-ttu-id="bca7b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bca7b-137">OUTPUTS</span></span>

### <span data-ttu-id="bca7b-138">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="bca7b-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="bca7b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="bca7b-139">NOTES</span></span>

## <span data-ttu-id="bca7b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bca7b-140">RELATED LINKS</span></span>

[<span data-ttu-id="bca7b-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="bca7b-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="bca7b-142">Satz-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="bca7b-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="bca7b-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="bca7b-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)