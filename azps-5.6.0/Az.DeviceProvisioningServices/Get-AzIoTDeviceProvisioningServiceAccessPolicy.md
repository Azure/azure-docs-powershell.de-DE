---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 6fff4be5fb4d0c8b76643e215dfda6d2f3d34ab8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930515"
---
# <span data-ttu-id="0f4ba-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0f4ba-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="0f4ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f4ba-102">SYNOPSIS</span></span>
<span data-ttu-id="0f4ba-103">Listen Sie alle auf, oder zeigen Sie Details zu Richtlinien für den freigegebenen Zugriff in einem Azure IoT Hub-Gerätebereitstellungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="0f4ba-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0f4ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f4ba-104">SYNTAX</span></span>

### <span data-ttu-id="0f4ba-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f4ba-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f4ba-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0f4ba-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f4ba-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0f4ba-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f4ba-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f4ba-108">DESCRIPTION</span></span>
<span data-ttu-id="0f4ba-109">Eine Einführung in den Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0f4ba-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0f4ba-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f4ba-110">EXAMPLES</span></span>

### <span data-ttu-id="0f4ba-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f4ba-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="0f4ba-112">Listen Sie alle Richtlinien für den freigegebenen Zugriff in "myiotdps" auf.</span><span class="sxs-lookup"><span data-stu-id="0f4ba-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="0f4ba-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0f4ba-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="0f4ba-114">Zeigen Sie Details zur Richtlinie "mypolicy" für freigegebenen Zugriff in einem Azure IoT Hub-Gerätebereitstellungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="0f4ba-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0f4ba-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0f4ba-115">PARAMETERS</span></span>

### <span data-ttu-id="0f4ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f4ba-116">-DefaultProfile</span></span>
<span data-ttu-id="0f4ba-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f4ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f4ba-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="0f4ba-118">-DpsObject</span></span>
<span data-ttu-id="0f4ba-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="0f4ba-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0f4ba-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0f4ba-120">-KeyName</span></span>
<span data-ttu-id="0f4ba-121">Name des Zugriffsrichtlinienschlüssels des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="0f4ba-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="0f4ba-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0f4ba-122">-Name</span></span>
<span data-ttu-id="0f4ba-123">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="0f4ba-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0f4ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f4ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f4ba-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0f4ba-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0f4ba-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f4ba-126">-ResourceId</span></span>
<span data-ttu-id="0f4ba-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="0f4ba-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0f4ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f4ba-128">CommonParameters</span></span>
<span data-ttu-id="0f4ba-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f4ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f4ba-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f4ba-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f4ba-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f4ba-131">INPUTS</span></span>

### <span data-ttu-id="0f4ba-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0f4ba-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="0f4ba-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0f4ba-133">System.String</span></span>

## <span data-ttu-id="0f4ba-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f4ba-134">OUTPUTS</span></span>

### <span data-ttu-id="0f4ba-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="0f4ba-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="0f4ba-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0f4ba-136">NOTES</span></span>

## <span data-ttu-id="0f4ba-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0f4ba-137">RELATED LINKS</span></span>
