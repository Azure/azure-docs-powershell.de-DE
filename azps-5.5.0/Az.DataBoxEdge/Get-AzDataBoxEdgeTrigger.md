---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 390646984cbe18c6fed0e6552e8034ae7afe311c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153540"
---
# <span data-ttu-id="f8c03-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="f8c03-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="f8c03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8c03-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c03-103">Konfigurieren der Trigger auf einem Gerät</span><span class="sxs-lookup"><span data-stu-id="f8c03-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="f8c03-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8c03-104">SYNTAX</span></span>

### <span data-ttu-id="f8c03-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8c03-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8c03-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8c03-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8c03-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8c03-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8c03-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8c03-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="f8c03-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8c03-109">DESCRIPTION</span></span>
<span data-ttu-id="f8c03-110">Das **Cmdlet "Get-AzDataBoxEdgeTriger"** ruft die Trigger für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="f8c03-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="f8c03-111">Sie können den Namen im Cmdlet als Parameter angeben, um die Details eines bestimmten Triggers abrufen zu können.</span><span class="sxs-lookup"><span data-stu-id="f8c03-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="f8c03-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f8c03-112">EXAMPLES</span></span>

### <span data-ttu-id="f8c03-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8c03-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="f8c03-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8c03-114">PARAMETERS</span></span>

### <span data-ttu-id="f8c03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c03-115">-DefaultProfile</span></span>
<span data-ttu-id="f8c03-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8c03-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8c03-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f8c03-117">-DeviceName</span></span>
<span data-ttu-id="f8c03-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="f8c03-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8c03-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f8c03-119">-DeviceObject</span></span>
<span data-ttu-id="f8c03-120">Geben Sie bitte ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="f8c03-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8c03-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f8c03-121">-Name</span></span>
<span data-ttu-id="f8c03-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="f8c03-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8c03-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8c03-123">-ResourceGroupName</span></span>
<span data-ttu-id="f8c03-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f8c03-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8c03-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8c03-125">-ResourceId</span></span>
<span data-ttu-id="f8c03-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8c03-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8c03-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c03-127">CommonParameters</span></span>
<span data-ttu-id="f8c03-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8c03-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c03-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8c03-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c03-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f8c03-130">INPUTS</span></span>

### <span data-ttu-id="f8c03-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f8c03-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="f8c03-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f8c03-132">OUTPUTS</span></span>

### <span data-ttu-id="f8c03-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="f8c03-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="f8c03-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f8c03-134">NOTES</span></span>

## <span data-ttu-id="f8c03-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f8c03-135">RELATED LINKS</span></span>
