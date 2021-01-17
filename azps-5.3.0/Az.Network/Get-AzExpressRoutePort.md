---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 670880a9fa82e4845f37cdb5f0d108533a2b72c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469312"
---
# <span data-ttu-id="36d77-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="36d77-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="36d77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36d77-102">SYNOPSIS</span></span>
<span data-ttu-id="36d77-103">Ruft eine Azure ExpressRoutePort-Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="36d77-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="36d77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36d77-104">SYNTAX</span></span>

### <span data-ttu-id="36d77-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="36d77-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36d77-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36d77-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36d77-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36d77-107">DESCRIPTION</span></span>
<span data-ttu-id="36d77-108">Das **Get-AzExpressRoutePort-Cmdlet** wird verwendet, um ein "ExpressRoutePort"-Objekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="36d77-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="36d77-109">Das zurückgegebene Expressrouteportobjekt kann als Eingabe für andere Cmdlets verwendet werden, die mit ExpressRoutePort funktionieren.</span><span class="sxs-lookup"><span data-stu-id="36d77-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="36d77-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36d77-110">EXAMPLES</span></span>

### <span data-ttu-id="36d77-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36d77-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="36d77-112">Ruft das "ExpressRoutePort"-Objekt mit $PortName in der Ressourcengruppe oder $rg Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="36d77-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="36d77-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="36d77-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="36d77-114">Ruft alle ExpressRoutePort-Objekte ab, deren Name mit "test" beginnt.</span><span class="sxs-lookup"><span data-stu-id="36d77-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="36d77-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="36d77-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="36d77-116">Ruft das "ExpressRoutePort"-Objekt mit "ResourceId"-$id.</span><span class="sxs-lookup"><span data-stu-id="36d77-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="36d77-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36d77-117">PARAMETERS</span></span>

### <span data-ttu-id="36d77-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d77-118">-DefaultProfile</span></span>
<span data-ttu-id="36d77-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36d77-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36d77-120">-Name</span><span class="sxs-lookup"><span data-stu-id="36d77-120">-Name</span></span>
<span data-ttu-id="36d77-121">Der Name des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="36d77-121">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="36d77-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d77-122">-ResourceGroupName</span></span>
<span data-ttu-id="36d77-123">Der Ressourcengruppenname des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="36d77-123">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="36d77-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36d77-124">-ResourceId</span></span>
<span data-ttu-id="36d77-125">ResourceId des Expressroutenports.</span><span class="sxs-lookup"><span data-stu-id="36d77-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="36d77-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d77-126">CommonParameters</span></span>
<span data-ttu-id="36d77-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36d77-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d77-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36d77-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d77-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36d77-129">INPUTS</span></span>

### <span data-ttu-id="36d77-130">System.String</span><span class="sxs-lookup"><span data-stu-id="36d77-130">System.String</span></span>

## <span data-ttu-id="36d77-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36d77-131">OUTPUTS</span></span>

### <span data-ttu-id="36d77-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="36d77-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="36d77-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="36d77-133">NOTES</span></span>

## <span data-ttu-id="36d77-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="36d77-134">RELATED LINKS</span></span>

[<span data-ttu-id="36d77-135">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="36d77-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="36d77-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="36d77-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="36d77-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="36d77-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
