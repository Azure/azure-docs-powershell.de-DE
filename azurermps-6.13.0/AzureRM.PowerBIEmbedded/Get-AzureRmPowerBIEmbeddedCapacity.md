---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4e15a9490fcaa41c77bb4ba822429646c6e45952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480202"
---
# <span data-ttu-id="31e19-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="31e19-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="31e19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31e19-102">SYNOPSIS</span></span>
<span data-ttu-id="31e19-103">Ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="31e19-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31e19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31e19-104">SYNTAX</span></span>

### <span data-ttu-id="31e19-105">ByCapacityOrResourceGroupOrSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="31e19-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31e19-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="31e19-106">ByResourceId</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31e19-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31e19-107">DESCRIPTION</span></span>
<span data-ttu-id="31e19-108">Das Get-AzureRmPowerBIEmbeddedCapacity-Cmdlet ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="31e19-108">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="31e19-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31e19-109">EXAMPLES</span></span>

### <span data-ttu-id="31e19-110">Beispiel 1: Abrufen von Ressourcengruppenkapazitäten</span><span class="sxs-lookup"><span data-stu-id="31e19-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/mycapacity
ResourceGroup          : testRG
Name                   : mycapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A4
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="31e19-111">Dieser Befehl ruft alle Azure PowerBI eingebettete Kapazität in der Ressourcengruppe mit dem Namen testRG</span><span class="sxs-lookup"><span data-stu-id="31e19-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="31e19-112">Beispiel 2: Abrufen einer Kapazität</span><span class="sxs-lookup"><span data-stu-id="31e19-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="31e19-113">Dieser Befehl ruft die eingebettete Azure PowerBI-Kapazität mit dem Namen testcapacity in der Ressourcengruppe mit dem Namen testRG.</span><span class="sxs-lookup"><span data-stu-id="31e19-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="31e19-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="31e19-114">PARAMETERS</span></span>

### <span data-ttu-id="31e19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e19-115">-DefaultProfile</span></span>
<span data-ttu-id="31e19-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31e19-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31e19-117">-Name</span><span class="sxs-lookup"><span data-stu-id="31e19-117">-Name</span></span>
<span data-ttu-id="31e19-118">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="31e19-118">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e19-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e19-119">-ResourceGroupName</span></span>
<span data-ttu-id="31e19-120">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="31e19-120">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e19-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="31e19-121">-ResourceId</span></span>
<span data-ttu-id="31e19-122">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="31e19-122">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31e19-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e19-123">CommonParameters</span></span>
<span data-ttu-id="31e19-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e19-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e19-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e19-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e19-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31e19-126">INPUTS</span></span>

### <span data-ttu-id="31e19-127">System. String</span><span class="sxs-lookup"><span data-stu-id="31e19-127">System.String</span></span>

## <span data-ttu-id="31e19-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31e19-128">OUTPUTS</span></span>

### <span data-ttu-id="31e19-129">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="31e19-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="31e19-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="31e19-130">NOTES</span></span>

## <span data-ttu-id="31e19-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31e19-131">RELATED LINKS</span></span>

[<span data-ttu-id="31e19-132">Neu – AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="31e19-132">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="31e19-133">Remove-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="31e19-133">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
