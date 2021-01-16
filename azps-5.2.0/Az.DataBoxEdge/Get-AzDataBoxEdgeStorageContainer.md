---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3f7ebc42efc2ad5ba73079fd2774614b941f432b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293555"
---
# <span data-ttu-id="45c33-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="45c33-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="45c33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45c33-102">SYNOPSIS</span></span>
<span data-ttu-id="45c33-103">Ruft die Container für ein Edgespeicherkonto auf einem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="45c33-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="45c33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45c33-104">SYNTAX</span></span>

### <span data-ttu-id="45c33-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="45c33-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45c33-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45c33-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45c33-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="45c33-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45c33-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45c33-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="45c33-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45c33-109">DESCRIPTION</span></span>
<span data-ttu-id="45c33-110">Das **Cmdlet "Get-AzDataBoxEdgeStorageContainer"** ruft den Speichercontainer für ein Edgespeicherkonto auf einem Data Box Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="45c33-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="45c33-111">Sie können den Namen im Cmdlet als Parameter angeben, um die Details eines bestimmten Speichercontainers abrufen zu können.</span><span class="sxs-lookup"><span data-stu-id="45c33-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="45c33-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="45c33-112">EXAMPLES</span></span>

### <span data-ttu-id="45c33-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="45c33-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="45c33-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="45c33-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="45c33-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="45c33-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="45c33-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45c33-116">PARAMETERS</span></span>

### <span data-ttu-id="45c33-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c33-117">-DefaultProfile</span></span>
<span data-ttu-id="45c33-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45c33-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45c33-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="45c33-119">-DeviceName</span></span>
<span data-ttu-id="45c33-120">Gerätename</span><span class="sxs-lookup"><span data-stu-id="45c33-120">Device Name</span></span>

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

### <span data-ttu-id="45c33-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="45c33-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="45c33-122">Bereitstellen des vorhandenen EdgeStorageAccount-Namens</span><span class="sxs-lookup"><span data-stu-id="45c33-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="45c33-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="45c33-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="45c33-124">Bereitstellen eines vorhandenen EdgeStorageAccount-Objekts</span><span class="sxs-lookup"><span data-stu-id="45c33-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45c33-125">-Name</span><span class="sxs-lookup"><span data-stu-id="45c33-125">-Name</span></span>
<span data-ttu-id="45c33-126">Name des EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="45c33-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="45c33-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c33-127">-ResourceGroupName</span></span>
<span data-ttu-id="45c33-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="45c33-128">Resource Group Name</span></span>

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

### <span data-ttu-id="45c33-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45c33-129">-ResourceId</span></span>
<span data-ttu-id="45c33-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="45c33-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="45c33-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c33-131">CommonParameters</span></span>
<span data-ttu-id="45c33-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45c33-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c33-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45c33-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c33-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="45c33-134">INPUTS</span></span>

### <span data-ttu-id="45c33-135">System.String</span><span class="sxs-lookup"><span data-stu-id="45c33-135">System.String</span></span>

### <span data-ttu-id="45c33-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45c33-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="45c33-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="45c33-137">OUTPUTS</span></span>

### <span data-ttu-id="45c33-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="45c33-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="45c33-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="45c33-139">NOTES</span></span>

## <span data-ttu-id="45c33-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="45c33-140">RELATED LINKS</span></span>
