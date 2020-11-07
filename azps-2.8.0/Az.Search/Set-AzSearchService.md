---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: 5967ffbb5b0a39a771604c2f456de008d98de5fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823351"
---
# <span data-ttu-id="5b4ae-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="5b4ae-101">Set-AzSearchService</span></span>

## <span data-ttu-id="5b4ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b4ae-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4ae-103">Aktualisieren eines Azure-Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="5b4ae-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="5b4ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b4ae-104">SYNTAX</span></span>

### <span data-ttu-id="5b4ae-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b4ae-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4ae-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b4ae-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4ae-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b4ae-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b4ae-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b4ae-108">DESCRIPTION</span></span>
<span data-ttu-id="5b4ae-109">Das Cmdlet " **Satz-AzSearchService** " ändert einen Azure-Suchdienst.</span><span class="sxs-lookup"><span data-stu-id="5b4ae-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="5b4ae-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b4ae-110">EXAMPLES</span></span>

### <span data-ttu-id="5b4ae-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b4ae-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


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

<span data-ttu-id="5b4ae-112">Im Beispiel werden die Partitionsanzahl und die Replikat Anzahl des Azure Search-Diensts auf 2 geändert.</span><span class="sxs-lookup"><span data-stu-id="5b4ae-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="5b4ae-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b4ae-113">PARAMETERS</span></span>

### <span data-ttu-id="5b4ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b4ae-114">-DefaultProfile</span></span>
<span data-ttu-id="5b4ae-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b4ae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b4ae-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5b4ae-116">-InputObject</span></span>
<span data-ttu-id="5b4ae-117">Suchdienst Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="5b4ae-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="5b4ae-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5b4ae-118">-Name</span></span>
<span data-ttu-id="5b4ae-119">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="5b4ae-119">Search Service name.</span></span>

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

### <span data-ttu-id="5b4ae-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="5b4ae-120">-PartitionCount</span></span>
<span data-ttu-id="5b4ae-121">Anzahl der Suchdienst Partitionen</span><span class="sxs-lookup"><span data-stu-id="5b4ae-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="5b4ae-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="5b4ae-122">-ReplicaCount</span></span>
<span data-ttu-id="5b4ae-123">Anzahl der Suchdienst Replikate</span><span class="sxs-lookup"><span data-stu-id="5b4ae-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="5b4ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b4ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="5b4ae-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5b4ae-125">Resource Group name.</span></span>

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

### <span data-ttu-id="5b4ae-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5b4ae-126">-ResourceId</span></span>
<span data-ttu-id="5b4ae-127">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="5b4ae-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="5b4ae-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b4ae-128">-Confirm</span></span>
<span data-ttu-id="5b4ae-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b4ae-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b4ae-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b4ae-130">-WhatIf</span></span>
<span data-ttu-id="5b4ae-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b4ae-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b4ae-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b4ae-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b4ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b4ae-133">CommonParameters</span></span>
<span data-ttu-id="5b4ae-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b4ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b4ae-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b4ae-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b4ae-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b4ae-136">INPUTS</span></span>

### <span data-ttu-id="5b4ae-137">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="5b4ae-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="5b4ae-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5b4ae-138">System.String</span></span>

## <span data-ttu-id="5b4ae-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b4ae-139">OUTPUTS</span></span>

### <span data-ttu-id="5b4ae-140">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="5b4ae-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="5b4ae-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b4ae-141">NOTES</span></span>

## <span data-ttu-id="5b4ae-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b4ae-142">RELATED LINKS</span></span>

[<span data-ttu-id="5b4ae-143">Neu – AzSearchService</span><span class="sxs-lookup"><span data-stu-id="5b4ae-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="5b4ae-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="5b4ae-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="5b4ae-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="5b4ae-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)