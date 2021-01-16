---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
ms.openlocfilehash: c2d97f4a7d713482a5e442e1fcb712ccb18797c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292925"
---
# <span data-ttu-id="cb5e9-101">Get-AzDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="cb5e9-101">Get-AzDataBoxEdgeJob</span></span>

## <span data-ttu-id="cb5e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb5e9-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5e9-103">Ruft die Aufträge ab, die auf einem Gerät geplant sind.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="cb5e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb5e9-104">SYNTAX</span></span>

### <span data-ttu-id="cb5e9-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb5e9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb5e9-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="cb5e9-106">GetByResourceIdObject</span></span>
```
Get-AzDataBoxEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb5e9-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb5e9-107">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="cb5e9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb5e9-108">DESCRIPTION</span></span>
<span data-ttu-id="cb5e9-109">Das **Cmdlet "Get-AzDataBoxEdgeJob"** ruft die aktiven Aufträge auf einem Data Box Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-109">The **Get-AzDataBoxEdgeJob** cmdlet gets the active jobs on a Data Box Edge device.</span></span> <span data-ttu-id="cb5e9-110">Sie können den Parameter "Name" erwähnen, um Details zu einem bestimmten Auftrag anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="cb5e9-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cb5e9-111">EXAMPLES</span></span>

### <span data-ttu-id="cb5e9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cb5e9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="cb5e9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb5e9-113">PARAMETERS</span></span>

### <span data-ttu-id="cb5e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5e9-114">-DefaultProfile</span></span>
<span data-ttu-id="cb5e9-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb5e9-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cb5e9-116">-DeviceName</span></span>
<span data-ttu-id="cb5e9-117">Name des Geräts</span><span class="sxs-lookup"><span data-stu-id="cb5e9-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5e9-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="cb5e9-118">-DeviceObject</span></span>
<span data-ttu-id="cb5e9-119">Geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="cb5e9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cb5e9-120">-Name</span></span>
<span data-ttu-id="cb5e9-121">Name des Auftrags, im Allgemeinen eine GUID</span><span class="sxs-lookup"><span data-stu-id="cb5e9-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5e9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb5e9-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb5e9-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="cb5e9-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5e9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb5e9-124">-ResourceId</span></span>
<span data-ttu-id="cb5e9-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb5e9-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5e9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5e9-126">CommonParameters</span></span>
<span data-ttu-id="cb5e9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5e9-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb5e9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5e9-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cb5e9-129">INPUTS</span></span>

### <span data-ttu-id="cb5e9-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="cb5e9-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="cb5e9-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cb5e9-131">OUTPUTS</span></span>

### <span data-ttu-id="cb5e9-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="cb5e9-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span></span>

## <span data-ttu-id="cb5e9-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cb5e9-133">NOTES</span></span>

## <span data-ttu-id="cb5e9-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cb5e9-134">RELATED LINKS</span></span>
