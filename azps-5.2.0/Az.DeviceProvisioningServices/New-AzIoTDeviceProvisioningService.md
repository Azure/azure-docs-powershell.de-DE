---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 482acd4f82320bbc14c5bf95c113304a8720019b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298408"
---
# <span data-ttu-id="fdb01-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="fdb01-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="fdb01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdb01-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb01-103">Erstellen Sie einen Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="fdb01-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="fdb01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdb01-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb01-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdb01-105">DESCRIPTION</span></span>
<span data-ttu-id="fdb01-106">Eine Einführung in den Bereitstellungsdienst für Azure IoT-Hub-Geräte finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="fdb01-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="fdb01-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fdb01-107">EXAMPLES</span></span>

### <span data-ttu-id="fdb01-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fdb01-108">Example 1</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {[key1, value1]}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="fdb01-109">Erstellen Sie einen Azure IoT Hub-Gerätebereitstellungsdienst mit der Standardpreisstufe S1 und Tags in der Region der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fdb01-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1 and tags, in the region of the resource group.</span></span>

### <span data-ttu-id="fdb01-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fdb01-110">Example 2</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : eastus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="fdb01-111">Erstellen Sie einen Azure IoT Hub-Gerätebereitstellungsdienst mit der Standardpreisstufe S1 in der Region "Ost".</span><span class="sxs-lookup"><span data-stu-id="fdb01-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="fdb01-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdb01-112">PARAMETERS</span></span>

### <span data-ttu-id="fdb01-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="fdb01-113">-AllocationPolicy</span></span>
<span data-ttu-id="fdb01-114">IoT Device Provisioning Service Allocation policy</span><span class="sxs-lookup"><span data-stu-id="fdb01-114">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb01-115">-DefaultProfile</span></span>
<span data-ttu-id="fdb01-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdb01-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdb01-117">-Location</span><span class="sxs-lookup"><span data-stu-id="fdb01-117">-Location</span></span>
<span data-ttu-id="fdb01-118">Position</span><span class="sxs-lookup"><span data-stu-id="fdb01-118">Location</span></span>

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

### <span data-ttu-id="fdb01-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fdb01-119">-Name</span></span>
<span data-ttu-id="fdb01-120">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="fdb01-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="fdb01-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb01-121">-ResourceGroupName</span></span>
<span data-ttu-id="fdb01-122">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fdb01-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb01-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fdb01-123">-SkuName</span></span>
<span data-ttu-id="fdb01-124">SKU</span><span class="sxs-lookup"><span data-stu-id="fdb01-124">Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb01-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="fdb01-125">-Tag</span></span>
<span data-ttu-id="fdb01-126">IoT Device Provisioning Service-Instanztags.</span><span class="sxs-lookup"><span data-stu-id="fdb01-126">IoT Device Provisioning Service instance tags.</span></span> <span data-ttu-id="fdb01-127">Eigenschaftentasche in Schlüssel-Wert-Paaren in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="fdb01-127">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb01-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdb01-128">-Confirm</span></span>
<span data-ttu-id="fdb01-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fdb01-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdb01-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fdb01-130">-WhatIf</span></span>
<span data-ttu-id="fdb01-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fdb01-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdb01-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fdb01-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdb01-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb01-133">CommonParameters</span></span>
<span data-ttu-id="fdb01-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb01-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb01-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb01-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb01-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fdb01-136">INPUTS</span></span>

### <span data-ttu-id="fdb01-137">Keine</span><span class="sxs-lookup"><span data-stu-id="fdb01-137">None</span></span>

## <span data-ttu-id="fdb01-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fdb01-138">OUTPUTS</span></span>

### <span data-ttu-id="fdb01-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="fdb01-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="fdb01-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fdb01-140">NOTES</span></span>

## <span data-ttu-id="fdb01-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fdb01-141">RELATED LINKS</span></span>
