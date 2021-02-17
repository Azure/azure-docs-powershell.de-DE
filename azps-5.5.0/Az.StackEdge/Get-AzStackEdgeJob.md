---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164833"
---
# <span data-ttu-id="f28bd-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="f28bd-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="f28bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f28bd-102">SYNOPSIS</span></span>
<span data-ttu-id="f28bd-103">Ruft die Aufträge ab, die auf einem Gerät geplant sind.</span><span class="sxs-lookup"><span data-stu-id="f28bd-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="f28bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f28bd-104">SYNTAX</span></span>

### <span data-ttu-id="f28bd-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f28bd-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f28bd-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="f28bd-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f28bd-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f28bd-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="f28bd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f28bd-108">DESCRIPTION</span></span>
<span data-ttu-id="f28bd-109">Das **Cmdlet "Get-AzStackEdgeJob"** ruft die aktiven Aufträge auf einem Stack Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="f28bd-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="f28bd-110">Sie können den Parameter "Name" erwähnen, um Details zu einem bestimmten Auftrag anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f28bd-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="f28bd-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f28bd-111">EXAMPLES</span></span>

### <span data-ttu-id="f28bd-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f28bd-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="f28bd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f28bd-113">PARAMETERS</span></span>

### <span data-ttu-id="f28bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f28bd-114">-DefaultProfile</span></span>
<span data-ttu-id="f28bd-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f28bd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f28bd-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f28bd-116">-DeviceName</span></span>
<span data-ttu-id="f28bd-117">Name des Geräts</span><span class="sxs-lookup"><span data-stu-id="f28bd-117">Name of the device</span></span>

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

### <span data-ttu-id="f28bd-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f28bd-118">-DeviceObject</span></span>
<span data-ttu-id="f28bd-119">Geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="f28bd-119">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f28bd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f28bd-120">-Name</span></span>
<span data-ttu-id="f28bd-121">Name des Auftrags, im Allgemeinen eine GUID</span><span class="sxs-lookup"><span data-stu-id="f28bd-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: Job

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f28bd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f28bd-122">-ResourceGroupName</span></span>
<span data-ttu-id="f28bd-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f28bd-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f28bd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f28bd-124">-ResourceId</span></span>
<span data-ttu-id="f28bd-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f28bd-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f28bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f28bd-126">CommonParameters</span></span>
<span data-ttu-id="f28bd-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f28bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f28bd-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f28bd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f28bd-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f28bd-129">INPUTS</span></span>

### <span data-ttu-id="f28bd-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f28bd-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="f28bd-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f28bd-131">OUTPUTS</span></span>

### <span data-ttu-id="f28bd-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="f28bd-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="f28bd-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f28bd-133">NOTES</span></span>

## <span data-ttu-id="f28bd-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f28bd-134">RELATED LINKS</span></span>
