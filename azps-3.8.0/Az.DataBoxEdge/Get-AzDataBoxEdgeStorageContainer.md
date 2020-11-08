---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3f7ebc42efc2ad5ba73079fd2774614b941f432b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003618"
---
# <span data-ttu-id="f7c6b-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f7c6b-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="f7c6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c6b-103">Ruft die Container für ein edgespeicher-Konto auf einem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="f7c6b-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="f7c6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7c6b-104">SYNTAX</span></span>

### <span data-ttu-id="f7c6b-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7c6b-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7c6b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7c6b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7c6b-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7c6b-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7c6b-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7c6b-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="f7c6b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7c6b-109">DESCRIPTION</span></span>
<span data-ttu-id="f7c6b-110">Das Cmdlet " **Get-AzDataBoxEdgeStorageContainer** " Ruft den Speichercontainer für ein edgespeicher-Konto auf einem Daten Feld-Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="f7c6b-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="f7c6b-111">Sie können den Namen als Parameter im Cmdlet angeben, um die Details eines bestimmten Speichercontainers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f7c6b-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="f7c6b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7c6b-112">EXAMPLES</span></span>

### <span data-ttu-id="f7c6b-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7c6b-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="f7c6b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f7c6b-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="f7c6b-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f7c6b-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="f7c6b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7c6b-116">PARAMETERS</span></span>

### <span data-ttu-id="f7c6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c6b-117">-DefaultProfile</span></span>
<span data-ttu-id="f7c6b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7c6b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7c6b-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f7c6b-119">-DeviceName</span></span>
<span data-ttu-id="f7c6b-120">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="f7c6b-120">Device Name</span></span>

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

### <span data-ttu-id="f7c6b-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f7c6b-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="f7c6b-122">Angeben des vorhandenen EdgeStorageAccount-namens</span><span class="sxs-lookup"><span data-stu-id="f7c6b-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="f7c6b-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="f7c6b-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="f7c6b-124">Bereitstellen eines vorhandenen EdgeStorageAccount-Objekts</span><span class="sxs-lookup"><span data-stu-id="f7c6b-124">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="f7c6b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f7c6b-125">-Name</span></span>
<span data-ttu-id="f7c6b-126">Name des EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f7c6b-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="f7c6b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7c6b-127">-ResourceGroupName</span></span>
<span data-ttu-id="f7c6b-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f7c6b-128">Resource Group Name</span></span>

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

### <span data-ttu-id="f7c6b-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f7c6b-129">-ResourceId</span></span>
<span data-ttu-id="f7c6b-130">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="f7c6b-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="f7c6b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c6b-131">CommonParameters</span></span>
<span data-ttu-id="f7c6b-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7c6b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c6b-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7c6b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c6b-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7c6b-134">INPUTS</span></span>

### <span data-ttu-id="f7c6b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f7c6b-135">System.String</span></span>

### <span data-ttu-id="f7c6b-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7c6b-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="f7c6b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7c6b-137">OUTPUTS</span></span>

### <span data-ttu-id="f7c6b-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f7c6b-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="f7c6b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7c6b-139">NOTES</span></span>

## <span data-ttu-id="f7c6b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7c6b-140">RELATED LINKS</span></span>
