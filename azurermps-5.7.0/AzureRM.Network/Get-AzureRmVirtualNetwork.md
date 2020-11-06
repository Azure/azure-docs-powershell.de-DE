---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: 1745e3a87d91917e762c9b0e441110b4b6945601
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479710"
---
# <span data-ttu-id="6997c-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6997c-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="6997c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6997c-102">SYNOPSIS</span></span>
<span data-ttu-id="6997c-103">Ruft ein virtuelles Netzwerk in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="6997c-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6997c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6997c-104">SYNTAX</span></span>

### <span data-ttu-id="6997c-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="6997c-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6997c-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="6997c-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6997c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6997c-107">DESCRIPTION</span></span>
<span data-ttu-id="6997c-108">Das Cmdlet " **Get-AzureRmVirtualNetwork** " ruft mindestens ein virtuelles Netzwerk n einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="6997c-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="6997c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6997c-109">EXAMPLES</span></span>

### <span data-ttu-id="6997c-110">1: Abrufen eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="6997c-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="6997c-111">Dieser Befehl ruft das virtuelle Netzwerk mit dem Namen MyVirtualNetwork in der Ressourcengruppe auf TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6997c-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="6997c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6997c-112">PARAMETERS</span></span>

### <span data-ttu-id="6997c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6997c-113">-DefaultProfile</span></span>
<span data-ttu-id="6997c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6997c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6997c-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="6997c-115">-ExpandResource</span></span>
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

### <span data-ttu-id="6997c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6997c-116">-Name</span></span>
<span data-ttu-id="6997c-117">Gibt den Namen des virtuellen Netzwerks an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6997c-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6997c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6997c-118">-ResourceGroupName</span></span>
<span data-ttu-id="6997c-119">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk gehört.</span><span class="sxs-lookup"><span data-stu-id="6997c-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="6997c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6997c-120">CommonParameters</span></span>
<span data-ttu-id="6997c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6997c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6997c-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6997c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6997c-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6997c-123">INPUTS</span></span>

### <span data-ttu-id="6997c-124">Keine</span><span class="sxs-lookup"><span data-stu-id="6997c-124">None</span></span>
<span data-ttu-id="6997c-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6997c-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6997c-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6997c-126">OUTPUTS</span></span>

### <span data-ttu-id="6997c-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6997c-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="6997c-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="6997c-128">NOTES</span></span>

## <span data-ttu-id="6997c-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6997c-129">RELATED LINKS</span></span>

[<span data-ttu-id="6997c-130">Neu – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6997c-130">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="6997c-131">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6997c-131">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="6997c-132">Satz-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6997c-132">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


