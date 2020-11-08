---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175723"
---
# <span data-ttu-id="fefa8-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="fefa8-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="fefa8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fefa8-102">SYNOPSIS</span></span>
<span data-ttu-id="fefa8-103">Abrufen eines Geräte Registrierungseintrags</span><span class="sxs-lookup"><span data-stu-id="fefa8-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="fefa8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fefa8-104">SYNTAX</span></span>

### <span data-ttu-id="fefa8-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fefa8-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fefa8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fefa8-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fefa8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fefa8-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fefa8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fefa8-108">DESCRIPTION</span></span>
<span data-ttu-id="fefa8-109">Abrufen von Details zur Geräteregistrierung oder Auflisten von Geräte Einschreibungen in einem Azure-viel-Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="fefa8-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="fefa8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fefa8-110">EXAMPLES</span></span>

### <span data-ttu-id="fefa8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fefa8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="fefa8-112">Abrufen von Details zur Geräteregistrierung in einem Azure viel-Bereitstellungsdienst für Hub-Geräte.</span><span class="sxs-lookup"><span data-stu-id="fefa8-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="fefa8-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fefa8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="fefa8-114">Auflisten von Geräte Einschreibungen in einem Azure-viel-Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="fefa8-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="fefa8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="fefa8-115">PARAMETERS</span></span>

### <span data-ttu-id="fefa8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fefa8-116">-DefaultProfile</span></span>
<span data-ttu-id="fefa8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fefa8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fefa8-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="fefa8-118">-DpsName</span></span>
<span data-ttu-id="fefa8-119">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="fefa8-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="fefa8-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="fefa8-120">-DpsObject</span></span>
<span data-ttu-id="fefa8-121">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="fefa8-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="fefa8-122">-Registrierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="fefa8-122">-RegistrationId</span></span>
<span data-ttu-id="fefa8-123">Individuelle Registrierungs-ID für die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="fefa8-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="fefa8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fefa8-124">-ResourceGroupName</span></span>
<span data-ttu-id="fefa8-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fefa8-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fefa8-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fefa8-126">-ResourceId</span></span>
<span data-ttu-id="fefa8-127">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="fefa8-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="fefa8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fefa8-128">CommonParameters</span></span>
<span data-ttu-id="fefa8-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fefa8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fefa8-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fefa8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fefa8-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fefa8-131">INPUTS</span></span>

### <span data-ttu-id="fefa8-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="fefa8-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="fefa8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fefa8-133">System.String</span></span>

## <span data-ttu-id="fefa8-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fefa8-134">OUTPUTS</span></span>

### <span data-ttu-id="fefa8-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="fefa8-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="fefa8-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollments []</span><span class="sxs-lookup"><span data-stu-id="fefa8-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="fefa8-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="fefa8-137">NOTES</span></span>

## <span data-ttu-id="fefa8-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fefa8-138">RELATED LINKS</span></span>
