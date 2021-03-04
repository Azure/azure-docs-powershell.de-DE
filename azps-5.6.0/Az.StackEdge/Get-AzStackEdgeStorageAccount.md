---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: a5844e4d03be96d4835a7bf83b2128958cee0b5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939856"
---
# <span data-ttu-id="286fd-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="286fd-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="286fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="286fd-102">SYNOPSIS</span></span>
<span data-ttu-id="286fd-103">Ruft die Edgespeicherkonten auf dem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="286fd-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="286fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="286fd-104">SYNTAX</span></span>

### <span data-ttu-id="286fd-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="286fd-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="286fd-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="286fd-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="286fd-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="286fd-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="286fd-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="286fd-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="286fd-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="286fd-109">DESCRIPTION</span></span>
<span data-ttu-id="286fd-110">Das **Get-AzStackEdgeStorageAccount-Cmdlet** ruft die Edgespeicherkonten ab, die auf einem Stack Edge-Gerät verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="286fd-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="286fd-111">Sie können den Namen als Parameter im Cmdlet angeben, um die Informationen eines bestimmten Edgespeicherkontos zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="286fd-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="286fd-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="286fd-112">EXAMPLES</span></span>

### <span data-ttu-id="286fd-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="286fd-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="286fd-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="286fd-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="286fd-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="286fd-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="286fd-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="286fd-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="286fd-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="286fd-117">PARAMETERS</span></span>

### <span data-ttu-id="286fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286fd-118">-DefaultProfile</span></span>
<span data-ttu-id="286fd-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="286fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="286fd-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="286fd-120">-DeviceName</span></span>
<span data-ttu-id="286fd-121">Gerätename</span><span class="sxs-lookup"><span data-stu-id="286fd-121">Device Name</span></span>

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

### <span data-ttu-id="286fd-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="286fd-122">-DeviceObject</span></span>
<span data-ttu-id="286fd-123">Bitte geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="286fd-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="286fd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="286fd-124">-Name</span></span>
<span data-ttu-id="286fd-125">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="286fd-125">Resource Name</span></span>

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

### <span data-ttu-id="286fd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="286fd-126">-ResourceGroupName</span></span>
<span data-ttu-id="286fd-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="286fd-127">Resource Group Name</span></span>

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

### <span data-ttu-id="286fd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="286fd-128">-ResourceId</span></span>
<span data-ttu-id="286fd-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="286fd-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="286fd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286fd-130">CommonParameters</span></span>
<span data-ttu-id="286fd-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="286fd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286fd-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="286fd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286fd-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="286fd-133">INPUTS</span></span>

### <span data-ttu-id="286fd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="286fd-134">System.String</span></span>

### <span data-ttu-id="286fd-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="286fd-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="286fd-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="286fd-136">OUTPUTS</span></span>

### <span data-ttu-id="286fd-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="286fd-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="286fd-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="286fd-138">NOTES</span></span>

## <span data-ttu-id="286fd-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="286fd-139">RELATED LINKS</span></span>
