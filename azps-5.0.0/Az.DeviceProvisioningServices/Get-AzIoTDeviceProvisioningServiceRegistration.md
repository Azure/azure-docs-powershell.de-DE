---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175720"
---
# <span data-ttu-id="8e523-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="8e523-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="8e523-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e523-102">SYNOPSIS</span></span>
<span data-ttu-id="8e523-103">Ruft den Geräte Registrierungsstatus ab.</span><span class="sxs-lookup"><span data-stu-id="8e523-103">Gets the device registration state.</span></span>

## <span data-ttu-id="8e523-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e523-104">SYNTAX</span></span>

### <span data-ttu-id="8e523-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e523-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e523-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8e523-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e523-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8e523-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e523-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e523-108">DESCRIPTION</span></span>
<span data-ttu-id="8e523-109">Rufen Sie den Geräte Registrierungsstatus oder den Registrierungsstatus von Geräten unter der Registrierungsstelle in einem Azure viel Hub-Device-Bereitstellungsdienst ab.</span><span class="sxs-lookup"><span data-stu-id="8e523-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="8e523-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e523-110">EXAMPLES</span></span>

### <span data-ttu-id="8e523-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e523-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="8e523-112">Rufen Sie die Details für den Geräte Registrierungsstatus in einem Azure viel Hub-Device-Bereitstellungsdienst ab.</span><span class="sxs-lookup"><span data-stu-id="8e523-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="8e523-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8e523-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="8e523-114">Listen Sie den gesamten Registrierungsstatus von Geräten in dieser Registrierungsliste auf.</span><span class="sxs-lookup"><span data-stu-id="8e523-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="8e523-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e523-115">PARAMETERS</span></span>

### <span data-ttu-id="8e523-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e523-116">-DefaultProfile</span></span>
<span data-ttu-id="8e523-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e523-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e523-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="8e523-118">-DpsName</span></span>
<span data-ttu-id="8e523-119">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="8e523-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8e523-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="8e523-120">-DpsObject</span></span>
<span data-ttu-id="8e523-121">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="8e523-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="8e523-122">-Registrierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="8e523-122">-EnrollmentId</span></span>
<span data-ttu-id="8e523-123">Die ID der Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8e523-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="8e523-124">-Query</span><span class="sxs-lookup"><span data-stu-id="8e523-124">-Query</span></span>
<span data-ttu-id="8e523-125">SQL-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="8e523-125">Sql query.</span></span>

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

### <span data-ttu-id="8e523-126">-Registrierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="8e523-126">-RegistrationId</span></span>
<span data-ttu-id="8e523-127">Die ID der Geräteregistrierung.</span><span class="sxs-lookup"><span data-stu-id="8e523-127">ID of device registration.</span></span>

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

### <span data-ttu-id="8e523-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e523-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e523-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8e523-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8e523-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8e523-130">-ResourceId</span></span>
<span data-ttu-id="8e523-131">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="8e523-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="8e523-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e523-132">CommonParameters</span></span>
<span data-ttu-id="8e523-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e523-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e523-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e523-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e523-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e523-135">INPUTS</span></span>

### <span data-ttu-id="8e523-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8e523-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="8e523-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8e523-137">System.String</span></span>

## <span data-ttu-id="8e523-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e523-138">OUTPUTS</span></span>

### <span data-ttu-id="8e523-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="8e523-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="8e523-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates []</span><span class="sxs-lookup"><span data-stu-id="8e523-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="8e523-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e523-141">NOTES</span></span>

## <span data-ttu-id="8e523-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e523-142">RELATED LINKS</span></span>
