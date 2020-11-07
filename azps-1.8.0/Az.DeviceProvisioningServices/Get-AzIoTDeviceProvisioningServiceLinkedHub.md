---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: ec7f6e6bd402086084bee387be6a0563a6bf0c5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661130"
---
# <span data-ttu-id="52a2f-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="52a2f-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="52a2f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="52a2f-103">Listen Sie alle oder Details zu verknüpften viele Hubs in einem Azure-viel-Hub-Device-Bereitstellungsdienst auf.</span><span class="sxs-lookup"><span data-stu-id="52a2f-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="52a2f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52a2f-104">SYNTAX</span></span>

### <span data-ttu-id="52a2f-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="52a2f-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52a2f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="52a2f-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52a2f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="52a2f-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52a2f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52a2f-108">DESCRIPTION</span></span>
<span data-ttu-id="52a2f-109">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="52a2f-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="52a2f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52a2f-110">EXAMPLES</span></span>

### <span data-ttu-id="52a2f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="52a2f-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="52a2f-112">Listen Sie alle verknüpften viele Hubs in "myiotdps" auf.</span><span class="sxs-lookup"><span data-stu-id="52a2f-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="52a2f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="52a2f-113">Example 2</span></span>
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

<span data-ttu-id="52a2f-114">Zeigen Sie Details des verknüpften viele-Hubs "myiothub1" in einem Azure-viel-Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="52a2f-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="52a2f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="52a2f-115">PARAMETERS</span></span>

### <span data-ttu-id="52a2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a2f-116">-DefaultProfile</span></span>
<span data-ttu-id="52a2f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52a2f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52a2f-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="52a2f-118">-DpsObject</span></span>
<span data-ttu-id="52a2f-119">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="52a2f-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="52a2f-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="52a2f-120">-LinkedHubName</span></span>
<span data-ttu-id="52a2f-121">Hostname des verknüpften Zahl-Hubs</span><span class="sxs-lookup"><span data-stu-id="52a2f-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="52a2f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="52a2f-122">-Name</span></span>
<span data-ttu-id="52a2f-123">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="52a2f-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="52a2f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a2f-124">-ResourceGroupName</span></span>
<span data-ttu-id="52a2f-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="52a2f-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="52a2f-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="52a2f-126">-ResourceId</span></span>
<span data-ttu-id="52a2f-127">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="52a2f-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="52a2f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a2f-128">CommonParameters</span></span>
<span data-ttu-id="52a2f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52a2f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a2f-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52a2f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a2f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52a2f-131">INPUTS</span></span>

### <span data-ttu-id="52a2f-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="52a2f-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="52a2f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="52a2f-133">System.String</span></span>

## <span data-ttu-id="52a2f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52a2f-134">OUTPUTS</span></span>

### <span data-ttu-id="52a2f-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="52a2f-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="52a2f-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="52a2f-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="52a2f-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="52a2f-137">NOTES</span></span>

## <span data-ttu-id="52a2f-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52a2f-138">RELATED LINKS</span></span>
