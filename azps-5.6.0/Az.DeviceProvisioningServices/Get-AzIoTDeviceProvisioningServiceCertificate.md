---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 788759abe543d3bddf3c67abe2ed37aafca6be3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931888"
---
# <span data-ttu-id="59d41-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="59d41-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="59d41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59d41-102">SYNOPSIS</span></span>
<span data-ttu-id="59d41-103">Listet alle Zertifikate oder ein bestimmtes Zertifikat auf, die in einem Azure IoT Hub Device Provisioning Service enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="59d41-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="59d41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59d41-104">SYNTAX</span></span>

### <span data-ttu-id="59d41-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="59d41-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59d41-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="59d41-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59d41-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="59d41-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59d41-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59d41-108">DESCRIPTION</span></span>
<span data-ttu-id="59d41-109">Eine detaillierte Erläuterung der Zertifizierungsstellenzertifikate in Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="59d41-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="59d41-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59d41-110">EXAMPLES</span></span>

### <span data-ttu-id="59d41-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59d41-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="59d41-112">Zeigen Sie Details zu "mycertificate" in einem Azure IoT Hub-Gerätebereitstellungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="59d41-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="59d41-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="59d41-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="59d41-114">Listen Sie alle Zertifikate in "myiotdps" mithilfe der Pipeline auf.</span><span class="sxs-lookup"><span data-stu-id="59d41-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="59d41-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="59d41-115">PARAMETERS</span></span>

### <span data-ttu-id="59d41-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="59d41-116">-CertificateName</span></span>
<span data-ttu-id="59d41-117">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="59d41-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="59d41-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d41-118">-DefaultProfile</span></span>
<span data-ttu-id="59d41-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59d41-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59d41-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="59d41-120">-DpsObject</span></span>
<span data-ttu-id="59d41-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="59d41-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="59d41-122">-Name</span><span class="sxs-lookup"><span data-stu-id="59d41-122">-Name</span></span>
<span data-ttu-id="59d41-123">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="59d41-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="59d41-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d41-124">-ResourceGroupName</span></span>
<span data-ttu-id="59d41-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="59d41-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="59d41-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59d41-126">-ResourceId</span></span>
<span data-ttu-id="59d41-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="59d41-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="59d41-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d41-128">CommonParameters</span></span>
<span data-ttu-id="59d41-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59d41-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d41-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d41-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d41-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59d41-131">INPUTS</span></span>

### <span data-ttu-id="59d41-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="59d41-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="59d41-133">System.String</span><span class="sxs-lookup"><span data-stu-id="59d41-133">System.String</span></span>

## <span data-ttu-id="59d41-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59d41-134">OUTPUTS</span></span>

### <span data-ttu-id="59d41-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="59d41-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="59d41-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="59d41-136">NOTES</span></span>

## <span data-ttu-id="59d41-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="59d41-137">RELATED LINKS</span></span>
