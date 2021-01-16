---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 87c6bdd72229baec8e65c40d4e2e4309bde59aba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292199"
---
# <span data-ttu-id="44636-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="44636-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="44636-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44636-102">SYNOPSIS</span></span>
<span data-ttu-id="44636-103">Hier erfahren Sie, wie Sie alle Richtlinien für den freigegebenen Zugriff in einem Azure IoT Hub-Gerätebereitstellungsdienst auflisten oder Details anzeigen.</span><span class="sxs-lookup"><span data-stu-id="44636-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="44636-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44636-104">SYNTAX</span></span>

### <span data-ttu-id="44636-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="44636-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44636-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="44636-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44636-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="44636-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44636-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44636-108">DESCRIPTION</span></span>
<span data-ttu-id="44636-109">Eine Einführung in den Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="44636-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="44636-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="44636-110">EXAMPLES</span></span>

### <span data-ttu-id="44636-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="44636-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="44636-112">Listen Sie alle Richtlinien für freigegebenen Zugriff in "myiotdps" auf.</span><span class="sxs-lookup"><span data-stu-id="44636-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="44636-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="44636-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="44636-114">Zeigen Sie Details der Richtlinie für freigegebenen Zugriff "mypolicy" in einem Azure IoT Hub-Gerätebereitstellungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="44636-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="44636-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44636-115">PARAMETERS</span></span>

### <span data-ttu-id="44636-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44636-116">-DefaultProfile</span></span>
<span data-ttu-id="44636-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44636-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44636-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="44636-118">-DpsObject</span></span>
<span data-ttu-id="44636-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="44636-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="44636-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="44636-120">-KeyName</span></span>
<span data-ttu-id="44636-121">Name der Zugriffsrichtlinie für die IoT-Gerätebereitstellungsdienst-Zugriffsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="44636-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="44636-122">-Name</span><span class="sxs-lookup"><span data-stu-id="44636-122">-Name</span></span>
<span data-ttu-id="44636-123">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="44636-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="44636-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44636-124">-ResourceGroupName</span></span>
<span data-ttu-id="44636-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="44636-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="44636-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44636-126">-ResourceId</span></span>
<span data-ttu-id="44636-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="44636-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="44636-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44636-128">CommonParameters</span></span>
<span data-ttu-id="44636-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44636-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44636-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44636-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44636-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="44636-131">INPUTS</span></span>

### <span data-ttu-id="44636-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="44636-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="44636-133">System.String</span><span class="sxs-lookup"><span data-stu-id="44636-133">System.String</span></span>

## <span data-ttu-id="44636-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="44636-134">OUTPUTS</span></span>

### <span data-ttu-id="44636-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="44636-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="44636-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="44636-136">NOTES</span></span>

## <span data-ttu-id="44636-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="44636-137">RELATED LINKS</span></span>
