---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175376"
---
# <span data-ttu-id="cb3b7-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb3b7-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="cb3b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb3b7-102">SYNOPSIS</span></span>
<span data-ttu-id="cb3b7-103">Ruft die edgespeicher-Konten auf dem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="cb3b7-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="cb3b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb3b7-104">SYNTAX</span></span>

### <span data-ttu-id="cb3b7-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb3b7-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb3b7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb3b7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb3b7-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb3b7-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb3b7-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb3b7-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="cb3b7-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb3b7-109">DESCRIPTION</span></span>
<span data-ttu-id="cb3b7-110">Das Cmdlet " **Get-AzStackEdgeStorageAccount** " Ruft die Edge-Speicherkonten ab, die auf einem Stack-Edge-Gerät verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="cb3b7-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="cb3b7-111">Sie können den Namen als Parameter im Cmdlet angeben, um die Informationen eines bestimmten edgespeicher-Kontos abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cb3b7-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="cb3b7-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb3b7-112">EXAMPLES</span></span>

### <span data-ttu-id="cb3b7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cb3b7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="cb3b7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cb3b7-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="cb3b7-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="cb3b7-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="cb3b7-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="cb3b7-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="cb3b7-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb3b7-117">PARAMETERS</span></span>

### <span data-ttu-id="cb3b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb3b7-118">-DefaultProfile</span></span>
<span data-ttu-id="cb3b7-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb3b7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb3b7-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cb3b7-120">-DeviceName</span></span>
<span data-ttu-id="cb3b7-121">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="cb3b7-121">Device Name</span></span>

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

### <span data-ttu-id="cb3b7-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="cb3b7-122">-DeviceObject</span></span>
<span data-ttu-id="cb3b7-123">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="cb3b7-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="cb3b7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cb3b7-124">-Name</span></span>
<span data-ttu-id="cb3b7-125">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="cb3b7-125">Resource Name</span></span>

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

### <span data-ttu-id="cb3b7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb3b7-126">-ResourceGroupName</span></span>
<span data-ttu-id="cb3b7-127">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="cb3b7-127">Resource Group Name</span></span>

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

### <span data-ttu-id="cb3b7-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cb3b7-128">-ResourceId</span></span>
<span data-ttu-id="cb3b7-129">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="cb3b7-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="cb3b7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb3b7-130">CommonParameters</span></span>
<span data-ttu-id="cb3b7-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb3b7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb3b7-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb3b7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb3b7-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb3b7-133">INPUTS</span></span>

### <span data-ttu-id="cb3b7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cb3b7-134">System.String</span></span>

### <span data-ttu-id="cb3b7-135">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="cb3b7-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="cb3b7-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb3b7-136">OUTPUTS</span></span>

### <span data-ttu-id="cb3b7-137">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb3b7-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="cb3b7-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb3b7-138">NOTES</span></span>

## <span data-ttu-id="cb3b7-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb3b7-139">RELATED LINKS</span></span>
