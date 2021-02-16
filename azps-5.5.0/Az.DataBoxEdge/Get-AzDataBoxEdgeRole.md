---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9bda923d7a0e7e999ae8368fd648ee6745cbb226
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170957"
---
# <span data-ttu-id="b3a57-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b3a57-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="b3a57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3a57-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a57-103">Ruft die verfügbaren Rollen für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="b3a57-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="b3a57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3a57-104">SYNTAX</span></span>

### <span data-ttu-id="b3a57-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b3a57-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3a57-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3a57-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3a57-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3a57-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3a57-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3a57-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="b3a57-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3a57-109">DESCRIPTION</span></span>
<span data-ttu-id="b3a57-110">Das **Cmdlet "Get-AzDataBoxEdgeRole"** ruft die verfügbaren IoT-Rollen für ein Data Box-Edgegerät ab.</span><span class="sxs-lookup"><span data-stu-id="b3a57-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="b3a57-111">Sie können den Parameter "Name" erwähnen, um die Details einer bestimmten IoT-Rolle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b3a57-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="b3a57-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3a57-112">EXAMPLES</span></span>

### <span data-ttu-id="b3a57-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b3a57-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="b3a57-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3a57-114">PARAMETERS</span></span>

### <span data-ttu-id="b3a57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a57-115">-DefaultProfile</span></span>
<span data-ttu-id="b3a57-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3a57-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a57-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b3a57-117">-DeviceName</span></span>
<span data-ttu-id="b3a57-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="b3a57-118">Device Name</span></span>

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

### <span data-ttu-id="b3a57-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="b3a57-119">-DeviceObject</span></span>
<span data-ttu-id="b3a57-120">Geben Sie bitte ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="b3a57-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="b3a57-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b3a57-121">-Name</span></span>
<span data-ttu-id="b3a57-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="b3a57-122">Resource Name</span></span>

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

### <span data-ttu-id="b3a57-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a57-123">-ResourceGroupName</span></span>
<span data-ttu-id="b3a57-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="b3a57-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b3a57-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a57-125">-ResourceId</span></span>
<span data-ttu-id="b3a57-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a57-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="b3a57-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a57-127">CommonParameters</span></span>
<span data-ttu-id="b3a57-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a57-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a57-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3a57-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a57-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3a57-130">INPUTS</span></span>

### <span data-ttu-id="b3a57-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b3a57-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="b3a57-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3a57-132">OUTPUTS</span></span>

### <span data-ttu-id="b3a57-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b3a57-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="b3a57-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b3a57-134">NOTES</span></span>

## <span data-ttu-id="b3a57-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b3a57-135">RELATED LINKS</span></span>
