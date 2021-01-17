---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467811"
---
# <span data-ttu-id="a6269-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="a6269-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="a6269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6269-102">SYNOPSIS</span></span>
<span data-ttu-id="a6269-103">Holen Sie sich eine Geräteregistrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a6269-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="a6269-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6269-104">SYNTAX</span></span>

### <span data-ttu-id="a6269-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6269-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6269-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a6269-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6269-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a6269-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6269-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6269-108">DESCRIPTION</span></span>
<span data-ttu-id="a6269-109">Erhalten Sie die Details einer Registrierungsgruppe, oder listen Sie alle Registrierungsgruppen in einem Azure IoT Hub Device Provisioning Service auf.</span><span class="sxs-lookup"><span data-stu-id="a6269-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="a6269-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a6269-110">EXAMPLES</span></span>

### <span data-ttu-id="a6269-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6269-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="a6269-112">Holen Sie sich die Geräteregistrierungsgruppe in einem Azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="a6269-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="a6269-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a6269-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="a6269-114">Listen Sie alle Geräteregistrierungsgruppen in einem Azure IoT Hub Device Provisioning Service auf.</span><span class="sxs-lookup"><span data-stu-id="a6269-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="a6269-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6269-115">PARAMETERS</span></span>

### <span data-ttu-id="a6269-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6269-116">-DefaultProfile</span></span>
<span data-ttu-id="a6269-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6269-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6269-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="a6269-118">-DpsName</span></span>
<span data-ttu-id="a6269-119">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="a6269-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a6269-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="a6269-120">-DpsObject</span></span>
<span data-ttu-id="a6269-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="a6269-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="a6269-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a6269-122">-Name</span></span>
<span data-ttu-id="a6269-123">Der Name der Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a6269-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="a6269-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6269-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6269-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a6269-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a6269-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6269-126">-ResourceId</span></span>
<span data-ttu-id="a6269-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="a6269-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a6269-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6269-128">CommonParameters</span></span>
<span data-ttu-id="a6269-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6269-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6269-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6269-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6269-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a6269-131">INPUTS</span></span>

### <span data-ttu-id="a6269-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a6269-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="a6269-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a6269-133">System.String</span></span>

## <span data-ttu-id="a6269-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a6269-134">OUTPUTS</span></span>

### <span data-ttu-id="a6269-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="a6269-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="a6269-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span><span class="sxs-lookup"><span data-stu-id="a6269-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="a6269-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a6269-137">NOTES</span></span>

## <span data-ttu-id="a6269-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a6269-138">RELATED LINKS</span></span>
