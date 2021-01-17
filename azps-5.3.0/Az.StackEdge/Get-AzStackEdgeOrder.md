---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472560"
---
# <span data-ttu-id="87e76-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="87e76-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="87e76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87e76-102">SYNOPSIS</span></span>
<span data-ttu-id="87e76-103">Erhalten der Bestelldetails für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="87e76-103">Get the order details for a device</span></span>

## <span data-ttu-id="87e76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87e76-104">SYNTAX</span></span>

### <span data-ttu-id="87e76-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="87e76-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87e76-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87e76-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87e76-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87e76-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87e76-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87e76-108">DESCRIPTION</span></span>
<span data-ttu-id="87e76-109">Das **Cmdlet "Get-AzStackEdgeOrder"** ruft die Bestelldetails für ein Stack Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="87e76-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="87e76-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87e76-110">EXAMPLES</span></span>

### <span data-ttu-id="87e76-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="87e76-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="87e76-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87e76-112">PARAMETERS</span></span>

### <span data-ttu-id="87e76-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e76-113">-DefaultProfile</span></span>
<span data-ttu-id="87e76-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87e76-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87e76-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="87e76-115">-DeviceName</span></span>
<span data-ttu-id="87e76-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="87e76-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e76-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="87e76-117">-DeviceObject</span></span>
<span data-ttu-id="87e76-118">Geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="87e76-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: GetByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87e76-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e76-119">-ResourceGroupName</span></span>
<span data-ttu-id="87e76-120">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="87e76-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e76-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87e76-121">-ResourceId</span></span>
<span data-ttu-id="87e76-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="87e76-122">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e76-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e76-123">CommonParameters</span></span>
<span data-ttu-id="87e76-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87e76-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e76-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87e76-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e76-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87e76-126">INPUTS</span></span>

### <span data-ttu-id="87e76-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="87e76-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="87e76-128">System.String</span><span class="sxs-lookup"><span data-stu-id="87e76-128">System.String</span></span>

## <span data-ttu-id="87e76-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87e76-129">OUTPUTS</span></span>

### <span data-ttu-id="87e76-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="87e76-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="87e76-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="87e76-131">NOTES</span></span>

## <span data-ttu-id="87e76-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="87e76-132">RELATED LINKS</span></span>
