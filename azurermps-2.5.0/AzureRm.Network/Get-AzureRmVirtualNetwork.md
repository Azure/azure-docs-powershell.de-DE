---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 983c23111486a964275a7efb85031b013fb365d2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850403"
---
# <span data-ttu-id="678b8-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="678b8-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="678b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="678b8-102">SYNOPSIS</span></span>
<span data-ttu-id="678b8-103">Ruft ein virtuelles Netzwerk in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="678b8-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="678b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="678b8-104">SYNTAX</span></span>

### <span data-ttu-id="678b8-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="678b8-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="678b8-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="678b8-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="678b8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="678b8-107">DESCRIPTION</span></span>
<span data-ttu-id="678b8-108">Das Cmdlet " **Get-AzureRmVirtualNetwork** " ruft mindestens ein virtuelles Netzwerk n einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="678b8-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="678b8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="678b8-109">EXAMPLES</span></span>

### <span data-ttu-id="678b8-110">1: Abrufen eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="678b8-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="678b8-111">Dieser Befehl ruft das virtuelle Netzwerk mit dem Namen MyVirtualNetwork in der Ressourcengruppe auf TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="678b8-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="678b8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="678b8-112">PARAMETERS</span></span>

### <span data-ttu-id="678b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678b8-113">-DefaultProfile</span></span>
<span data-ttu-id="678b8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="678b8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678b8-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="678b8-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678b8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="678b8-116">-Name</span></span>
<span data-ttu-id="678b8-117">Gibt den Namen des virtuellen Netzwerks an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="678b8-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678b8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="678b8-118">-ResourceGroupName</span></span>
<span data-ttu-id="678b8-119">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk gehört.</span><span class="sxs-lookup"><span data-stu-id="678b8-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678b8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678b8-120">CommonParameters</span></span>
<span data-ttu-id="678b8-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="678b8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678b8-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="678b8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678b8-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="678b8-123">INPUTS</span></span>

## <span data-ttu-id="678b8-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="678b8-124">OUTPUTS</span></span>

### <span data-ttu-id="678b8-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="678b8-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="678b8-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="678b8-126">NOTES</span></span>

## <span data-ttu-id="678b8-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="678b8-127">RELATED LINKS</span></span>

[<span data-ttu-id="678b8-128">Neu – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="678b8-128">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="678b8-129">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="678b8-129">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="678b8-130">Satz-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="678b8-130">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


