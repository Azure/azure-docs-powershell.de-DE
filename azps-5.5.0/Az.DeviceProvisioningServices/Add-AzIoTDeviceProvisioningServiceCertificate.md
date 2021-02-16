---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: d4dcf52a3a705042f994c8106bd931a8b704a049
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163657"
---
# <span data-ttu-id="c2abb-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="c2abb-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="c2abb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2abb-102">SYNOPSIS</span></span>
<span data-ttu-id="c2abb-103">Erstellen/aktualisieren Sie ein Azure IoT Hub Device Provisioning Service-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="c2abb-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="c2abb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2abb-104">SYNTAX</span></span>

### <span data-ttu-id="c2abb-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2abb-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2abb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c2abb-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2abb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c2abb-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2abb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2abb-108">DESCRIPTION</span></span>
<span data-ttu-id="c2abb-109">Lädt ein neues Zertifikat hoch, oder ersetzen Sie das vorhandene Zertifikat durch denselben Namen.</span><span class="sxs-lookup"><span data-stu-id="c2abb-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="c2abb-110">Eine ausführliche Erläuterung der Zertifizierungsstellenzertifikate im Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="c2abb-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="c2abb-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2abb-111">EXAMPLES</span></span>

### <span data-ttu-id="c2abb-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2abb-112">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

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

<span data-ttu-id="c2abb-113">Laden Sie eine ZERTIFIZIERUNGSSTELLENzertifikat-CER-Datei in einen Azure IoT Hub-Gerätebereitstellungsdienst hoch.</span><span class="sxs-lookup"><span data-stu-id="c2abb-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="c2abb-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c2abb-114">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="c2abb-115">Aktualisiert ein Zertifizierungsstellenzertifikat in einem Bereitstellungsdienst für IoT-Hub-Geräte, indem eine neue CER-Datei hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="c2abb-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="c2abb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2abb-116">PARAMETERS</span></span>

### <span data-ttu-id="c2abb-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c2abb-117">-CertificateName</span></span>
<span data-ttu-id="c2abb-118">Name des Zertifikats für den Bereitstellungsdienst für das Iot-Gerät</span><span class="sxs-lookup"><span data-stu-id="c2abb-118">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2abb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2abb-119">-DefaultProfile</span></span>
<span data-ttu-id="c2abb-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2abb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2abb-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="c2abb-121">-Etag</span></span>
<span data-ttu-id="c2abb-122">Etag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="c2abb-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="c2abb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2abb-123">-InputObject</span></span>
<span data-ttu-id="c2abb-124">IoT Device Provisioning Service Certificate Object</span><span class="sxs-lookup"><span data-stu-id="c2abb-124">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2abb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c2abb-125">-Name</span></span>
<span data-ttu-id="c2abb-126">Name des Bereitstellungsdiensts für IoT-Geräte</span><span class="sxs-lookup"><span data-stu-id="c2abb-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c2abb-127">-Path</span><span class="sxs-lookup"><span data-stu-id="c2abb-127">-Path</span></span>
<span data-ttu-id="c2abb-128">Base-64-Darstellung von X509-Zertifikat-CER-Datei oder PEM-Dateipfad</span><span class="sxs-lookup"><span data-stu-id="c2abb-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2abb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2abb-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2abb-130">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c2abb-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c2abb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2abb-131">-ResourceId</span></span>
<span data-ttu-id="c2abb-132">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="c2abb-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="c2abb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2abb-133">-Confirm</span></span>
<span data-ttu-id="c2abb-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2abb-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2abb-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c2abb-135">-WhatIf</span></span>
<span data-ttu-id="c2abb-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2abb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2abb-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2abb-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2abb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2abb-138">CommonParameters</span></span>
<span data-ttu-id="c2abb-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2abb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2abb-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2abb-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2abb-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2abb-141">INPUTS</span></span>

### <span data-ttu-id="c2abb-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="c2abb-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="c2abb-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c2abb-143">System.String</span></span>

## <span data-ttu-id="c2abb-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2abb-144">OUTPUTS</span></span>

### <span data-ttu-id="c2abb-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="c2abb-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="c2abb-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c2abb-146">NOTES</span></span>

## <span data-ttu-id="c2abb-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c2abb-147">RELATED LINKS</span></span>
