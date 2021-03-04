---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 34ef411b96aaee2a6caa32452c678d888cf62b65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923915"
---
# <span data-ttu-id="f1fb9-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f1fb9-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="f1fb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="f1fb9-103">Ruft die verfügbaren Freigaben für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="f1fb9-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="f1fb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1fb9-104">SYNTAX</span></span>

### <span data-ttu-id="f1fb9-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1fb9-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1fb9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1fb9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1fb9-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1fb9-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1fb9-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1fb9-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="f1fb9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1fb9-109">DESCRIPTION</span></span>
<span data-ttu-id="f1fb9-110">Das **Get-AzStackEdgeShare-Cmdlet** ruft die verfügbaren Freigaben für ein Stack Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="f1fb9-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="f1fb9-111">Wenn Name angegeben ist, wird die Freigabe nach Name angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f1fb9-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="f1fb9-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1fb9-112">EXAMPLES</span></span>

### <span data-ttu-id="f1fb9-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1fb9-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="f1fb9-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f1fb9-114">PARAMETERS</span></span>

### <span data-ttu-id="f1fb9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1fb9-115">-DefaultProfile</span></span>
<span data-ttu-id="f1fb9-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1fb9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1fb9-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f1fb9-117">-DeviceName</span></span>
<span data-ttu-id="f1fb9-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="f1fb9-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb9-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f1fb9-119">-DeviceObject</span></span>
<span data-ttu-id="f1fb9-120">Bitte geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="f1fb9-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f1fb9-121">-Name</span></span>
<span data-ttu-id="f1fb9-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="f1fb9-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1fb9-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1fb9-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f1fb9-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1fb9-125">-ResourceId</span></span>
<span data-ttu-id="f1fb9-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1fb9-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="f1fb9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1fb9-127">CommonParameters</span></span>
<span data-ttu-id="f1fb9-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1fb9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1fb9-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1fb9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1fb9-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1fb9-130">INPUTS</span></span>

### <span data-ttu-id="f1fb9-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f1fb9-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="f1fb9-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1fb9-132">OUTPUTS</span></span>

### <span data-ttu-id="f1fb9-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f1fb9-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="f1fb9-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f1fb9-134">NOTES</span></span>

## <span data-ttu-id="f1fb9-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f1fb9-135">RELATED LINKS</span></span>
