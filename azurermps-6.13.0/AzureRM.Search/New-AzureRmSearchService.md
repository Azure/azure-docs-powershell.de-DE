---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchService.md
ms.openlocfilehash: 934ba85d438178ee636d5042f1fa145e63d60291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482078"
---
# <span data-ttu-id="a6b69-101">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="a6b69-101">New-AzureRmSearchService</span></span>

## <span data-ttu-id="a6b69-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6b69-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b69-103">Erstellt einen Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="a6b69-103">Creates an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6b69-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6b69-104">SYNTAX</span></span>

```
New-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6b69-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6b69-105">DESCRIPTION</span></span>
<span data-ttu-id="a6b69-106">Das Cmdlet **New-AzureRmSearchService** erstellt einen Azure-Suchdienst mit angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="a6b69-106">The **New-AzureRmSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="a6b69-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6b69-107">EXAMPLES</span></span>

### <span data-ttu-id="a6b69-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6b69-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


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

<span data-ttu-id="a6b69-109">Der Befehl erstellt einen Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="a6b69-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="a6b69-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6b69-110">PARAMETERS</span></span>

### <span data-ttu-id="a6b69-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b69-111">-DefaultProfile</span></span>
<span data-ttu-id="a6b69-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6b69-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6b69-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="a6b69-113">-HostingMode</span></span>
<span data-ttu-id="a6b69-114">Search Service Hosting-Modus.</span><span class="sxs-lookup"><span data-stu-id="a6b69-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="a6b69-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="a6b69-115">-Location</span></span>
<span data-ttu-id="a6b69-116">Suchdienst Standort.</span><span class="sxs-lookup"><span data-stu-id="a6b69-116">Search Service location.</span></span>

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

### <span data-ttu-id="a6b69-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a6b69-117">-Name</span></span>
<span data-ttu-id="a6b69-118">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="a6b69-118">Search Service name.</span></span>

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

### <span data-ttu-id="a6b69-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="a6b69-119">-PartitionCount</span></span>
<span data-ttu-id="a6b69-120">Anzahl der Suchdienst Partitionen</span><span class="sxs-lookup"><span data-stu-id="a6b69-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="a6b69-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="a6b69-121">-ReplicaCount</span></span>
<span data-ttu-id="a6b69-122">Anzahl der Suchdienst Replikate</span><span class="sxs-lookup"><span data-stu-id="a6b69-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="a6b69-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6b69-123">-ResourceGroupName</span></span>
<span data-ttu-id="a6b69-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a6b69-124">Resource Group name.</span></span>

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

### <span data-ttu-id="a6b69-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="a6b69-125">-Sku</span></span>
<span data-ttu-id="a6b69-126">Suchdienst-SKU.</span><span class="sxs-lookup"><span data-stu-id="a6b69-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="a6b69-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6b69-127">-Confirm</span></span>
<span data-ttu-id="a6b69-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6b69-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6b69-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6b69-129">-WhatIf</span></span>
<span data-ttu-id="a6b69-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6b69-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6b69-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6b69-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6b69-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b69-132">CommonParameters</span></span>
<span data-ttu-id="a6b69-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6b69-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b69-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6b69-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b69-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6b69-135">INPUTS</span></span>

### <span data-ttu-id="a6b69-136">Keine</span><span class="sxs-lookup"><span data-stu-id="a6b69-136">None</span></span>

## <span data-ttu-id="a6b69-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6b69-137">OUTPUTS</span></span>

### <span data-ttu-id="a6b69-138">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a6b69-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="a6b69-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6b69-139">NOTES</span></span>

## <span data-ttu-id="a6b69-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6b69-140">RELATED LINKS</span></span>

[<span data-ttu-id="a6b69-141">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="a6b69-141">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="a6b69-142">Satz-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="a6b69-142">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="a6b69-143">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="a6b69-143">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
