---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: ce52463e9e983f3ad2483262775f5d4114370aa8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308315"
---
# <span data-ttu-id="6814c-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6814c-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="6814c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6814c-102">SYNOPSIS</span></span>
<span data-ttu-id="6814c-103">Ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="6814c-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="6814c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6814c-104">SYNTAX</span></span>

### <span data-ttu-id="6814c-105">ByCriptionOrResourceGroupOrSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="6814c-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6814c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6814c-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6814c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6814c-107">DESCRIPTION</span></span>
<span data-ttu-id="6814c-108">Das Get-AzPowerBIEmbeddedCapacity cmdlet ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="6814c-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="6814c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6814c-109">EXAMPLES</span></span>

### <span data-ttu-id="6814c-110">Beispiel 1: Ressourcengruppenressourcen erhalten</span><span class="sxs-lookup"><span data-stu-id="6814c-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="6814c-111">Dieser Befehl ruft alle eingebetteten Azure PowerBI-Kapazität in der Ressourcengruppe namens testRG ab.</span><span class="sxs-lookup"><span data-stu-id="6814c-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="6814c-112">Beispiel 2: Erhalten einer Kapazität</span><span class="sxs-lookup"><span data-stu-id="6814c-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="6814c-113">Mit diesem Befehl wird die eingebettete Azure PowerBI-Kapazität, die in der Ressourcengruppe "testRG" genannt wird, als Testkraft bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6814c-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="6814c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6814c-114">PARAMETERS</span></span>

### <span data-ttu-id="6814c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6814c-115">-DefaultProfile</span></span>
<span data-ttu-id="6814c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6814c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6814c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6814c-117">-Name</span></span>
<span data-ttu-id="6814c-118">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="6814c-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="6814c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6814c-119">-ResourceGroupName</span></span>
<span data-ttu-id="6814c-120">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="6814c-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="6814c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6814c-121">-ResourceId</span></span>
<span data-ttu-id="6814c-122">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6814c-122">Azure resource ID</span></span>

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

### <span data-ttu-id="6814c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6814c-123">CommonParameters</span></span>
<span data-ttu-id="6814c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6814c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6814c-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6814c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6814c-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6814c-126">INPUTS</span></span>

### <span data-ttu-id="6814c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6814c-127">System.String</span></span>

## <span data-ttu-id="6814c-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6814c-128">OUTPUTS</span></span>

### <span data-ttu-id="6814c-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbedded1</span><span class="sxs-lookup"><span data-stu-id="6814c-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="6814c-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6814c-130">NOTES</span></span>

## <span data-ttu-id="6814c-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6814c-131">RELATED LINKS</span></span>

[<span data-ttu-id="6814c-132">New-AzPowerBIEmbedded1 </span><span class="sxs-lookup"><span data-stu-id="6814c-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="6814c-133">Remove-AzPowerBIEmbedded1 </span><span class="sxs-lookup"><span data-stu-id="6814c-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
