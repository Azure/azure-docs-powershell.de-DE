---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 71540063e9eb4323d94a579df8f6489719f7c3fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948336"
---
# <span data-ttu-id="51650-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="51650-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="51650-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51650-102">SYNOPSIS</span></span>
<span data-ttu-id="51650-103">Ruft die Container für ein Edgespeicherkonto auf einem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="51650-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="51650-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51650-104">SYNTAX</span></span>

### <span data-ttu-id="51650-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="51650-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51650-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51650-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51650-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="51650-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51650-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51650-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="51650-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51650-109">DESCRIPTION</span></span>
<span data-ttu-id="51650-110">Das **Get-AzStackEdgeStorageContainer-Cmdlet** ruft den Speichercontainer für ein Edgespeicherkonto auf einem Stack Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="51650-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="51650-111">Sie können den Namen als Parameter im Cmdlet angeben, um die Details eines bestimmten Speichercontainers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="51650-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="51650-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="51650-112">EXAMPLES</span></span>

### <span data-ttu-id="51650-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="51650-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="51650-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="51650-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="51650-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="51650-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="51650-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="51650-116">PARAMETERS</span></span>

### <span data-ttu-id="51650-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51650-117">-DefaultProfile</span></span>
<span data-ttu-id="51650-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51650-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51650-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="51650-119">-DeviceName</span></span>
<span data-ttu-id="51650-120">Gerätename</span><span class="sxs-lookup"><span data-stu-id="51650-120">Device Name</span></span>

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

### <span data-ttu-id="51650-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="51650-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="51650-122">Bereitstellen des Vorhandenen EdgeStorageAccount-Namens</span><span class="sxs-lookup"><span data-stu-id="51650-122">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51650-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="51650-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="51650-124">Bereitstellen eines vorhandenen EdgeStorageAccount-Objekts</span><span class="sxs-lookup"><span data-stu-id="51650-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51650-125">-Name</span><span class="sxs-lookup"><span data-stu-id="51650-125">-Name</span></span>
<span data-ttu-id="51650-126">Name des EdgeStorageContainers</span><span class="sxs-lookup"><span data-stu-id="51650-126">Name of the EdgeStorageContainer</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageContainerName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51650-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51650-127">-ResourceGroupName</span></span>
<span data-ttu-id="51650-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="51650-128">Resource Group Name</span></span>

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

### <span data-ttu-id="51650-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51650-129">-ResourceId</span></span>
<span data-ttu-id="51650-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="51650-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51650-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51650-131">CommonParameters</span></span>
<span data-ttu-id="51650-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51650-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51650-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51650-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51650-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="51650-134">INPUTS</span></span>

### <span data-ttu-id="51650-135">System.String</span><span class="sxs-lookup"><span data-stu-id="51650-135">System.String</span></span>

### <span data-ttu-id="51650-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51650-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="51650-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="51650-137">OUTPUTS</span></span>

### <span data-ttu-id="51650-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="51650-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="51650-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="51650-139">NOTES</span></span>

## <span data-ttu-id="51650-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="51650-140">RELATED LINKS</span></span>
