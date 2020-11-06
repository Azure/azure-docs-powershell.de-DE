---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
ms.openlocfilehash: d4d9af3184b1b6f858ea4f1e6910fc6562e68f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482358"
---
# <span data-ttu-id="65716-101">Get-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="65716-101">Get-AzureRmVirtualWan</span></span>

## <span data-ttu-id="65716-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65716-102">SYNOPSIS</span></span>
<span data-ttu-id="65716-103">Ruft ein virtuelles WAN oder alle virtuellen WANs in einer Ressourcengruppe oder einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="65716-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65716-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65716-104">SYNTAX</span></span>

### <span data-ttu-id="65716-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="65716-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65716-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65716-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualWan -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65716-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65716-107">DESCRIPTION</span></span>
<span data-ttu-id="65716-108">Ruft ein virtuelles WAN oder alle virtuellen WANs in einer Ressourcengruppe oder einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="65716-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="65716-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65716-109">EXAMPLES</span></span>

### <span data-ttu-id="65716-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65716-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzureRmVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="65716-111">Dieser Befehl ruft das virtuelle WAN mit dem Namen myVirtualWAN in der Ressourcengruppe testRG.</span><span class="sxs-lookup"><span data-stu-id="65716-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

## <span data-ttu-id="65716-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="65716-112">PARAMETERS</span></span>

### <span data-ttu-id="65716-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65716-113">-DefaultProfile</span></span>
<span data-ttu-id="65716-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65716-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65716-115">-Name</span><span class="sxs-lookup"><span data-stu-id="65716-115">-Name</span></span>
<span data-ttu-id="65716-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="65716-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65716-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65716-117">-ResourceGroupName</span></span>
<span data-ttu-id="65716-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="65716-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65716-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65716-119">CommonParameters</span></span>
<span data-ttu-id="65716-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65716-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65716-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65716-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65716-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65716-122">INPUTS</span></span>

### <span data-ttu-id="65716-123">Keine</span><span class="sxs-lookup"><span data-stu-id="65716-123">None</span></span>

## <span data-ttu-id="65716-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65716-124">OUTPUTS</span></span>

### <span data-ttu-id="65716-125">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="65716-125">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="65716-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="65716-126">NOTES</span></span>

## <span data-ttu-id="65716-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65716-127">RELATED LINKS</span></span>
