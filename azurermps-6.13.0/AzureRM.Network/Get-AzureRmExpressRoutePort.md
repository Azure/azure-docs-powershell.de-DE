---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
ms.openlocfilehash: 36c15c9a0bfae9bbf3a14f59877d23c1c8778163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664830"
---
# <span data-ttu-id="d1bd0-101">Get-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d1bd0-101">Get-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="d1bd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="d1bd0-103">Ruft eine Azure ExpressRoutePort-Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="d1bd0-103">Gets an Azure ExpressRoutePort resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1bd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1bd0-104">SYNTAX</span></span>

### <span data-ttu-id="d1bd0-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1bd0-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1bd0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1bd0-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1bd0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1bd0-107">DESCRIPTION</span></span>
<span data-ttu-id="d1bd0-108">Das Cmdlet " **Get-AzureRmExpressRoutePort** " wird verwendet, um ein ExpressRoutePort-Objekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d1bd0-108">The **Get-AzureRmExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="d1bd0-109">Das zurückgegebene expressrouteport-Objekt kann als Eingabe für andere Cmdlets verwendet werden, die auf expressrouteport ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d1bd0-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="d1bd0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1bd0-110">EXAMPLES</span></span>

### <span data-ttu-id="d1bd0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1bd0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="d1bd0-112">Ruft das ExpressRoutePort-Objekt mit dem Namen $Portname in der Ressourcengruppe $RG in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d1bd0-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="d1bd0-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d1bd0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -ResourceId $id
```

<span data-ttu-id="d1bd0-114">Ruft das ExpressRoutePort-Objekt mit der $ID "resourcecode" ab.</span><span class="sxs-lookup"><span data-stu-id="d1bd0-114">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="d1bd0-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1bd0-115">PARAMETERS</span></span>

### <span data-ttu-id="d1bd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1bd0-116">-DefaultProfile</span></span>
<span data-ttu-id="d1bd0-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1bd0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1bd0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d1bd0-118">-Name</span></span>
<span data-ttu-id="d1bd0-119">Der Name des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d1bd0-119">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1bd0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1bd0-120">-ResourceGroupName</span></span>
<span data-ttu-id="d1bd0-121">Der Ressourcengruppenname des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d1bd0-121">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1bd0-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d1bd0-122">-ResourceId</span></span>
<span data-ttu-id="d1bd0-123">Die Quelle des Express-Route-Ports.</span><span class="sxs-lookup"><span data-stu-id="d1bd0-123">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1bd0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1bd0-124">CommonParameters</span></span>
<span data-ttu-id="d1bd0-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1bd0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1bd0-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1bd0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1bd0-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1bd0-127">INPUTS</span></span>

### <span data-ttu-id="d1bd0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d1bd0-128">System.String</span></span>

## <span data-ttu-id="d1bd0-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1bd0-129">OUTPUTS</span></span>

### <span data-ttu-id="d1bd0-130">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d1bd0-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="d1bd0-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1bd0-131">NOTES</span></span>

## <span data-ttu-id="d1bd0-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1bd0-132">RELATED LINKS</span></span>
