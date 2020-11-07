---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 346a09a635b72612c270889afd904a1535994624
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661136"
---
# <span data-ttu-id="b2064-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="b2064-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="b2064-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2064-102">SYNOPSIS</span></span>
<span data-ttu-id="b2064-103">Verbundener viel Hub zu einem Azure-viel-Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="b2064-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="b2064-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2064-104">SYNTAX</span></span>

### <span data-ttu-id="b2064-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2064-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2064-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b2064-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2064-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b2064-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2064-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2064-108">DESCRIPTION</span></span>
<span data-ttu-id="b2064-109">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="b2064-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="b2064-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2064-110">EXAMPLES</span></span>

### <span data-ttu-id="b2064-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b2064-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="b2064-112">Verbundener viel Hub zu einem Azure-viel-Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="b2064-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="b2064-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b2064-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="b2064-114">Verknüpfter viel-Hub zu einem Azure-viel-Hub-Device-Bereitstellungsdienst mit AllocationWeight und ApplyAllocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="b2064-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="b2064-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2064-115">PARAMETERS</span></span>

### <span data-ttu-id="b2064-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="b2064-116">-AllocationWeight</span></span>
<span data-ttu-id="b2064-117">Zuordnungs Gewicht des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="b2064-117">Allocation weight of the IoT Hub</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2064-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="b2064-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="b2064-119">Ein boolescher Wert, der angibt, ob die Zuweisungsrichtlinie auf den viel Hub angewendet werden soll</span><span class="sxs-lookup"><span data-stu-id="b2064-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2064-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2064-120">-DefaultProfile</span></span>
<span data-ttu-id="b2064-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2064-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2064-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="b2064-122">-DpsObject</span></span>
<span data-ttu-id="b2064-123">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="b2064-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="b2064-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="b2064-124">-IotHubConnectionString</span></span>
<span data-ttu-id="b2064-125">Verbindungszeichenfolge der viel Hub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b2064-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="b2064-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="b2064-126">-IotHubLocation</span></span>
<span data-ttu-id="b2064-127">Standort des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="b2064-127">Location of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2064-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b2064-128">-Name</span></span>
<span data-ttu-id="b2064-129">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="b2064-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b2064-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2064-130">-ResourceGroupName</span></span>
<span data-ttu-id="b2064-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b2064-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b2064-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b2064-132">-ResourceId</span></span>
<span data-ttu-id="b2064-133">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="b2064-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="b2064-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2064-134">-Confirm</span></span>
<span data-ttu-id="b2064-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2064-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2064-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2064-136">-WhatIf</span></span>
<span data-ttu-id="b2064-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2064-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2064-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2064-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2064-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2064-139">CommonParameters</span></span>
<span data-ttu-id="b2064-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2064-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2064-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2064-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2064-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2064-142">INPUTS</span></span>

### <span data-ttu-id="b2064-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="b2064-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="b2064-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b2064-144">System.String</span></span>

## <span data-ttu-id="b2064-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2064-145">OUTPUTS</span></span>

### <span data-ttu-id="b2064-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="b2064-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="b2064-147">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="b2064-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="b2064-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2064-148">NOTES</span></span>

## <span data-ttu-id="b2064-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2064-149">RELATED LINKS</span></span>
