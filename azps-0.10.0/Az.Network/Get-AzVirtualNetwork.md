---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: 97ae2607484828350be67cff9c9311fc73f19b6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841520"
---
# <span data-ttu-id="cc156-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc156-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="cc156-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc156-102">SYNOPSIS</span></span>
<span data-ttu-id="cc156-103">Ruft ein virtuelles Netzwerk in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="cc156-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="cc156-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc156-104">SYNTAX</span></span>

### <span data-ttu-id="cc156-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="cc156-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc156-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="cc156-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc156-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc156-107">DESCRIPTION</span></span>
<span data-ttu-id="cc156-108">Das Cmdlet " **Get-AzVirtualNetwork** " ruft mindestens ein virtuelles Netzwerk n einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="cc156-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="cc156-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc156-109">EXAMPLES</span></span>

### <span data-ttu-id="cc156-110">1: Abrufen eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="cc156-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="cc156-111">Dieser Befehl ruft das virtuelle Netzwerk mit dem Namen MyVirtualNetwork in der Ressourcengruppe auf TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc156-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="cc156-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc156-112">PARAMETERS</span></span>

### <span data-ttu-id="cc156-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc156-113">-DefaultProfile</span></span>
<span data-ttu-id="cc156-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc156-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc156-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="cc156-115">-ExpandResource</span></span>
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

### <span data-ttu-id="cc156-116">-Name</span><span class="sxs-lookup"><span data-stu-id="cc156-116">-Name</span></span>
<span data-ttu-id="cc156-117">Gibt den Namen des virtuellen Netzwerks an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="cc156-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cc156-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc156-118">-ResourceGroupName</span></span>
<span data-ttu-id="cc156-119">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk gehört.</span><span class="sxs-lookup"><span data-stu-id="cc156-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="cc156-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc156-120">CommonParameters</span></span>
<span data-ttu-id="cc156-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc156-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc156-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc156-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc156-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc156-123">INPUTS</span></span>

## <span data-ttu-id="cc156-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc156-124">OUTPUTS</span></span>

### <span data-ttu-id="cc156-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc156-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="cc156-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc156-126">NOTES</span></span>

## <span data-ttu-id="cc156-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc156-127">RELATED LINKS</span></span>

[<span data-ttu-id="cc156-128">Neu – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc156-128">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="cc156-129">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc156-129">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="cc156-130">Satz-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc156-130">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


