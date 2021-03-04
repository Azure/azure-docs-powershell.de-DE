---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: f9ce00bb5efbe5182143a08f9f205101b9f85611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932408"
---
# <span data-ttu-id="a80d7-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a80d7-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="a80d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a80d7-102">SYNOPSIS</span></span>
<span data-ttu-id="a80d7-103">Ruft eine Azure ExpressRoutePort-Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="a80d7-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="a80d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a80d7-104">SYNTAX</span></span>

### <span data-ttu-id="a80d7-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a80d7-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a80d7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a80d7-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a80d7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a80d7-107">DESCRIPTION</span></span>
<span data-ttu-id="a80d7-108">Das **Get-AzExpressRoutePort-Cmdlet** wird verwendet, um ein ExpressRoutePort-Objekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a80d7-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="a80d7-109">Das zurückgegebene Expressrouteport-Objekt kann als Eingabe für andere Cmdlets verwendet werden, die auf ExpressRoutePort funktionieren.</span><span class="sxs-lookup"><span data-stu-id="a80d7-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="a80d7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a80d7-110">EXAMPLES</span></span>

### <span data-ttu-id="a80d7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a80d7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="a80d7-112">Ruft das ExpressRoutePort-Objekt mit dem Namen $PortName in der Ressourcengruppe $rg in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a80d7-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="a80d7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a80d7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="a80d7-114">Ruft alle ExpressRoutePort-Objekte ab, deren Name mit "test" beginnt.</span><span class="sxs-lookup"><span data-stu-id="a80d7-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="a80d7-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a80d7-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="a80d7-116">Ruft das ExpressRoutePort-Objekt mit ResourceId-$id.</span><span class="sxs-lookup"><span data-stu-id="a80d7-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="a80d7-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a80d7-117">PARAMETERS</span></span>

### <span data-ttu-id="a80d7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a80d7-118">-DefaultProfile</span></span>
<span data-ttu-id="a80d7-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a80d7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a80d7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a80d7-120">-Name</span></span>
<span data-ttu-id="a80d7-121">Der Name des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a80d7-121">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="a80d7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a80d7-122">-ResourceGroupName</span></span>
<span data-ttu-id="a80d7-123">Der Ressourcengruppenname des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a80d7-123">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="a80d7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a80d7-124">-ResourceId</span></span>
<span data-ttu-id="a80d7-125">ResourceId des Expressroutenports.</span><span class="sxs-lookup"><span data-stu-id="a80d7-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="a80d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a80d7-126">CommonParameters</span></span>
<span data-ttu-id="a80d7-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a80d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a80d7-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a80d7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a80d7-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a80d7-129">INPUTS</span></span>

### <span data-ttu-id="a80d7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a80d7-130">System.String</span></span>

## <span data-ttu-id="a80d7-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a80d7-131">OUTPUTS</span></span>

### <span data-ttu-id="a80d7-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a80d7-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="a80d7-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a80d7-133">NOTES</span></span>

## <span data-ttu-id="a80d7-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a80d7-134">RELATED LINKS</span></span>

[<span data-ttu-id="a80d7-135">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a80d7-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="a80d7-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a80d7-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="a80d7-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a80d7-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
