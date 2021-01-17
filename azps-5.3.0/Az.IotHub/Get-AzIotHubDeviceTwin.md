---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472410"
---
# <span data-ttu-id="42418-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="42418-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="42418-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42418-102">SYNOPSIS</span></span>
<span data-ttu-id="42418-103">Ruft ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="42418-103">Gets a device twin.</span></span>

## <span data-ttu-id="42418-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42418-104">SYNTAX</span></span>

### <span data-ttu-id="42418-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="42418-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42418-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="42418-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42418-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="42418-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42418-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42418-108">DESCRIPTION</span></span>
<span data-ttu-id="42418-109">Ruft ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="42418-109">Gets a device twin.</span></span> <span data-ttu-id="42418-110">Weitere https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins Informationen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="42418-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="42418-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="42418-111">EXAMPLES</span></span>

### <span data-ttu-id="42418-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42418-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="42418-113">Gibt das Device -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="42418-113">Returns the device twin object.</span></span>

## <span data-ttu-id="42418-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42418-114">PARAMETERS</span></span>

### <span data-ttu-id="42418-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42418-115">-DefaultProfile</span></span>
<span data-ttu-id="42418-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42418-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42418-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="42418-117">-DeviceId</span></span>
<span data-ttu-id="42418-118">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="42418-118">Target Device Id.</span></span>

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

### <span data-ttu-id="42418-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42418-119">-InputObject</span></span>
<span data-ttu-id="42418-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="42418-120">IotHub object</span></span>

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

### <span data-ttu-id="42418-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="42418-121">-IotHubName</span></span>
<span data-ttu-id="42418-122">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="42418-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="42418-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42418-123">-ResourceGroupName</span></span>
<span data-ttu-id="42418-124">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="42418-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="42418-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42418-125">-ResourceId</span></span>
<span data-ttu-id="42418-126">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="42418-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="42418-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42418-127">CommonParameters</span></span>
<span data-ttu-id="42418-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42418-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42418-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42418-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42418-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="42418-130">INPUTS</span></span>

### <span data-ttu-id="42418-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="42418-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="42418-132">System.String</span><span class="sxs-lookup"><span data-stu-id="42418-132">System.String</span></span>

## <span data-ttu-id="42418-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="42418-133">OUTPUTS</span></span>

### <span data-ttu-id="42418-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="42418-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="42418-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="42418-135">NOTES</span></span>

## <span data-ttu-id="42418-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="42418-136">RELATED LINKS</span></span>
