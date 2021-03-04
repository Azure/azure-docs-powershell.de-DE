---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 5aff957c16fa6fefb52706f70016092a37cdcb3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932835"
---
# <span data-ttu-id="43415-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="43415-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="43415-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43415-102">SYNOPSIS</span></span>
<span data-ttu-id="43415-103">Listen Sie alle auf, oder zeigen Sie Details zu verknüpften IoT-Hubs in einem Azure IoT Hub-Gerätebereitstellungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="43415-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="43415-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43415-104">SYNTAX</span></span>

### <span data-ttu-id="43415-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="43415-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43415-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="43415-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43415-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="43415-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43415-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43415-108">DESCRIPTION</span></span>
<span data-ttu-id="43415-109">Eine Einführung in den Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="43415-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="43415-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43415-110">EXAMPLES</span></span>

### <span data-ttu-id="43415-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43415-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="43415-112">Listen Sie alle verknüpften IoT-Hubs in "myiotdps" auf.</span><span class="sxs-lookup"><span data-stu-id="43415-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="43415-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="43415-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="43415-114">Zeigen Sie Details des verknüpften IoT Hubs "myiothub1" in einem Azure IoT Hub-Gerätebereitstellungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="43415-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="43415-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="43415-115">PARAMETERS</span></span>

### <span data-ttu-id="43415-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43415-116">-DefaultProfile</span></span>
<span data-ttu-id="43415-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43415-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43415-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="43415-118">-DpsObject</span></span>
<span data-ttu-id="43415-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="43415-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43415-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="43415-120">-LinkedHubName</span></span>
<span data-ttu-id="43415-121">Hostname des verknüpften IoT Hub</span><span class="sxs-lookup"><span data-stu-id="43415-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="43415-122">-Name</span><span class="sxs-lookup"><span data-stu-id="43415-122">-Name</span></span>
<span data-ttu-id="43415-123">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="43415-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="43415-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43415-124">-ResourceGroupName</span></span>
<span data-ttu-id="43415-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="43415-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="43415-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43415-126">-ResourceId</span></span>
<span data-ttu-id="43415-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="43415-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="43415-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43415-128">CommonParameters</span></span>
<span data-ttu-id="43415-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43415-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43415-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43415-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43415-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43415-131">INPUTS</span></span>

### <span data-ttu-id="43415-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="43415-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="43415-133">System.String</span><span class="sxs-lookup"><span data-stu-id="43415-133">System.String</span></span>

## <span data-ttu-id="43415-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43415-134">OUTPUTS</span></span>

### <span data-ttu-id="43415-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="43415-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="43415-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="43415-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="43415-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="43415-137">NOTES</span></span>

## <span data-ttu-id="43415-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="43415-138">RELATED LINKS</span></span>
