---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 17d7547daaffdfafc117a250d20c0af1f069b70f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919352"
---
# <span data-ttu-id="3ef30-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3ef30-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3ef30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ef30-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef30-103">Ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="3ef30-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="3ef30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ef30-104">SYNTAX</span></span>

### <span data-ttu-id="3ef30-105">ByCapacityOrResourceGroupOrSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ef30-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ef30-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ef30-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ef30-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ef30-107">DESCRIPTION</span></span>
<span data-ttu-id="3ef30-108">Das Get-AzPowerBIEmbeddedCapacity-Cmdlet ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="3ef30-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="3ef30-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ef30-109">EXAMPLES</span></span>

### <span data-ttu-id="3ef30-110">Beispiel 1: Ressourcengruppenkapazität erhalten</span><span class="sxs-lookup"><span data-stu-id="3ef30-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
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

<span data-ttu-id="3ef30-111">Dieser Befehl ruft alle eingebetteten Azure PowerBI-Kapazität in der Ressourcengruppe "testRG" ab.</span><span class="sxs-lookup"><span data-stu-id="3ef30-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="3ef30-112">Beispiel 2: Erhalten einer Kapazität</span><span class="sxs-lookup"><span data-stu-id="3ef30-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
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

<span data-ttu-id="3ef30-113">Dieser Befehl ruft die eingebettete Azure PowerBI-Kapazität mit dem Namen Testkapazität in der Ressourcengruppe mit dem Namen testRG ab.</span><span class="sxs-lookup"><span data-stu-id="3ef30-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="3ef30-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3ef30-114">PARAMETERS</span></span>

### <span data-ttu-id="3ef30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef30-115">-DefaultProfile</span></span>
<span data-ttu-id="3ef30-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ef30-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ef30-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3ef30-117">-Name</span></span>
<span data-ttu-id="3ef30-118">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="3ef30-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="3ef30-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ef30-119">-ResourceGroupName</span></span>
<span data-ttu-id="3ef30-120">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="3ef30-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="3ef30-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ef30-121">-ResourceId</span></span>
<span data-ttu-id="3ef30-122">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3ef30-122">Azure resource ID</span></span>

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

### <span data-ttu-id="3ef30-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef30-123">CommonParameters</span></span>
<span data-ttu-id="3ef30-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ef30-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef30-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ef30-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef30-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ef30-126">INPUTS</span></span>

### <span data-ttu-id="3ef30-127">System.String</span><span class="sxs-lookup"><span data-stu-id="3ef30-127">System.String</span></span>

## <span data-ttu-id="3ef30-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ef30-128">OUTPUTS</span></span>

### <span data-ttu-id="3ef30-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3ef30-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3ef30-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3ef30-130">NOTES</span></span>

## <span data-ttu-id="3ef30-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3ef30-131">RELATED LINKS</span></span>

[<span data-ttu-id="3ef30-132">New-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="3ef30-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="3ef30-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="3ef30-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
