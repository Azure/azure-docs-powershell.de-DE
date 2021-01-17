---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470635"
---
# <span data-ttu-id="39f9d-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="39f9d-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="39f9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="39f9d-103">Ruft die Anmeldeinformationen des Speicherkontos ab, die dem Speicherkonto auf dem Gerät entspricht.</span><span class="sxs-lookup"><span data-stu-id="39f9d-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="39f9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39f9d-104">SYNTAX</span></span>

### <span data-ttu-id="39f9d-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="39f9d-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39f9d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39f9d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39f9d-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="39f9d-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39f9d-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39f9d-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="39f9d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39f9d-109">DESCRIPTION</span></span>
<span data-ttu-id="39f9d-110">Das **Cmdlet "Get-AzDataBoxEdgeStorageAccountCredential"** ruft die Anmeldeinformationen des Speicherkontos für das entsprechende Speicherkonto auf dem Data Box Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="39f9d-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="39f9d-111">Sie können die Parameter "Name", "Ressourcengruppenname" und "Gerätename" angeben, um Informationen zu einem bestimmten Speicherkonto als Anmeldeinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="39f9d-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="39f9d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39f9d-112">EXAMPLES</span></span>

### <span data-ttu-id="39f9d-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39f9d-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="39f9d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39f9d-114">PARAMETERS</span></span>

### <span data-ttu-id="39f9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f9d-115">-DefaultProfile</span></span>
<span data-ttu-id="39f9d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39f9d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39f9d-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="39f9d-117">-DeviceName</span></span>
<span data-ttu-id="39f9d-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="39f9d-118">Device Name</span></span>

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

### <span data-ttu-id="39f9d-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="39f9d-119">-DeviceObject</span></span>
<span data-ttu-id="39f9d-120">Geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="39f9d-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="39f9d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="39f9d-121">-Name</span></span>
<span data-ttu-id="39f9d-122">Name des zu verwendende Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="39f9d-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="39f9d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f9d-123">-ResourceGroupName</span></span>
<span data-ttu-id="39f9d-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="39f9d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="39f9d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39f9d-125">-ResourceId</span></span>
<span data-ttu-id="39f9d-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="39f9d-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="39f9d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f9d-127">CommonParameters</span></span>
<span data-ttu-id="39f9d-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39f9d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f9d-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39f9d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f9d-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39f9d-130">INPUTS</span></span>

### <span data-ttu-id="39f9d-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="39f9d-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="39f9d-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39f9d-132">OUTPUTS</span></span>

### <span data-ttu-id="39f9d-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="39f9d-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="39f9d-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="39f9d-134">NOTES</span></span>

## <span data-ttu-id="39f9d-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="39f9d-135">RELATED LINKS</span></span>
