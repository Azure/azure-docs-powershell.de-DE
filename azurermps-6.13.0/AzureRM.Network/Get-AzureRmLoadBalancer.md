---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: 90cafc66857ee2ec94806628b41960eaafaf6e15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495950"
---
# <span data-ttu-id="475e1-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="475e1-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="475e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="475e1-102">SYNOPSIS</span></span>
<span data-ttu-id="475e1-103">Ruft ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="475e1-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="475e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="475e1-104">SYNTAX</span></span>

### <span data-ttu-id="475e1-105">NOEXPAND (Standard)</span><span class="sxs-lookup"><span data-stu-id="475e1-105">NoExpand (Default)</span></span>
```
Get-AzureRmLoadBalancer [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="475e1-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="475e1-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="475e1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="475e1-107">DESCRIPTION</span></span>
<span data-ttu-id="475e1-108">Das Cmdlet " **Get-AzureRmLoadBalancer** " Ruft einen oder mehrere Azure-Lastenausgleichs Elemente ab, die in einer Ressourcengruppe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="475e1-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="475e1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="475e1-109">EXAMPLES</span></span>

### <span data-ttu-id="475e1-110">Beispiel 1: Abrufen eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="475e1-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="475e1-111">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab.</span><span class="sxs-lookup"><span data-stu-id="475e1-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="475e1-112">Bevor Sie dieses Cmdlet ausführen können, muss ein Lastenausgleichsmodul vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="475e1-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="475e1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="475e1-113">PARAMETERS</span></span>

### <span data-ttu-id="475e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475e1-114">-DefaultProfile</span></span>
<span data-ttu-id="475e1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="475e1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="475e1-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="475e1-116">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="475e1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="475e1-117">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="475e1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="475e1-118">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="475e1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475e1-119">CommonParameters</span></span>
<span data-ttu-id="475e1-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475e1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475e1-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="475e1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475e1-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="475e1-122">INPUTS</span></span>

### <span data-ttu-id="475e1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="475e1-123">System.String</span></span>

## <span data-ttu-id="475e1-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="475e1-124">OUTPUTS</span></span>

### <span data-ttu-id="475e1-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="475e1-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="475e1-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="475e1-126">NOTES</span></span>

## <span data-ttu-id="475e1-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="475e1-127">RELATED LINKS</span></span>

[<span data-ttu-id="475e1-128">Neu – AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="475e1-128">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="475e1-129">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="475e1-129">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="475e1-130">Satz-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="475e1-130">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


