---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 6a20f81644827c84ee1ce215ad2e87268650caf9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362787"
---
# <span data-ttu-id="9be0c-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="9be0c-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="9be0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9be0c-102">SYNOPSIS</span></span>
<span data-ttu-id="9be0c-103">Ruft die verfügbaren Freigaben für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="9be0c-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="9be0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9be0c-104">SYNTAX</span></span>

### <span data-ttu-id="9be0c-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9be0c-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9be0c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9be0c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9be0c-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9be0c-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9be0c-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9be0c-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="9be0c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9be0c-109">DESCRIPTION</span></span>
<span data-ttu-id="9be0c-110">Das **Cmdlet "Get-AzDataBoxEdgeShare"** ruft die verfügbaren Freigaben für ein Data Box Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="9be0c-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="9be0c-111">Wird "Name" angegeben, wird die Freigabe nach Name bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9be0c-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="9be0c-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9be0c-112">EXAMPLES</span></span>

### <span data-ttu-id="9be0c-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9be0c-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="9be0c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9be0c-114">PARAMETERS</span></span>

### <span data-ttu-id="9be0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9be0c-115">-DefaultProfile</span></span>
<span data-ttu-id="9be0c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9be0c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9be0c-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9be0c-117">-DeviceName</span></span>
<span data-ttu-id="9be0c-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="9be0c-118">Device Name</span></span>

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

### <span data-ttu-id="9be0c-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="9be0c-119">-DeviceObject</span></span>
<span data-ttu-id="9be0c-120">Geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="9be0c-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="9be0c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9be0c-121">-Name</span></span>
<span data-ttu-id="9be0c-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="9be0c-122">Resource Name</span></span>

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

### <span data-ttu-id="9be0c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9be0c-123">-ResourceGroupName</span></span>
<span data-ttu-id="9be0c-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="9be0c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="9be0c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9be0c-125">-ResourceId</span></span>
<span data-ttu-id="9be0c-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9be0c-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="9be0c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be0c-127">CommonParameters</span></span>
<span data-ttu-id="9be0c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9be0c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9be0c-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9be0c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be0c-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9be0c-130">INPUTS</span></span>

### <span data-ttu-id="9be0c-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9be0c-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="9be0c-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9be0c-132">OUTPUTS</span></span>

### <span data-ttu-id="9be0c-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="9be0c-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="9be0c-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9be0c-134">NOTES</span></span>

## <span data-ttu-id="9be0c-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9be0c-135">RELATED LINKS</span></span>
