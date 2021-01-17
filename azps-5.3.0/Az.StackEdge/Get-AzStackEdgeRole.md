---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472559"
---
# <span data-ttu-id="54a56-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="54a56-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="54a56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54a56-102">SYNOPSIS</span></span>
<span data-ttu-id="54a56-103">Ruft die verfügbaren Rollen für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="54a56-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="54a56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54a56-104">SYNTAX</span></span>

### <span data-ttu-id="54a56-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="54a56-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54a56-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54a56-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54a56-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="54a56-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54a56-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54a56-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="54a56-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54a56-109">DESCRIPTION</span></span>
<span data-ttu-id="54a56-110">Das **Cmdlet "Get-AzStackEdgeRole"** ruft die verfügbaren IoT-Rollen für ein Stack Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="54a56-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="54a56-111">Sie können den Parameter "Name" erwähnen, um die Details einer bestimmten IoT-Rolle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="54a56-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="54a56-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54a56-112">EXAMPLES</span></span>

### <span data-ttu-id="54a56-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54a56-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="54a56-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54a56-114">PARAMETERS</span></span>

### <span data-ttu-id="54a56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a56-115">-DefaultProfile</span></span>
<span data-ttu-id="54a56-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54a56-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54a56-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="54a56-117">-DeviceName</span></span>
<span data-ttu-id="54a56-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="54a56-118">Device Name</span></span>

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

### <span data-ttu-id="54a56-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="54a56-119">-DeviceObject</span></span>
<span data-ttu-id="54a56-120">Geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="54a56-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="54a56-121">-Name</span><span class="sxs-lookup"><span data-stu-id="54a56-121">-Name</span></span>
<span data-ttu-id="54a56-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="54a56-122">Resource Name</span></span>

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

### <span data-ttu-id="54a56-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54a56-123">-ResourceGroupName</span></span>
<span data-ttu-id="54a56-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="54a56-124">Resource Group Name</span></span>

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

### <span data-ttu-id="54a56-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54a56-125">-ResourceId</span></span>
<span data-ttu-id="54a56-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="54a56-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="54a56-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a56-127">CommonParameters</span></span>
<span data-ttu-id="54a56-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54a56-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a56-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54a56-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a56-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54a56-130">INPUTS</span></span>

### <span data-ttu-id="54a56-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="54a56-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="54a56-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54a56-132">OUTPUTS</span></span>

### <span data-ttu-id="54a56-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="54a56-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="54a56-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="54a56-134">NOTES</span></span>

## <span data-ttu-id="54a56-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="54a56-135">RELATED LINKS</span></span>
