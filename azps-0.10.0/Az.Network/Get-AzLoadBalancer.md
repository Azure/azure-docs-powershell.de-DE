---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: f5f0ce9768226c79210db3a38c5c09303e94a852
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841640"
---
# <span data-ttu-id="31f7b-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="31f7b-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="31f7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="31f7b-103">Ruft ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="31f7b-103">Gets a load balancer.</span></span>

## <span data-ttu-id="31f7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31f7b-104">SYNTAX</span></span>

### <span data-ttu-id="31f7b-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="31f7b-105">NoExpand</span></span>
```
Get-AzLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31f7b-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="31f7b-106">Expand</span></span>
```
Get-AzLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31f7b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31f7b-107">DESCRIPTION</span></span>
<span data-ttu-id="31f7b-108">Das Cmdlet " **Get-AzLoadBalancer** " Ruft einen oder mehrere Azure-Lastenausgleichs Elemente ab, die in einer Ressourcengruppe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="31f7b-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="31f7b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31f7b-109">EXAMPLES</span></span>

### <span data-ttu-id="31f7b-110">Beispiel 1: Abrufen eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="31f7b-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="31f7b-111">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab.</span><span class="sxs-lookup"><span data-stu-id="31f7b-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="31f7b-112">Bevor Sie dieses Cmdlet ausführen können, muss ein Lastenausgleichsmodul vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="31f7b-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="31f7b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="31f7b-113">PARAMETERS</span></span>

### <span data-ttu-id="31f7b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f7b-114">-DefaultProfile</span></span>
<span data-ttu-id="31f7b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31f7b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31f7b-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="31f7b-116">-ExpandResource</span></span>
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

### <span data-ttu-id="31f7b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="31f7b-117">-Name</span></span>
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

### <span data-ttu-id="31f7b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f7b-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="31f7b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f7b-119">CommonParameters</span></span>
<span data-ttu-id="31f7b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f7b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f7b-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31f7b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f7b-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31f7b-122">INPUTS</span></span>

## <span data-ttu-id="31f7b-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31f7b-123">OUTPUTS</span></span>

### <span data-ttu-id="31f7b-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="31f7b-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="31f7b-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="31f7b-125">NOTES</span></span>

## <span data-ttu-id="31f7b-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31f7b-126">RELATED LINKS</span></span>

[<span data-ttu-id="31f7b-127">Neu – AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="31f7b-127">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="31f7b-128">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="31f7b-128">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="31f7b-129">Satz-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="31f7b-129">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


