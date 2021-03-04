---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 616830906621b673010ca8708b909608c06f93fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942947"
---
# <span data-ttu-id="3ad06-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3ad06-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="3ad06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ad06-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad06-103">Ruft die verfügbaren Freigaben für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="3ad06-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="3ad06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ad06-104">SYNTAX</span></span>

### <span data-ttu-id="3ad06-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ad06-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ad06-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ad06-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ad06-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ad06-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ad06-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ad06-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="3ad06-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ad06-109">DESCRIPTION</span></span>
<span data-ttu-id="3ad06-110">Das **Get-AzDataBoxEdgeShare-Cmdlet** ruft die verfügbaren Freigaben für ein Data Box Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="3ad06-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="3ad06-111">Wenn Name angegeben ist, wird die Freigabe nach Name angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3ad06-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="3ad06-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ad06-112">EXAMPLES</span></span>

### <span data-ttu-id="3ad06-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ad06-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="3ad06-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3ad06-114">PARAMETERS</span></span>

### <span data-ttu-id="3ad06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad06-115">-DefaultProfile</span></span>
<span data-ttu-id="3ad06-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ad06-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ad06-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3ad06-117">-DeviceName</span></span>
<span data-ttu-id="3ad06-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="3ad06-118">Device Name</span></span>

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

### <span data-ttu-id="3ad06-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="3ad06-119">-DeviceObject</span></span>
<span data-ttu-id="3ad06-120">Bitte geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="3ad06-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="3ad06-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3ad06-121">-Name</span></span>
<span data-ttu-id="3ad06-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="3ad06-122">Resource Name</span></span>

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

### <span data-ttu-id="3ad06-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ad06-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ad06-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3ad06-124">Resource Group Name</span></span>

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

### <span data-ttu-id="3ad06-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ad06-125">-ResourceId</span></span>
<span data-ttu-id="3ad06-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ad06-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="3ad06-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad06-127">CommonParameters</span></span>
<span data-ttu-id="3ad06-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad06-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad06-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ad06-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad06-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ad06-130">INPUTS</span></span>

### <span data-ttu-id="3ad06-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3ad06-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="3ad06-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ad06-132">OUTPUTS</span></span>

### <span data-ttu-id="3ad06-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3ad06-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="3ad06-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3ad06-134">NOTES</span></span>

## <span data-ttu-id="3ad06-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3ad06-135">RELATED LINKS</span></span>
