---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153241"
---
# <span data-ttu-id="d2839-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="d2839-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="d2839-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2839-102">SYNOPSIS</span></span>
<span data-ttu-id="d2839-103">Ruft den Geräteregistrierungsstatus ab.</span><span class="sxs-lookup"><span data-stu-id="d2839-103">Gets the device registration state.</span></span>

## <span data-ttu-id="d2839-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2839-104">SYNTAX</span></span>

### <span data-ttu-id="d2839-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2839-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2839-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d2839-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2839-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d2839-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2839-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2839-108">DESCRIPTION</span></span>
<span data-ttu-id="d2839-109">Holen Sie sich den Geräteregistrierungsstatus oder den Registrierungsstatus von Geräten unter der Registrierungsgruppe in einem Azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="d2839-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="d2839-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d2839-110">EXAMPLES</span></span>

### <span data-ttu-id="d2839-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d2839-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="d2839-112">Informationen zum Geräteregistrierungsstatus finden Sie in einem Azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="d2839-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="d2839-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d2839-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="d2839-114">Listen Sie alle Registrierungsstatus von Geräten in dieser Registrierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="d2839-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="d2839-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2839-115">PARAMETERS</span></span>

### <span data-ttu-id="d2839-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2839-116">-DefaultProfile</span></span>
<span data-ttu-id="d2839-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2839-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2839-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="d2839-118">-DpsName</span></span>
<span data-ttu-id="d2839-119">Name des Bereitstellungsdiensts für IoT-Geräte</span><span class="sxs-lookup"><span data-stu-id="d2839-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d2839-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="d2839-120">-DpsObject</span></span>
<span data-ttu-id="d2839-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="d2839-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d2839-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="d2839-122">-EnrollmentId</span></span>
<span data-ttu-id="d2839-123">ID der Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d2839-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="d2839-124">-Query</span><span class="sxs-lookup"><span data-stu-id="d2839-124">-Query</span></span>
<span data-ttu-id="d2839-125">"Sql-Abfrage" aus.</span><span class="sxs-lookup"><span data-stu-id="d2839-125">Sql query.</span></span>

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

### <span data-ttu-id="d2839-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="d2839-126">-RegistrationId</span></span>
<span data-ttu-id="d2839-127">ID der Geräteregistrierung.</span><span class="sxs-lookup"><span data-stu-id="d2839-127">ID of device registration.</span></span>

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

### <span data-ttu-id="d2839-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2839-128">-ResourceGroupName</span></span>
<span data-ttu-id="d2839-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d2839-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d2839-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2839-130">-ResourceId</span></span>
<span data-ttu-id="d2839-131">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="d2839-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d2839-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2839-132">CommonParameters</span></span>
<span data-ttu-id="d2839-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2839-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2839-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2839-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2839-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d2839-135">INPUTS</span></span>

### <span data-ttu-id="d2839-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d2839-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d2839-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d2839-137">System.String</span></span>

## <span data-ttu-id="d2839-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d2839-138">OUTPUTS</span></span>

### <span data-ttu-id="d2839-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="d2839-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="d2839-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span><span class="sxs-lookup"><span data-stu-id="d2839-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="d2839-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d2839-141">NOTES</span></span>

## <span data-ttu-id="d2839-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d2839-142">RELATED LINKS</span></span>
