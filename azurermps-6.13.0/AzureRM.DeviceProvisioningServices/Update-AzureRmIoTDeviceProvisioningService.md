---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: 80032ab2a677683ff876aca499f7e0ee682e6fd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499525"
---
# <span data-ttu-id="0a1ae-101">Update-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="0a1ae-101">Update-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="0a1ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="0a1ae-103">Aktualisieren eines Azure viele-Hub-Device-Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="0a1ae-103">Update an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a1ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a1ae-104">SYNTAX</span></span>

### <span data-ttu-id="0a1ae-105">ResourceUpdateSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0a1ae-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a1ae-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0a1ae-106">InputObjectUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a1ae-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0a1ae-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a1ae-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0a1ae-108">ResourceIdUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a1ae-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0a1ae-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a1ae-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0a1ae-110">ResourceCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a1ae-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a1ae-111">DESCRIPTION</span></span>
<span data-ttu-id="0a1ae-112">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0a1ae-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0a1ae-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a1ae-113">EXAMPLES</span></span>

### <span data-ttu-id="0a1ae-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a1ae-114">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

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

<span data-ttu-id="0a1ae-115">Aktualisieren Sie die Zuordnungs Richtlinie auf "geolatenz" eines Azure viel Hub-Device-Bereitstellungs Diensts "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="0a1ae-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="0a1ae-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0a1ae-116">Example 2</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

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

<span data-ttu-id="0a1ae-117">Fügen Sie " @tags " zum Tag eines Azure-Service-Bereitstellungs Diensts "myiotdps" hinzu.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-117">Add "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="0a1ae-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0a1ae-118">Example 3</span></span>
```
PS C:\> Get-AzureRmIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzureRmIoTDps -Tag @tags -Reset

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

<span data-ttu-id="0a1ae-119">Löschen Sie das Tag, und fügen Sie @tags dem Tag eines azureely-Hub-Device-Bereitstellungs Diensts "myiotdps" mithilfe von Pipeline ein neues "" hinzu.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-119">Delete Tag and add new "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="0a1ae-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a1ae-120">PARAMETERS</span></span>

### <span data-ttu-id="0a1ae-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="0a1ae-121">-AllocationPolicy</span></span>
<span data-ttu-id="0a1ae-122">Dienst Zuweisungsrichtlinien für Geräte Bereitstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="0a1ae-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="0a1ae-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a1ae-123">-DefaultProfile</span></span>
<span data-ttu-id="0a1ae-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a1ae-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0a1ae-125">-InputObject</span></span>
<span data-ttu-id="0a1ae-126">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="0a1ae-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0a1ae-127">-Name</span><span class="sxs-lookup"><span data-stu-id="0a1ae-127">-Name</span></span>
<span data-ttu-id="0a1ae-128">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="0a1ae-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0a1ae-129">-Zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="0a1ae-129">-Reset</span></span>
<span data-ttu-id="0a1ae-130">Zurücksetzen von viel Geräte Bereitstellungs Service-Tags</span><span class="sxs-lookup"><span data-stu-id="0a1ae-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="0a1ae-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a1ae-131">-ResourceGroupName</span></span>
<span data-ttu-id="0a1ae-132">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0a1ae-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0a1ae-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0a1ae-133">-ResourceId</span></span>
<span data-ttu-id="0a1ae-134">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="0a1ae-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0a1ae-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a1ae-135">-Tag</span></span>
<span data-ttu-id="0a1ae-136">Service-Tag-Sammlung für Gerätebereitstellung</span><span class="sxs-lookup"><span data-stu-id="0a1ae-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="0a1ae-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0a1ae-137">-Confirm</span></span>
<span data-ttu-id="0a1ae-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a1ae-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a1ae-139">-WhatIf</span></span>
<span data-ttu-id="0a1ae-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a1ae-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a1ae-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a1ae-142">CommonParameters</span></span>
<span data-ttu-id="0a1ae-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a1ae-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a1ae-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a1ae-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a1ae-145">INPUTS</span></span>

### <span data-ttu-id="0a1ae-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0a1ae-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="0a1ae-147">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0a1ae-147">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0a1ae-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0a1ae-148">System.String</span></span>

## <span data-ttu-id="0a1ae-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a1ae-149">OUTPUTS</span></span>

### <span data-ttu-id="0a1ae-150">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0a1ae-150">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="0a1ae-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a1ae-151">NOTES</span></span>

## <span data-ttu-id="0a1ae-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a1ae-152">RELATED LINKS</span></span>
