---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/set-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
ms.openlocfilehash: c938dd611d9f6d731c07d5aee76cb390838f4679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482073"
---
# <span data-ttu-id="5f450-101">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="5f450-101">Set-AzureRmSearchService</span></span>

## <span data-ttu-id="5f450-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f450-102">SYNOPSIS</span></span>
<span data-ttu-id="5f450-103">Aktualisieren eines Azure-Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="5f450-103">Update an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f450-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f450-104">SYNTAX</span></span>

### <span data-ttu-id="5f450-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f450-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f450-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f450-106">InputObjectParameterSet</span></span>
```
Set-AzureRmSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f450-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f450-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f450-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f450-108">DESCRIPTION</span></span>
<span data-ttu-id="5f450-109">Das Cmdlet " **Satz-AzureRmSearchService** " ändert einen Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="5f450-109">The **Set-AzureRmSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="5f450-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f450-110">EXAMPLES</span></span>

### <span data-ttu-id="5f450-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f450-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="5f450-112">Im Beispiel werden die Partitionsanzahl und die Replikat Anzahl des Azure Search-Diensts auf 2 geändert.</span><span class="sxs-lookup"><span data-stu-id="5f450-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="5f450-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f450-113">PARAMETERS</span></span>

### <span data-ttu-id="5f450-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f450-114">-DefaultProfile</span></span>
<span data-ttu-id="5f450-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f450-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f450-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f450-116">-InputObject</span></span>
<span data-ttu-id="5f450-117">Suchdienst Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="5f450-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="5f450-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5f450-118">-Name</span></span>
<span data-ttu-id="5f450-119">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="5f450-119">Search Service name.</span></span>

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

### <span data-ttu-id="5f450-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="5f450-120">-PartitionCount</span></span>
<span data-ttu-id="5f450-121">Anzahl der Suchdienst Partitionen</span><span class="sxs-lookup"><span data-stu-id="5f450-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="5f450-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="5f450-122">-ReplicaCount</span></span>
<span data-ttu-id="5f450-123">Anzahl der Suchdienst Replikate</span><span class="sxs-lookup"><span data-stu-id="5f450-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="5f450-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f450-124">-ResourceGroupName</span></span>
<span data-ttu-id="5f450-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5f450-125">Resource Group name.</span></span>

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

### <span data-ttu-id="5f450-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5f450-126">-ResourceId</span></span>
<span data-ttu-id="5f450-127">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="5f450-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="5f450-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f450-128">-Confirm</span></span>
<span data-ttu-id="5f450-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f450-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f450-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f450-130">-WhatIf</span></span>
<span data-ttu-id="5f450-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f450-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f450-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f450-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f450-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f450-133">CommonParameters</span></span>
<span data-ttu-id="5f450-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f450-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f450-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f450-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f450-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f450-136">INPUTS</span></span>

### <span data-ttu-id="5f450-137">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="5f450-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="5f450-138">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5f450-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5f450-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5f450-139">System.String</span></span>

## <span data-ttu-id="5f450-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f450-140">OUTPUTS</span></span>

### <span data-ttu-id="5f450-141">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="5f450-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="5f450-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f450-142">NOTES</span></span>

## <span data-ttu-id="5f450-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f450-143">RELATED LINKS</span></span>

[<span data-ttu-id="5f450-144">Neu – AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="5f450-144">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="5f450-145">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="5f450-145">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="5f450-146">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="5f450-146">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
