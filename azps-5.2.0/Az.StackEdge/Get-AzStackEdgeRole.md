---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359119"
---
# <span data-ttu-id="30829-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="30829-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="30829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30829-102">SYNOPSIS</span></span>
<span data-ttu-id="30829-103">Ruft die verfügbaren Rollen für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="30829-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="30829-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30829-104">SYNTAX</span></span>

### <span data-ttu-id="30829-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="30829-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30829-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30829-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30829-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="30829-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30829-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30829-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="30829-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30829-109">DESCRIPTION</span></span>
<span data-ttu-id="30829-110">Das **Cmdlet "Get-AzStackEdgeRole"** ruft die verfügbaren IoT-Rollen für ein Stack Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="30829-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="30829-111">Sie können den Parameter "Name" erwähnen, um die Details einer bestimmten IoT-Rolle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="30829-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="30829-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="30829-112">EXAMPLES</span></span>

### <span data-ttu-id="30829-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="30829-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="30829-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30829-114">PARAMETERS</span></span>

### <span data-ttu-id="30829-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30829-115">-DefaultProfile</span></span>
<span data-ttu-id="30829-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="30829-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30829-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="30829-117">-DeviceName</span></span>
<span data-ttu-id="30829-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="30829-118">Device Name</span></span>

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

### <span data-ttu-id="30829-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="30829-119">-DeviceObject</span></span>
<span data-ttu-id="30829-120">Geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="30829-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="30829-121">-Name</span><span class="sxs-lookup"><span data-stu-id="30829-121">-Name</span></span>
<span data-ttu-id="30829-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="30829-122">Resource Name</span></span>

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

### <span data-ttu-id="30829-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30829-123">-ResourceGroupName</span></span>
<span data-ttu-id="30829-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="30829-124">Resource Group Name</span></span>

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

### <span data-ttu-id="30829-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30829-125">-ResourceId</span></span>
<span data-ttu-id="30829-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="30829-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="30829-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30829-127">CommonParameters</span></span>
<span data-ttu-id="30829-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30829-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30829-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30829-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30829-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="30829-130">INPUTS</span></span>

### <span data-ttu-id="30829-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="30829-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="30829-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="30829-132">OUTPUTS</span></span>

### <span data-ttu-id="30829-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="30829-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="30829-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="30829-134">NOTES</span></span>

## <span data-ttu-id="30829-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="30829-135">RELATED LINKS</span></span>
