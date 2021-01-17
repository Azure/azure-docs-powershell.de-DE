---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471741"
---
# <span data-ttu-id="5452b-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5452b-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="5452b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5452b-102">SYNOPSIS</span></span>
<span data-ttu-id="5452b-103">Ruft die Container für ein Edgespeicherkonto auf einem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="5452b-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="5452b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5452b-104">SYNTAX</span></span>

### <span data-ttu-id="5452b-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5452b-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5452b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5452b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5452b-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5452b-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5452b-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5452b-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="5452b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5452b-109">DESCRIPTION</span></span>
<span data-ttu-id="5452b-110">Das **Cmdlet "Get-AzStackEdgeStorageContainer"** ruft den Speichercontainer für ein Edgespeicherkonto auf einem Stack Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="5452b-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="5452b-111">Sie können den Namen im Cmdlet als Parameter angeben, um die Details eines bestimmten Speichercontainers abrufen zu können.</span><span class="sxs-lookup"><span data-stu-id="5452b-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="5452b-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5452b-112">EXAMPLES</span></span>

### <span data-ttu-id="5452b-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5452b-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="5452b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5452b-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="5452b-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5452b-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="5452b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5452b-116">PARAMETERS</span></span>

### <span data-ttu-id="5452b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5452b-117">-DefaultProfile</span></span>
<span data-ttu-id="5452b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5452b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5452b-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5452b-119">-DeviceName</span></span>
<span data-ttu-id="5452b-120">Gerätename</span><span class="sxs-lookup"><span data-stu-id="5452b-120">Device Name</span></span>

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

### <span data-ttu-id="5452b-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5452b-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="5452b-122">Bereitstellen des vorhandenen EdgeStorageAccount-Namens</span><span class="sxs-lookup"><span data-stu-id="5452b-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="5452b-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="5452b-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="5452b-124">Bereitstellen eines vorhandenen EdgeStorageAccount-Objekts</span><span class="sxs-lookup"><span data-stu-id="5452b-124">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="5452b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5452b-125">-Name</span></span>
<span data-ttu-id="5452b-126">Name des EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5452b-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="5452b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5452b-127">-ResourceGroupName</span></span>
<span data-ttu-id="5452b-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="5452b-128">Resource Group Name</span></span>

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

### <span data-ttu-id="5452b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5452b-129">-ResourceId</span></span>
<span data-ttu-id="5452b-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5452b-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="5452b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5452b-131">CommonParameters</span></span>
<span data-ttu-id="5452b-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5452b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5452b-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5452b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5452b-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5452b-134">INPUTS</span></span>

### <span data-ttu-id="5452b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5452b-135">System.String</span></span>

### <span data-ttu-id="5452b-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5452b-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="5452b-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5452b-137">OUTPUTS</span></span>

### <span data-ttu-id="5452b-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5452b-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="5452b-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5452b-139">NOTES</span></span>

## <span data-ttu-id="5452b-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5452b-140">RELATED LINKS</span></span>
