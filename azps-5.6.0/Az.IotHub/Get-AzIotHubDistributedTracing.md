---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: 290b2ddcea6812b840b9c19ad2d44c4a0e461e64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936888"
---
# <span data-ttu-id="d01a8-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="d01a8-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="d01a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d01a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d01a8-103">Hier erhalten Sie die Einstellungen für die verteilte Ablaufverfolgung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="d01a8-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="d01a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d01a8-104">SYNTAX</span></span>

### <span data-ttu-id="d01a8-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d01a8-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d01a8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d01a8-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d01a8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d01a8-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d01a8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d01a8-108">DESCRIPTION</span></span>
<span data-ttu-id="d01a8-109">Hier erhalten Sie die Einstellungen für die verteilte Ablaufverfolgung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="d01a8-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="d01a8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d01a8-110">EXAMPLES</span></span>

### <span data-ttu-id="d01a8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d01a8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="d01a8-112">Hier erhalten Sie die Einstellungen für die verteilte Ablaufverfolgung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="d01a8-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="d01a8-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d01a8-113">PARAMETERS</span></span>

### <span data-ttu-id="d01a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d01a8-114">-DefaultProfile</span></span>
<span data-ttu-id="d01a8-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d01a8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d01a8-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d01a8-116">-DeviceId</span></span>
<span data-ttu-id="d01a8-117">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="d01a8-117">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d01a8-118">-InputObject</span></span>
<span data-ttu-id="d01a8-119">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="d01a8-119">IotHub object</span></span>

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

### <span data-ttu-id="d01a8-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d01a8-120">-IotHubName</span></span>
<span data-ttu-id="d01a8-121">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="d01a8-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d01a8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d01a8-122">-ResourceGroupName</span></span>
<span data-ttu-id="d01a8-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d01a8-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d01a8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d01a8-124">-ResourceId</span></span>
<span data-ttu-id="d01a8-125">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d01a8-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d01a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d01a8-126">CommonParameters</span></span>
<span data-ttu-id="d01a8-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d01a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d01a8-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d01a8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d01a8-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d01a8-129">INPUTS</span></span>

### <span data-ttu-id="d01a8-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d01a8-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d01a8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d01a8-131">System.String</span></span>

## <span data-ttu-id="d01a8-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d01a8-132">OUTPUTS</span></span>

### <span data-ttu-id="d01a8-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="d01a8-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="d01a8-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d01a8-134">NOTES</span></span>

## <span data-ttu-id="d01a8-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d01a8-135">RELATED LINKS</span></span>
