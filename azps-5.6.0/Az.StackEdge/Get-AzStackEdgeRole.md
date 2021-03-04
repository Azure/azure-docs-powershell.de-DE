---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: c4d33dad9377c6ee53452c90b5d582413e2eee73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923923"
---
# <span data-ttu-id="afdcd-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="afdcd-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="afdcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afdcd-102">SYNOPSIS</span></span>
<span data-ttu-id="afdcd-103">Ruft die verfügbaren Rollen für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="afdcd-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="afdcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afdcd-104">SYNTAX</span></span>

### <span data-ttu-id="afdcd-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="afdcd-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afdcd-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afdcd-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afdcd-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="afdcd-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afdcd-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afdcd-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="afdcd-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afdcd-109">DESCRIPTION</span></span>
<span data-ttu-id="afdcd-110">Das **Get-AzStackEdgeRole-Cmdlet** ruft die verfügbaren IoT-Rollen für ein Stack Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="afdcd-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="afdcd-111">Sie können den Parameter Name erwähnen, um die Details einer bestimmten IoT-Rolle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="afdcd-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="afdcd-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="afdcd-112">EXAMPLES</span></span>

### <span data-ttu-id="afdcd-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="afdcd-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="afdcd-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="afdcd-114">PARAMETERS</span></span>

### <span data-ttu-id="afdcd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afdcd-115">-DefaultProfile</span></span>
<span data-ttu-id="afdcd-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afdcd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afdcd-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="afdcd-117">-DeviceName</span></span>
<span data-ttu-id="afdcd-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="afdcd-118">Device Name</span></span>

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

### <span data-ttu-id="afdcd-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="afdcd-119">-DeviceObject</span></span>
<span data-ttu-id="afdcd-120">Bitte geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="afdcd-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="afdcd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="afdcd-121">-Name</span></span>
<span data-ttu-id="afdcd-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="afdcd-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: RoleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afdcd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afdcd-123">-ResourceGroupName</span></span>
<span data-ttu-id="afdcd-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="afdcd-124">Resource Group Name</span></span>

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

### <span data-ttu-id="afdcd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afdcd-125">-ResourceId</span></span>
<span data-ttu-id="afdcd-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="afdcd-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="afdcd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afdcd-127">CommonParameters</span></span>
<span data-ttu-id="afdcd-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afdcd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afdcd-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afdcd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afdcd-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="afdcd-130">INPUTS</span></span>

### <span data-ttu-id="afdcd-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="afdcd-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="afdcd-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="afdcd-132">OUTPUTS</span></span>

### <span data-ttu-id="afdcd-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="afdcd-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="afdcd-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="afdcd-134">NOTES</span></span>

## <span data-ttu-id="afdcd-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="afdcd-135">RELATED LINKS</span></span>
