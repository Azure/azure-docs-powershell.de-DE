---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 68d9e388238f9054ce56592186f686728e378000
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660025"
---
# <span data-ttu-id="d0691-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d0691-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d0691-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d0691-102">SYNOPSIS</span></span>
<span data-ttu-id="d0691-103">Ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="d0691-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="d0691-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0691-104">SYNTAX</span></span>

### <span data-ttu-id="d0691-105">ByCapacityOrResourceGroupOrSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="d0691-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0691-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0691-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0691-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0691-107">DESCRIPTION</span></span>
<span data-ttu-id="d0691-108">Das Get-AzPowerBIEmbeddedCapacity-Cmdlet ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="d0691-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="d0691-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0691-109">EXAMPLES</span></span>

### <span data-ttu-id="d0691-110">Beispiel 1: Abrufen von Ressourcengruppenkapazitäten</span><span class="sxs-lookup"><span data-stu-id="d0691-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="d0691-111">Dieser Befehl ruft alle Azure PowerBI eingebettete Kapazität in der Ressourcengruppe mit dem Namen testRG</span><span class="sxs-lookup"><span data-stu-id="d0691-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="d0691-112">Beispiel 2: Abrufen einer Kapazität</span><span class="sxs-lookup"><span data-stu-id="d0691-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="d0691-113">Dieser Befehl ruft die eingebettete Azure PowerBI-Kapazität mit dem Namen testcapacity in der Ressourcengruppe mit dem Namen testRG.</span><span class="sxs-lookup"><span data-stu-id="d0691-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="d0691-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0691-114">PARAMETERS</span></span>

### <span data-ttu-id="d0691-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0691-115">-DefaultProfile</span></span>
<span data-ttu-id="d0691-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d0691-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0691-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d0691-117">-Name</span></span>
<span data-ttu-id="d0691-118">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="d0691-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="d0691-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0691-119">-ResourceGroupName</span></span>
<span data-ttu-id="d0691-120">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="d0691-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="d0691-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d0691-121">-ResourceId</span></span>
<span data-ttu-id="d0691-122">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d0691-122">Azure resource ID</span></span>

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

### <span data-ttu-id="d0691-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0691-123">CommonParameters</span></span>
<span data-ttu-id="d0691-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0691-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0691-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0691-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0691-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d0691-126">INPUTS</span></span>

### <span data-ttu-id="d0691-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d0691-127">System.String</span></span>

## <span data-ttu-id="d0691-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d0691-128">OUTPUTS</span></span>

### <span data-ttu-id="d0691-129">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d0691-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d0691-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="d0691-130">NOTES</span></span>

## <span data-ttu-id="d0691-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d0691-131">RELATED LINKS</span></span>

[<span data-ttu-id="d0691-132">Neu – AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="d0691-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d0691-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="d0691-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
