---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ac9d9423bf0098f0f6cf7abba958eb2b08404778
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661129"
---
# <span data-ttu-id="999f3-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="999f3-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="999f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="999f3-102">SYNOPSIS</span></span>
<span data-ttu-id="999f3-103">Erstellen Sie einen Azure-viel-Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="999f3-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="999f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="999f3-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="999f3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="999f3-105">DESCRIPTION</span></span>
<span data-ttu-id="999f3-106">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="999f3-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="999f3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="999f3-107">EXAMPLES</span></span>

### <span data-ttu-id="999f3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="999f3-108">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="999f3-109">Erstellen Sie einen Azure-to-Hub-Device-Bereitstellungsdienst mit der Standardpreis Stufe S1 im Bereich der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="999f3-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="999f3-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="999f3-110">Example 2</span></span>
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

<span data-ttu-id="999f3-111">Erstellen Sie einen Azure-to-Hub-Device-Bereitstellungsdienst mit der standardmäßigen Preisstufe S1 in der Region "eastus".</span><span class="sxs-lookup"><span data-stu-id="999f3-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="999f3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="999f3-112">PARAMETERS</span></span>

### <span data-ttu-id="999f3-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="999f3-113">-AllocationPolicy</span></span>
<span data-ttu-id="999f3-114">Dienst Zuweisungsrichtlinien für Geräte Bereitstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="999f3-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="999f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="999f3-115">-DefaultProfile</span></span>
<span data-ttu-id="999f3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="999f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="999f3-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="999f3-117">-Location</span></span>
<span data-ttu-id="999f3-118">Lage</span><span class="sxs-lookup"><span data-stu-id="999f3-118">Location</span></span>

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

### <span data-ttu-id="999f3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="999f3-119">-Name</span></span>
<span data-ttu-id="999f3-120">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="999f3-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="999f3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="999f3-121">-ResourceGroupName</span></span>
<span data-ttu-id="999f3-122">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="999f3-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="999f3-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="999f3-123">-SkuName</span></span>
<span data-ttu-id="999f3-124">SKU</span><span class="sxs-lookup"><span data-stu-id="999f3-124">Sku</span></span>

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

### <span data-ttu-id="999f3-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="999f3-125">-Confirm</span></span>
<span data-ttu-id="999f3-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="999f3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="999f3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="999f3-127">-WhatIf</span></span>
<span data-ttu-id="999f3-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="999f3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="999f3-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="999f3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="999f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="999f3-130">CommonParameters</span></span>
<span data-ttu-id="999f3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="999f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="999f3-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="999f3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="999f3-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="999f3-133">INPUTS</span></span>

### <span data-ttu-id="999f3-134">Keine</span><span class="sxs-lookup"><span data-stu-id="999f3-134">None</span></span>

## <span data-ttu-id="999f3-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="999f3-135">OUTPUTS</span></span>

### <span data-ttu-id="999f3-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="999f3-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="999f3-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="999f3-137">NOTES</span></span>

## <span data-ttu-id="999f3-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="999f3-138">RELATED LINKS</span></span>
