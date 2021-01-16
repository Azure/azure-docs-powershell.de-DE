---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 62f9a2d77ce3a5b34b25c98d681bcfba55ae62e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296890"
---
# <span data-ttu-id="54a97-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="54a97-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="54a97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54a97-102">SYNOPSIS</span></span>
<span data-ttu-id="54a97-103">Listen Sie alle verknüpften IoT-Hubs in einem Azure IoT Hub-Gerätebereitstellungsdienst auf, oder zeigen Sie Details an.</span><span class="sxs-lookup"><span data-stu-id="54a97-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="54a97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54a97-104">SYNTAX</span></span>

### <span data-ttu-id="54a97-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="54a97-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54a97-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="54a97-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54a97-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="54a97-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54a97-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54a97-108">DESCRIPTION</span></span>
<span data-ttu-id="54a97-109">Eine Einführung in den Bereitstellungsdienst für Azure IoT-Hub-Geräte finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="54a97-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="54a97-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54a97-110">EXAMPLES</span></span>

### <span data-ttu-id="54a97-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54a97-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="54a97-112">Listen Sie alle verknüpften IoT-Hubs in "myiotdps" auf.</span><span class="sxs-lookup"><span data-stu-id="54a97-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="54a97-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="54a97-113">Example 2</span></span>
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

<span data-ttu-id="54a97-114">Zeigen Sie Details des verknüpften IoT-Hubs "myiothub1" in einem Azure IoT -Hub-Gerätebereitstellungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="54a97-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="54a97-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54a97-115">PARAMETERS</span></span>

### <span data-ttu-id="54a97-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a97-116">-DefaultProfile</span></span>
<span data-ttu-id="54a97-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54a97-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54a97-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="54a97-118">-DpsObject</span></span>
<span data-ttu-id="54a97-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="54a97-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="54a97-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="54a97-120">-LinkedHubName</span></span>
<span data-ttu-id="54a97-121">Hostname des verknüpften IoT Hubs</span><span class="sxs-lookup"><span data-stu-id="54a97-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="54a97-122">-Name</span><span class="sxs-lookup"><span data-stu-id="54a97-122">-Name</span></span>
<span data-ttu-id="54a97-123">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="54a97-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="54a97-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54a97-124">-ResourceGroupName</span></span>
<span data-ttu-id="54a97-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="54a97-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="54a97-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54a97-126">-ResourceId</span></span>
<span data-ttu-id="54a97-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="54a97-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="54a97-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a97-128">CommonParameters</span></span>
<span data-ttu-id="54a97-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54a97-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a97-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54a97-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a97-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54a97-131">INPUTS</span></span>

### <span data-ttu-id="54a97-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="54a97-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="54a97-133">System.String</span><span class="sxs-lookup"><span data-stu-id="54a97-133">System.String</span></span>

## <span data-ttu-id="54a97-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54a97-134">OUTPUTS</span></span>

### <span data-ttu-id="54a97-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="54a97-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="54a97-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="54a97-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="54a97-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="54a97-137">NOTES</span></span>

## <span data-ttu-id="54a97-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="54a97-138">RELATED LINKS</span></span>
