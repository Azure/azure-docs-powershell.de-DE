---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: ec84ee72caadc4d49c29a72e1e5171e589dc11d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936920"
---
# <span data-ttu-id="7262d-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="7262d-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="7262d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7262d-102">SYNOPSIS</span></span>
<span data-ttu-id="7262d-103">Drucken Sie eine durch Kommas getrennte Liste der zugewiesenen untergeordneten Geräte.</span><span class="sxs-lookup"><span data-stu-id="7262d-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="7262d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7262d-104">SYNTAX</span></span>

### <span data-ttu-id="7262d-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7262d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7262d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7262d-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7262d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7262d-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7262d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7262d-108">DESCRIPTION</span></span>
<span data-ttu-id="7262d-109">Zeigen Sie alle zugewiesenen Nicht-Edge-Geräte als durch Kommas getrennte Liste aller Edgegeräte oder angegebenen Geräte an.</span><span class="sxs-lookup"><span data-stu-id="7262d-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="7262d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7262d-110">EXAMPLES</span></span>

### <span data-ttu-id="7262d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7262d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="7262d-112">Zeigen Sie alle zugewiesenen Nicht-Edge-Geräte als durch Kommas getrennte Liste an.</span><span class="sxs-lookup"><span data-stu-id="7262d-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="7262d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7262d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="7262d-114">Zeigen Sie alle zugewiesenen Nicht-Edge-Geräte als durch Kommas getrennte Liste aller Edgegeräte an.</span><span class="sxs-lookup"><span data-stu-id="7262d-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="7262d-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7262d-115">PARAMETERS</span></span>

### <span data-ttu-id="7262d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7262d-116">-DefaultProfile</span></span>
<span data-ttu-id="7262d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7262d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7262d-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7262d-118">-DeviceId</span></span>
<span data-ttu-id="7262d-119">ID des Edgegeräts.</span><span class="sxs-lookup"><span data-stu-id="7262d-119">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7262d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7262d-120">-InputObject</span></span>
<span data-ttu-id="7262d-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="7262d-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7262d-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7262d-122">-IotHubName</span></span>
<span data-ttu-id="7262d-123">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="7262d-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7262d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7262d-124">-ResourceGroupName</span></span>
<span data-ttu-id="7262d-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7262d-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7262d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7262d-126">-ResourceId</span></span>
<span data-ttu-id="7262d-127">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="7262d-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7262d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7262d-128">CommonParameters</span></span>
<span data-ttu-id="7262d-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7262d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7262d-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7262d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7262d-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7262d-131">INPUTS</span></span>

### <span data-ttu-id="7262d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7262d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7262d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7262d-133">System.String</span></span>

## <span data-ttu-id="7262d-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7262d-134">OUTPUTS</span></span>

### <span data-ttu-id="7262d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="7262d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="7262d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span><span class="sxs-lookup"><span data-stu-id="7262d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="7262d-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7262d-137">NOTES</span></span>

## <span data-ttu-id="7262d-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7262d-138">RELATED LINKS</span></span>
