---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ab6dd43cff746d670fe05d66d983836433323728
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997046"
---
# <span data-ttu-id="c5aa0-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="c5aa0-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="c5aa0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="c5aa0-103">Listen Sie alle auf, oder zeigen Sie die Details der Azure-Device-Bereitstellungsdienste an.</span><span class="sxs-lookup"><span data-stu-id="c5aa0-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="c5aa0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5aa0-104">SYNTAX</span></span>

### <span data-ttu-id="c5aa0-105">ListIotDpsByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5aa0-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5aa0-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="c5aa0-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5aa0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5aa0-107">DESCRIPTION</span></span>
<span data-ttu-id="c5aa0-108">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="c5aa0-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c5aa0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5aa0-109">EXAMPLES</span></span>

### <span data-ttu-id="c5aa0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c5aa0-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="c5aa0-111">Auflisten aller Azure-to-Hub-Device-Bereitstellungsdienste in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5aa0-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="c5aa0-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c5aa0-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="c5aa0-113">Auflisten aller Azure-to-Hub-Device-Bereitstellungsdienste in der Ressourcengruppe "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="c5aa0-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="c5aa0-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c5aa0-114">Example 3</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

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
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="c5aa0-115">Zeigen Sie Details zu einem Azure-viel-Hub-Device-Bereitstellungsdienst "myiotdps" an.</span><span class="sxs-lookup"><span data-stu-id="c5aa0-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="c5aa0-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5aa0-116">PARAMETERS</span></span>

### <span data-ttu-id="c5aa0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5aa0-117">-DefaultProfile</span></span>
<span data-ttu-id="c5aa0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5aa0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5aa0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c5aa0-119">-Name</span></span>
<span data-ttu-id="c5aa0-120">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="c5aa0-120">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5aa0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5aa0-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5aa0-122">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c5aa0-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotDpsByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5aa0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5aa0-123">CommonParameters</span></span>
<span data-ttu-id="c5aa0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5aa0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5aa0-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5aa0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5aa0-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5aa0-126">INPUTS</span></span>

### <span data-ttu-id="c5aa0-127">Keine</span><span class="sxs-lookup"><span data-stu-id="c5aa0-127">None</span></span>

## <span data-ttu-id="c5aa0-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5aa0-128">OUTPUTS</span></span>

### <span data-ttu-id="c5aa0-129">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c5aa0-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="c5aa0-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5aa0-130">NOTES</span></span>

## <span data-ttu-id="c5aa0-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5aa0-131">RELATED LINKS</span></span>
