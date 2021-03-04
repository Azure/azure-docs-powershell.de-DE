---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 56aadda2d7f1dccb77795d5226fb79c8a0fc65ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921976"
---
# <span data-ttu-id="fdd7b-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="fdd7b-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="fdd7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdd7b-102">SYNOPSIS</span></span>
<span data-ttu-id="fdd7b-103">Holen Sie sich einen Geräteregistrierungseintrag.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="fdd7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdd7b-104">SYNTAX</span></span>

### <span data-ttu-id="fdd7b-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fdd7b-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdd7b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fdd7b-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdd7b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fdd7b-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdd7b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdd7b-108">DESCRIPTION</span></span>
<span data-ttu-id="fdd7b-109">Erhalten Sie Geräteregistrierungsdetails oder Listen von Geräteregistrierungen in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="fdd7b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fdd7b-110">EXAMPLES</span></span>

### <span data-ttu-id="fdd7b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fdd7b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="fdd7b-112">Informationen zur Geräteregistrierung in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="fdd7b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fdd7b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="fdd7b-114">Listen Sie Geräteregistrierungen in einem Azure IoT Hub-Gerätebereitstellungsdienst auf.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="fdd7b-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fdd7b-115">PARAMETERS</span></span>

### <span data-ttu-id="fdd7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdd7b-116">-DefaultProfile</span></span>
<span data-ttu-id="fdd7b-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdd7b-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="fdd7b-118">-DpsName</span></span>
<span data-ttu-id="fdd7b-119">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="fdd7b-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="fdd7b-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="fdd7b-120">-DpsObject</span></span>
<span data-ttu-id="fdd7b-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="fdd7b-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="fdd7b-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="fdd7b-122">-RegistrationId</span></span>
<span data-ttu-id="fdd7b-123">Individuelle Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="fdd7b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdd7b-124">-ResourceGroupName</span></span>
<span data-ttu-id="fdd7b-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fdd7b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fdd7b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdd7b-126">-ResourceId</span></span>
<span data-ttu-id="fdd7b-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="fdd7b-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="fdd7b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdd7b-128">CommonParameters</span></span>
<span data-ttu-id="fdd7b-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdd7b-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdd7b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdd7b-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fdd7b-131">INPUTS</span></span>

### <span data-ttu-id="fdd7b-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="fdd7b-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="fdd7b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fdd7b-133">System.String</span></span>

## <span data-ttu-id="fdd7b-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fdd7b-134">OUTPUTS</span></span>

### <span data-ttu-id="fdd7b-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="fdd7b-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="fdd7b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span><span class="sxs-lookup"><span data-stu-id="fdd7b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="fdd7b-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fdd7b-137">NOTES</span></span>

## <span data-ttu-id="fdd7b-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fdd7b-138">RELATED LINKS</span></span>
