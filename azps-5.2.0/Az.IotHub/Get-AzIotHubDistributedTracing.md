---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298760"
---
# <span data-ttu-id="e5d0d-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="e5d0d-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="e5d0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5d0d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d0d-103">Hier erhalten Sie die Einstellungen für die verteilte Ablaufverfolgung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="e5d0d-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="e5d0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5d0d-104">SYNTAX</span></span>

### <span data-ttu-id="e5d0d-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5d0d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5d0d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e5d0d-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5d0d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e5d0d-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5d0d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5d0d-108">DESCRIPTION</span></span>
<span data-ttu-id="e5d0d-109">Hier erhalten Sie die Einstellungen für die verteilte Ablaufverfolgung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="e5d0d-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="e5d0d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e5d0d-110">EXAMPLES</span></span>

### <span data-ttu-id="e5d0d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5d0d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="e5d0d-112">Hier erhalten Sie die Einstellungen für die verteilte Ablaufverfolgung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="e5d0d-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="e5d0d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5d0d-113">PARAMETERS</span></span>

### <span data-ttu-id="e5d0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d0d-114">-DefaultProfile</span></span>
<span data-ttu-id="e5d0d-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5d0d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5d0d-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e5d0d-116">-DeviceId</span></span>
<span data-ttu-id="e5d0d-117">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="e5d0d-117">Target Device Id.</span></span>

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

### <span data-ttu-id="e5d0d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5d0d-118">-InputObject</span></span>
<span data-ttu-id="e5d0d-119">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="e5d0d-119">IotHub object</span></span>

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

### <span data-ttu-id="e5d0d-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e5d0d-120">-IotHubName</span></span>
<span data-ttu-id="e5d0d-121">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="e5d0d-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e5d0d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5d0d-122">-ResourceGroupName</span></span>
<span data-ttu-id="e5d0d-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e5d0d-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e5d0d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5d0d-124">-ResourceId</span></span>
<span data-ttu-id="e5d0d-125">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e5d0d-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e5d0d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d0d-126">CommonParameters</span></span>
<span data-ttu-id="e5d0d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5d0d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d0d-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5d0d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d0d-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e5d0d-129">INPUTS</span></span>

### <span data-ttu-id="e5d0d-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e5d0d-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e5d0d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e5d0d-131">System.String</span></span>

## <span data-ttu-id="e5d0d-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e5d0d-132">OUTPUTS</span></span>

### <span data-ttu-id="e5d0d-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="e5d0d-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="e5d0d-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e5d0d-134">NOTES</span></span>

## <span data-ttu-id="e5d0d-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e5d0d-135">RELATED LINKS</span></span>
