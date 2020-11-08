---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: ce52463e9e983f3ad2483262775f5d4114370aa8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178701"
---
# <span data-ttu-id="bca47-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bca47-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="bca47-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bca47-102">SYNOPSIS</span></span>
<span data-ttu-id="bca47-103">Ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="bca47-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="bca47-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bca47-104">SYNTAX</span></span>

### <span data-ttu-id="bca47-105">ByCapacityOrResourceGroupOrSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="bca47-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bca47-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bca47-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bca47-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bca47-107">DESCRIPTION</span></span>
<span data-ttu-id="bca47-108">Das Get-AzPowerBIEmbeddedCapacity-Cmdlet ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="bca47-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="bca47-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bca47-109">EXAMPLES</span></span>

### <span data-ttu-id="bca47-110">Beispiel 1: Abrufen von Ressourcengruppenkapazitäten</span><span class="sxs-lookup"><span data-stu-id="bca47-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="bca47-111">Dieser Befehl ruft alle Azure PowerBI eingebettete Kapazität in der Ressourcengruppe mit dem Namen testRG</span><span class="sxs-lookup"><span data-stu-id="bca47-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="bca47-112">Beispiel 2: Abrufen einer Kapazität</span><span class="sxs-lookup"><span data-stu-id="bca47-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="bca47-113">Dieser Befehl ruft die eingebettete Azure PowerBI-Kapazität mit dem Namen testcapacity in der Ressourcengruppe mit dem Namen testRG.</span><span class="sxs-lookup"><span data-stu-id="bca47-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="bca47-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="bca47-114">PARAMETERS</span></span>

### <span data-ttu-id="bca47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca47-115">-DefaultProfile</span></span>
<span data-ttu-id="bca47-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bca47-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bca47-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bca47-117">-Name</span></span>
<span data-ttu-id="bca47-118">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="bca47-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="bca47-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bca47-119">-ResourceGroupName</span></span>
<span data-ttu-id="bca47-120">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="bca47-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="bca47-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bca47-121">-ResourceId</span></span>
<span data-ttu-id="bca47-122">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="bca47-122">Azure resource ID</span></span>

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

### <span data-ttu-id="bca47-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca47-123">CommonParameters</span></span>
<span data-ttu-id="bca47-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bca47-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca47-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bca47-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca47-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bca47-126">INPUTS</span></span>

### <span data-ttu-id="bca47-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bca47-127">System.String</span></span>

## <span data-ttu-id="bca47-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bca47-128">OUTPUTS</span></span>

### <span data-ttu-id="bca47-129">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bca47-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="bca47-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="bca47-130">NOTES</span></span>

## <span data-ttu-id="bca47-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bca47-131">RELATED LINKS</span></span>

[<span data-ttu-id="bca47-132">Neu – AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="bca47-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="bca47-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="bca47-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
