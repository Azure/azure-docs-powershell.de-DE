---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: efb9c7828417596afecc21fc5e5c2b2b8f7c81b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946426"
---
# <span data-ttu-id="c53b0-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c53b0-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c53b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c53b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c53b0-103">Ruft die Speicherkontoanmeldeinformationen ab, die dem Speicherkonto auf dem Gerät entsprechend sind.</span><span class="sxs-lookup"><span data-stu-id="c53b0-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="c53b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c53b0-104">SYNTAX</span></span>

### <span data-ttu-id="c53b0-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c53b0-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c53b0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c53b0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c53b0-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c53b0-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c53b0-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c53b0-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="c53b0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c53b0-109">DESCRIPTION</span></span>
<span data-ttu-id="c53b0-110">Das **Get-AzStackEdgeStorageAccountCredential-Cmdlet** ruft die Speicherkontoanmeldeinformationen für das entsprechende Speicherkonto auf dem Stack Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="c53b0-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="c53b0-111">Sie können Die Parameter Name, Ressourcengruppenname und Gerätename angeben, um Informationen zu einem bestimmten Speicherkonto zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c53b0-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="c53b0-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c53b0-112">EXAMPLES</span></span>

### <span data-ttu-id="c53b0-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c53b0-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="c53b0-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c53b0-114">PARAMETERS</span></span>

### <span data-ttu-id="c53b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c53b0-115">-DefaultProfile</span></span>
<span data-ttu-id="c53b0-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c53b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c53b0-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c53b0-117">-DeviceName</span></span>
<span data-ttu-id="c53b0-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="c53b0-118">Device Name</span></span>

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

### <span data-ttu-id="c53b0-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c53b0-119">-DeviceObject</span></span>
<span data-ttu-id="c53b0-120">Bitte geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="c53b0-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="c53b0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c53b0-121">-Name</span></span>
<span data-ttu-id="c53b0-122">Name des zu verwendende Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="c53b0-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: StorageAccountCredentialName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c53b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c53b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="c53b0-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="c53b0-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c53b0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c53b0-125">-ResourceId</span></span>
<span data-ttu-id="c53b0-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c53b0-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="c53b0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c53b0-127">CommonParameters</span></span>
<span data-ttu-id="c53b0-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c53b0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c53b0-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c53b0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c53b0-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c53b0-130">INPUTS</span></span>

### <span data-ttu-id="c53b0-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c53b0-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="c53b0-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c53b0-132">OUTPUTS</span></span>

### <span data-ttu-id="c53b0-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c53b0-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c53b0-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c53b0-134">NOTES</span></span>

## <span data-ttu-id="c53b0-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c53b0-135">RELATED LINKS</span></span>
