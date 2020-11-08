---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: aa51001163e4559dd0d3ef7edfb48abd3448c0b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008504"
---
# <span data-ttu-id="e54fd-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="e54fd-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="e54fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e54fd-102">SYNOPSIS</span></span>
<span data-ttu-id="e54fd-103">Listet alle Zertifikate oder ein bestimmtes Zertifikat auf, das in einem Azure viel Hub-Device-Bereitstellungsdienst enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e54fd-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="e54fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e54fd-104">SYNTAX</span></span>

### <span data-ttu-id="e54fd-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e54fd-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e54fd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e54fd-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e54fd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e54fd-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e54fd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e54fd-108">DESCRIPTION</span></span>
<span data-ttu-id="e54fd-109">Eine ausführliche Erläuterung der CA-Zertifikate im Azure-Service-Bereitstellungsdienst für Hub-Geräte finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="e54fd-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="e54fd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e54fd-110">EXAMPLES</span></span>

### <span data-ttu-id="e54fd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e54fd-111">Example 1</span></span>
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

<span data-ttu-id="e54fd-112">Details zu "myCertificate" in einem Azure-viel-Hub-Device-Bereitstellungsdienst anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e54fd-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="e54fd-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e54fd-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="e54fd-114">Auflisten aller Zertifikate in "myiotdps" mithilfe von Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e54fd-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="e54fd-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e54fd-115">PARAMETERS</span></span>

### <span data-ttu-id="e54fd-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="e54fd-116">-CertificateName</span></span>
<span data-ttu-id="e54fd-117">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="e54fd-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="e54fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e54fd-118">-DefaultProfile</span></span>
<span data-ttu-id="e54fd-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e54fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e54fd-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="e54fd-120">-DpsObject</span></span>
<span data-ttu-id="e54fd-121">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="e54fd-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="e54fd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e54fd-122">-Name</span></span>
<span data-ttu-id="e54fd-123">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="e54fd-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e54fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e54fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="e54fd-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e54fd-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e54fd-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e54fd-126">-ResourceId</span></span>
<span data-ttu-id="e54fd-127">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="e54fd-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="e54fd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54fd-128">CommonParameters</span></span>
<span data-ttu-id="e54fd-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e54fd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54fd-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e54fd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54fd-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e54fd-131">INPUTS</span></span>

### <span data-ttu-id="e54fd-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="e54fd-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="e54fd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e54fd-133">System.String</span></span>

## <span data-ttu-id="e54fd-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e54fd-134">OUTPUTS</span></span>

### <span data-ttu-id="e54fd-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="e54fd-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="e54fd-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="e54fd-136">NOTES</span></span>

## <span data-ttu-id="e54fd-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e54fd-137">RELATED LINKS</span></span>
