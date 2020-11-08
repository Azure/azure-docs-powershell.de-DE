---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 411d4594c94fe1eb031f60d6abbff35f5060d4e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008498"
---
# <span data-ttu-id="a0a85-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="a0a85-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="a0a85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0a85-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a85-103">Aktualisieren eines Azure viele-Hub-Device-Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="a0a85-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="a0a85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0a85-104">SYNTAX</span></span>

### <span data-ttu-id="a0a85-105">ResourceUpdateSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0a85-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0a85-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="a0a85-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0a85-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="a0a85-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0a85-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="a0a85-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0a85-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="a0a85-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0a85-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="a0a85-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0a85-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0a85-111">DESCRIPTION</span></span>
<span data-ttu-id="a0a85-112">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="a0a85-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="a0a85-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0a85-113">EXAMPLES</span></span>

### <span data-ttu-id="a0a85-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0a85-114">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : GeoLatency
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="a0a85-115">Aktualisieren Sie die Zuordnungs Richtlinie auf "geolatenz" eines Azure viel Hub-Device-Bereitstellungs Diensts "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="a0a85-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="a0a85-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a0a85-116">Example 2</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="a0a85-117">Fügen Sie " @tags " zum Tag eines Azure-Service-Bereitstellungs Diensts "myiotdps" hinzu.</span><span class="sxs-lookup"><span data-stu-id="a0a85-117">Add "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="a0a85-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a0a85-118">Example 3</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag @tags -Reset

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAS1dY=
```

<span data-ttu-id="a0a85-119">Löschen Sie das Tag, und fügen Sie @tags dem Tag eines azureely-Hub-Device-Bereitstellungs Diensts "myiotdps" mithilfe von Pipeline ein neues "" hinzu.</span><span class="sxs-lookup"><span data-stu-id="a0a85-119">Delete Tag and add new "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="a0a85-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0a85-120">PARAMETERS</span></span>

### <span data-ttu-id="a0a85-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="a0a85-121">-AllocationPolicy</span></span>
<span data-ttu-id="a0a85-122">Dienst Zuweisungsrichtlinien für Geräte Bereitstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="a0a85-122">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectCreateUpdateSet, ResourceIdCreateUpdateSet, ResourceCreateUpdateSet
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a85-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a85-123">-DefaultProfile</span></span>
<span data-ttu-id="a0a85-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0a85-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0a85-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a0a85-125">-InputObject</span></span>
<span data-ttu-id="a0a85-126">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="a0a85-126">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectUpdateSet, InputObjectCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a85-127">-Name</span><span class="sxs-lookup"><span data-stu-id="a0a85-127">-Name</span></span>
<span data-ttu-id="a0a85-128">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="a0a85-128">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a85-129">-Zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="a0a85-129">-Reset</span></span>
<span data-ttu-id="a0a85-130">Zurücksetzen von viel Geräte Bereitstellungs Service-Tags</span><span class="sxs-lookup"><span data-stu-id="a0a85-130">Reset IoT Device Provisioning Service Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a85-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0a85-131">-ResourceGroupName</span></span>
<span data-ttu-id="a0a85-132">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a0a85-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a85-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a0a85-133">-ResourceId</span></span>
<span data-ttu-id="a0a85-134">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="a0a85-134">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdUpdateSet, ResourceIdCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a85-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0a85-135">-Tag</span></span>
<span data-ttu-id="a0a85-136">Service-Tag-Sammlung für Gerätebereitstellung</span><span class="sxs-lookup"><span data-stu-id="a0a85-136">IoT Device Provisioning Service Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a85-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0a85-137">-Confirm</span></span>
<span data-ttu-id="a0a85-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0a85-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0a85-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0a85-139">-WhatIf</span></span>
<span data-ttu-id="a0a85-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0a85-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0a85-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0a85-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0a85-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a85-142">CommonParameters</span></span>
<span data-ttu-id="a0a85-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0a85-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a85-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0a85-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a85-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0a85-145">INPUTS</span></span>

### <span data-ttu-id="a0a85-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a0a85-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="a0a85-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a0a85-147">System.String</span></span>

## <span data-ttu-id="a0a85-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0a85-148">OUTPUTS</span></span>

### <span data-ttu-id="a0a85-149">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a0a85-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="a0a85-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0a85-150">NOTES</span></span>

## <span data-ttu-id="a0a85-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0a85-151">RELATED LINKS</span></span>
