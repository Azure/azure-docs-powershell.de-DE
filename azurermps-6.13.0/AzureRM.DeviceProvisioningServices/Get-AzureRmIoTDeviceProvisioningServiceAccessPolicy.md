---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: e0685e82a4db2c786d4bb578544f6cbbd5dbadc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476089"
---
# <span data-ttu-id="105ac-101">Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="105ac-101">Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="105ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="105ac-102">SYNOPSIS</span></span>
<span data-ttu-id="105ac-103">Listen Sie alle auf, oder zeigen Sie Details zu den freigegebenen Zugriffsrichtlinien in einem Azure viel Hub-Device-Bereitstellungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="105ac-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="105ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="105ac-104">SYNTAX</span></span>

### <span data-ttu-id="105ac-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="105ac-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="105ac-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="105ac-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="105ac-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="105ac-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="105ac-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="105ac-108">DESCRIPTION</span></span>
<span data-ttu-id="105ac-109">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="105ac-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="105ac-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="105ac-110">EXAMPLES</span></span>

### <span data-ttu-id="105ac-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="105ac-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="105ac-112">Listen Sie alle freigegebenen Zugriffsrichtlinien in "myiotdps" auf.</span><span class="sxs-lookup"><span data-stu-id="105ac-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="105ac-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="105ac-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="105ac-114">Details zur gemeinsamen Zugriffsrichtlinie "MyPolicy" in einem Azure-viel-Hub-Device-Bereitstellungsdienst anzeigen.</span><span class="sxs-lookup"><span data-stu-id="105ac-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="105ac-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="105ac-115">PARAMETERS</span></span>

### <span data-ttu-id="105ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="105ac-116">-DefaultProfile</span></span>
<span data-ttu-id="105ac-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="105ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="105ac-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="105ac-118">-DpsObject</span></span>
<span data-ttu-id="105ac-119">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="105ac-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="105ac-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="105ac-120">-KeyName</span></span>
<span data-ttu-id="105ac-121">Dienstzugriffs Richtlinien-Schlüsselname für den Geräte Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="105ac-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="105ac-122">-Name</span><span class="sxs-lookup"><span data-stu-id="105ac-122">-Name</span></span>
<span data-ttu-id="105ac-123">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="105ac-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="105ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="105ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="105ac-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="105ac-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="105ac-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="105ac-126">-ResourceId</span></span>
<span data-ttu-id="105ac-127">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="105ac-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="105ac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="105ac-128">CommonParameters</span></span>
<span data-ttu-id="105ac-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="105ac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="105ac-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="105ac-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="105ac-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="105ac-131">INPUTS</span></span>

### <span data-ttu-id="105ac-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="105ac-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="105ac-133">Parameter: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="105ac-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="105ac-134">System. String</span><span class="sxs-lookup"><span data-stu-id="105ac-134">System.String</span></span>

## <span data-ttu-id="105ac-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="105ac-135">OUTPUTS</span></span>

### <span data-ttu-id="105ac-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="105ac-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="105ac-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="105ac-137">NOTES</span></span>

## <span data-ttu-id="105ac-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="105ac-138">RELATED LINKS</span></span>
