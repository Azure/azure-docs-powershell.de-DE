---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: ce52463e9e983f3ad2483262775f5d4114370aa8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158636"
---
# <span data-ttu-id="25986-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="25986-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="25986-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25986-102">SYNOPSIS</span></span>
<span data-ttu-id="25986-103">Ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="25986-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="25986-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25986-104">SYNTAX</span></span>

### <span data-ttu-id="25986-105">ByCriptionOrResourceGroupOrSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="25986-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25986-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="25986-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25986-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25986-107">DESCRIPTION</span></span>
<span data-ttu-id="25986-108">Das Get-AzPowerBIEmbeddedCapacity cmdlet ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="25986-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="25986-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25986-109">EXAMPLES</span></span>

### <span data-ttu-id="25986-110">Beispiel 1: Ressourcengruppenressourcen erhalten</span><span class="sxs-lookup"><span data-stu-id="25986-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="25986-111">Dieser Befehl ruft alle eingebetteten Azure PowerBI-Kapazität in der Ressourcengruppe namens testRG ab.</span><span class="sxs-lookup"><span data-stu-id="25986-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="25986-112">Beispiel 2: Erhalten einer Kapazität</span><span class="sxs-lookup"><span data-stu-id="25986-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="25986-113">Mit diesem Befehl wird die eingebettete Azure PowerBI-Kapazität, die in der Ressourcengruppe "testRG" genannt wird, als Testkraft bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="25986-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="25986-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25986-114">PARAMETERS</span></span>

### <span data-ttu-id="25986-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25986-115">-DefaultProfile</span></span>
<span data-ttu-id="25986-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25986-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25986-117">-Name</span><span class="sxs-lookup"><span data-stu-id="25986-117">-Name</span></span>
<span data-ttu-id="25986-118">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="25986-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="25986-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25986-119">-ResourceGroupName</span></span>
<span data-ttu-id="25986-120">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="25986-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="25986-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25986-121">-ResourceId</span></span>
<span data-ttu-id="25986-122">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="25986-122">Azure resource ID</span></span>

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

### <span data-ttu-id="25986-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25986-123">CommonParameters</span></span>
<span data-ttu-id="25986-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25986-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25986-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25986-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25986-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25986-126">INPUTS</span></span>

### <span data-ttu-id="25986-127">System.String</span><span class="sxs-lookup"><span data-stu-id="25986-127">System.String</span></span>

## <span data-ttu-id="25986-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25986-128">OUTPUTS</span></span>

### <span data-ttu-id="25986-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbedded1</span><span class="sxs-lookup"><span data-stu-id="25986-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="25986-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="25986-130">NOTES</span></span>

## <span data-ttu-id="25986-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="25986-131">RELATED LINKS</span></span>

[<span data-ttu-id="25986-132">New-AzPowerBIEmbedded1 </span><span class="sxs-lookup"><span data-stu-id="25986-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="25986-133">Remove-AzPowerBIEmbedded1 </span><span class="sxs-lookup"><span data-stu-id="25986-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
