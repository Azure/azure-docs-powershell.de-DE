---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 8dba984529d52dad6d256a5ad40b7594e561f324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942928"
---
# <span data-ttu-id="c06bc-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c06bc-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c06bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c06bc-102">SYNOPSIS</span></span>
<span data-ttu-id="c06bc-103">Ruft die Speicherkontoanmeldeinformationen ab, die dem Speicherkonto auf dem Gerät entsprechend sind.</span><span class="sxs-lookup"><span data-stu-id="c06bc-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="c06bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c06bc-104">SYNTAX</span></span>

### <span data-ttu-id="c06bc-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c06bc-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c06bc-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c06bc-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c06bc-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c06bc-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c06bc-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c06bc-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="c06bc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c06bc-109">DESCRIPTION</span></span>
<span data-ttu-id="c06bc-110">Das **Get-AzDataBoxEdgeStorageAccountCredential-Cmdlet** ruft die Speicherkontoanmeldeinformationen für das entsprechende Speicherkonto auf dem Data Box Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="c06bc-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="c06bc-111">Sie können Die Parameter Name, Ressourcengruppenname und Gerätename angeben, um Informationen zu einem bestimmten Speicherkonto zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c06bc-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="c06bc-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c06bc-112">EXAMPLES</span></span>

### <span data-ttu-id="c06bc-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c06bc-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="c06bc-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c06bc-114">PARAMETERS</span></span>

### <span data-ttu-id="c06bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06bc-115">-DefaultProfile</span></span>
<span data-ttu-id="c06bc-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c06bc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c06bc-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c06bc-117">-DeviceName</span></span>
<span data-ttu-id="c06bc-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="c06bc-118">Device Name</span></span>

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

### <span data-ttu-id="c06bc-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c06bc-119">-DeviceObject</span></span>
<span data-ttu-id="c06bc-120">Bitte geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="c06bc-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="c06bc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c06bc-121">-Name</span></span>
<span data-ttu-id="c06bc-122">Name des zu verwendende Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="c06bc-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="c06bc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c06bc-123">-ResourceGroupName</span></span>
<span data-ttu-id="c06bc-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="c06bc-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c06bc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c06bc-125">-ResourceId</span></span>
<span data-ttu-id="c06bc-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c06bc-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="c06bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06bc-127">CommonParameters</span></span>
<span data-ttu-id="c06bc-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c06bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06bc-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c06bc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06bc-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c06bc-130">INPUTS</span></span>

### <span data-ttu-id="c06bc-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c06bc-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="c06bc-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c06bc-132">OUTPUTS</span></span>

### <span data-ttu-id="c06bc-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c06bc-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c06bc-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c06bc-134">NOTES</span></span>

## <span data-ttu-id="c06bc-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c06bc-135">RELATED LINKS</span></span>
