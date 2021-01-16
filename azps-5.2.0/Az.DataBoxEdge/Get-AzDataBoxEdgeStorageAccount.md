---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 7b797b4088cab20ee1933ce88a2462288f04653e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362800"
---
# <span data-ttu-id="7c330-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c330-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="7c330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c330-102">SYNOPSIS</span></span>
<span data-ttu-id="7c330-103">Ruft die Edgespeicherkonten auf dem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="7c330-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="7c330-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c330-104">SYNTAX</span></span>

### <span data-ttu-id="7c330-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c330-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c330-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c330-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c330-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c330-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c330-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c330-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="7c330-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c330-109">DESCRIPTION</span></span>
<span data-ttu-id="7c330-110">Das **Cmdlet "Get-AzDataBoxEdgeStorageAccount"** ruft die Edgespeicherkonten ab, die auf einem Data Box -Edgegerät verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7c330-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="7c330-111">Sie können den Namen als Parameter im Cmdlet angeben, um die Informationen eines bestimmten Edgespeicherkontos zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7c330-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="7c330-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c330-112">EXAMPLES</span></span>

### <span data-ttu-id="7c330-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7c330-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="7c330-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7c330-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="7c330-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7c330-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="7c330-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="7c330-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="7c330-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c330-117">PARAMETERS</span></span>

### <span data-ttu-id="7c330-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c330-118">-DefaultProfile</span></span>
<span data-ttu-id="7c330-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c330-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c330-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7c330-120">-DeviceName</span></span>
<span data-ttu-id="7c330-121">Gerätename</span><span class="sxs-lookup"><span data-stu-id="7c330-121">Device Name</span></span>

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

### <span data-ttu-id="7c330-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="7c330-122">-DeviceObject</span></span>
<span data-ttu-id="7c330-123">Geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="7c330-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="7c330-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7c330-124">-Name</span></span>
<span data-ttu-id="7c330-125">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="7c330-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccountName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c330-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c330-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c330-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="7c330-127">Resource Group Name</span></span>

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

### <span data-ttu-id="7c330-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c330-128">-ResourceId</span></span>
<span data-ttu-id="7c330-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c330-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="7c330-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c330-130">CommonParameters</span></span>
<span data-ttu-id="7c330-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c330-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c330-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c330-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c330-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c330-133">INPUTS</span></span>

### <span data-ttu-id="7c330-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7c330-134">System.String</span></span>

### <span data-ttu-id="7c330-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7c330-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="7c330-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c330-136">OUTPUTS</span></span>

### <span data-ttu-id="7c330-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c330-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="7c330-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7c330-138">NOTES</span></span>

## <span data-ttu-id="7c330-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7c330-139">RELATED LINKS</span></span>
