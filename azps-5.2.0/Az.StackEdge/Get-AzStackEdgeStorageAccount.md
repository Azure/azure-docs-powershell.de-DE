---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367953"
---
# <span data-ttu-id="7947a-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7947a-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="7947a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7947a-102">SYNOPSIS</span></span>
<span data-ttu-id="7947a-103">Ruft die Edgespeicherkonten auf dem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="7947a-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="7947a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7947a-104">SYNTAX</span></span>

### <span data-ttu-id="7947a-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7947a-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7947a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7947a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7947a-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7947a-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7947a-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7947a-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="7947a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7947a-109">DESCRIPTION</span></span>
<span data-ttu-id="7947a-110">Das **Cmdlet "Get-AzStackEdgeStorageAccount"** ruft die Edgespeicherkonten auf einem Stack Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="7947a-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="7947a-111">Sie können den Namen als Parameter im Cmdlet angeben, um die Informationen eines bestimmten Edgespeicherkontos zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7947a-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="7947a-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7947a-112">EXAMPLES</span></span>

### <span data-ttu-id="7947a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7947a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="7947a-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7947a-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="7947a-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7947a-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="7947a-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="7947a-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="7947a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7947a-117">PARAMETERS</span></span>

### <span data-ttu-id="7947a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7947a-118">-DefaultProfile</span></span>
<span data-ttu-id="7947a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7947a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7947a-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7947a-120">-DeviceName</span></span>
<span data-ttu-id="7947a-121">Gerätename</span><span class="sxs-lookup"><span data-stu-id="7947a-121">Device Name</span></span>

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

### <span data-ttu-id="7947a-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="7947a-122">-DeviceObject</span></span>
<span data-ttu-id="7947a-123">Geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="7947a-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="7947a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7947a-124">-Name</span></span>
<span data-ttu-id="7947a-125">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="7947a-125">Resource Name</span></span>

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

### <span data-ttu-id="7947a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7947a-126">-ResourceGroupName</span></span>
<span data-ttu-id="7947a-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="7947a-127">Resource Group Name</span></span>

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

### <span data-ttu-id="7947a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7947a-128">-ResourceId</span></span>
<span data-ttu-id="7947a-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7947a-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="7947a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7947a-130">CommonParameters</span></span>
<span data-ttu-id="7947a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7947a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7947a-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7947a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7947a-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7947a-133">INPUTS</span></span>

### <span data-ttu-id="7947a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7947a-134">System.String</span></span>

### <span data-ttu-id="7947a-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7947a-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="7947a-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7947a-136">OUTPUTS</span></span>

### <span data-ttu-id="7947a-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7947a-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="7947a-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7947a-138">NOTES</span></span>

## <span data-ttu-id="7947a-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7947a-139">RELATED LINKS</span></span>
