---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301744"
---
# <span data-ttu-id="e4931-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="e4931-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="e4931-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e4931-102">SYNOPSIS</span></span>
<span data-ttu-id="e4931-103">Abrufen der Bestelldetails für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="e4931-103">Get the order details for a device</span></span>

## <span data-ttu-id="e4931-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4931-104">SYNTAX</span></span>

### <span data-ttu-id="e4931-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e4931-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4931-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4931-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4931-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4931-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4931-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4931-108">DESCRIPTION</span></span>
<span data-ttu-id="e4931-109">Das Cmdlet " **Get-AzStackEdgeOrder** " Ruft die Bestelldetails für ein Stack-Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="e4931-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="e4931-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4931-110">EXAMPLES</span></span>

### <span data-ttu-id="e4931-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e4931-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="e4931-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4931-112">PARAMETERS</span></span>

### <span data-ttu-id="e4931-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4931-113">-DefaultProfile</span></span>
<span data-ttu-id="e4931-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e4931-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4931-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e4931-115">-DeviceName</span></span>
<span data-ttu-id="e4931-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="e4931-116">Resource Group Name</span></span>

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

### <span data-ttu-id="e4931-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e4931-117">-DeviceObject</span></span>
<span data-ttu-id="e4931-118">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="e4931-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="e4931-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4931-119">-ResourceGroupName</span></span>
<span data-ttu-id="e4931-120">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="e4931-120">Resource Group Name</span></span>

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

### <span data-ttu-id="e4931-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e4931-121">-ResourceId</span></span>
<span data-ttu-id="e4931-122">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="e4931-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="e4931-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4931-123">CommonParameters</span></span>
<span data-ttu-id="e4931-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4931-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4931-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4931-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4931-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e4931-126">INPUTS</span></span>

### <span data-ttu-id="e4931-127">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e4931-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="e4931-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e4931-128">System.String</span></span>

## <span data-ttu-id="e4931-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e4931-129">OUTPUTS</span></span>

### <span data-ttu-id="e4931-130">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="e4931-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="e4931-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4931-131">NOTES</span></span>

## <span data-ttu-id="e4931-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e4931-132">RELATED LINKS</span></span>
