---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 670880a9fa82e4845f37cdb5f0d108533a2b72c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174359"
---
# <span data-ttu-id="92f62-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="92f62-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="92f62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92f62-102">SYNOPSIS</span></span>
<span data-ttu-id="92f62-103">Ruft eine Azure ExpressRoutePort-Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="92f62-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="92f62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92f62-104">SYNTAX</span></span>

### <span data-ttu-id="92f62-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="92f62-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92f62-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92f62-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92f62-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92f62-107">DESCRIPTION</span></span>
<span data-ttu-id="92f62-108">Das Cmdlet " **Get-AzExpressRoutePort** " wird verwendet, um ein ExpressRoutePort-Objekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="92f62-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="92f62-109">Das zurückgegebene expressrouteport-Objekt kann als Eingabe für andere Cmdlets verwendet werden, die auf expressrouteport ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="92f62-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="92f62-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92f62-110">EXAMPLES</span></span>

### <span data-ttu-id="92f62-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="92f62-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="92f62-112">Ruft das ExpressRoutePort-Objekt mit dem Namen $Portname in der Ressourcengruppe $RG in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="92f62-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="92f62-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="92f62-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="92f62-114">Ruft alle ExpressRoutePort-Objekte ab, deren Name mit "Test" beginnt.</span><span class="sxs-lookup"><span data-stu-id="92f62-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="92f62-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="92f62-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="92f62-116">Ruft das ExpressRoutePort-Objekt mit der $ID "resourcecode" ab.</span><span class="sxs-lookup"><span data-stu-id="92f62-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="92f62-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="92f62-117">PARAMETERS</span></span>

### <span data-ttu-id="92f62-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f62-118">-DefaultProfile</span></span>
<span data-ttu-id="92f62-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92f62-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92f62-120">-Name</span><span class="sxs-lookup"><span data-stu-id="92f62-120">-Name</span></span>
<span data-ttu-id="92f62-121">Der Name des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="92f62-121">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="92f62-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f62-122">-ResourceGroupName</span></span>
<span data-ttu-id="92f62-123">Der Ressourcengruppenname des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="92f62-123">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="92f62-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="92f62-124">-ResourceId</span></span>
<span data-ttu-id="92f62-125">Die Quelle des Express-Route-Ports.</span><span class="sxs-lookup"><span data-stu-id="92f62-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="92f62-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f62-126">CommonParameters</span></span>
<span data-ttu-id="92f62-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f62-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f62-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92f62-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f62-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92f62-129">INPUTS</span></span>

### <span data-ttu-id="92f62-130">System. String</span><span class="sxs-lookup"><span data-stu-id="92f62-130">System.String</span></span>

## <span data-ttu-id="92f62-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92f62-131">OUTPUTS</span></span>

### <span data-ttu-id="92f62-132">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="92f62-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="92f62-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="92f62-133">NOTES</span></span>

## <span data-ttu-id="92f62-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92f62-134">RELATED LINKS</span></span>

[<span data-ttu-id="92f62-135">Neu – AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="92f62-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="92f62-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="92f62-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="92f62-137">Satz-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="92f62-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
