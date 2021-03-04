---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 05c275448ffecb006c8a23de36fcd7f33397af4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947859"
---
# <span data-ttu-id="79bf1-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="79bf1-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="79bf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="79bf1-103">Erstellen/Aktualisieren eines Azure IoT Hub Device Provisioning Service-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="79bf1-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="79bf1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79bf1-104">SYNTAX</span></span>

### <span data-ttu-id="79bf1-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="79bf1-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79bf1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="79bf1-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79bf1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="79bf1-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79bf1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79bf1-108">DESCRIPTION</span></span>
<span data-ttu-id="79bf1-109">Lädt ein neues Zertifikat hoch, oder ersetzen Sie das vorhandene Zertifikat durch denselben Namen.</span><span class="sxs-lookup"><span data-stu-id="79bf1-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="79bf1-110">Eine detaillierte Erläuterung der Zertifizierungsstellenzertifikate in Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="79bf1-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="79bf1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79bf1-111">EXAMPLES</span></span>

### <span data-ttu-id="79bf1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79bf1-112">Example 1</span></span>
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

<span data-ttu-id="79bf1-113">Laden Sie eine Zertifizierungsstellenzertifikat-CER-Datei in einen Azure IoT Hub-Gerätebereitstellungsdienst hoch.</span><span class="sxs-lookup"><span data-stu-id="79bf1-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="79bf1-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="79bf1-114">Example 2</span></span>
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

<span data-ttu-id="79bf1-115">Aktualisiert ein Zertifizierungsstellenzertifikat in einem IoT-Hub-Gerätebereitstellungsdienst, indem eine neue CER-Datei hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="79bf1-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="79bf1-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="79bf1-116">PARAMETERS</span></span>

### <span data-ttu-id="79bf1-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="79bf1-117">-CertificateName</span></span>
<span data-ttu-id="79bf1-118">Name des Iot-Gerätebereitstellungsdienstzertifikats</span><span class="sxs-lookup"><span data-stu-id="79bf1-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="79bf1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79bf1-119">-DefaultProfile</span></span>
<span data-ttu-id="79bf1-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79bf1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79bf1-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="79bf1-121">-Etag</span></span>
<span data-ttu-id="79bf1-122">Etag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="79bf1-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="79bf1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79bf1-123">-InputObject</span></span>
<span data-ttu-id="79bf1-124">IoT Device Provisioning Service Certificate Object</span><span class="sxs-lookup"><span data-stu-id="79bf1-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="79bf1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="79bf1-125">-Name</span></span>
<span data-ttu-id="79bf1-126">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="79bf1-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="79bf1-127">-Path</span><span class="sxs-lookup"><span data-stu-id="79bf1-127">-Path</span></span>
<span data-ttu-id="79bf1-128">Base-64-Darstellung der X509-Zertifikat-CER-Datei oder des PEM-Dateipfads</span><span class="sxs-lookup"><span data-stu-id="79bf1-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="79bf1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79bf1-129">-ResourceGroupName</span></span>
<span data-ttu-id="79bf1-130">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="79bf1-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="79bf1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79bf1-131">-ResourceId</span></span>
<span data-ttu-id="79bf1-132">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="79bf1-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="79bf1-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79bf1-133">-Confirm</span></span>
<span data-ttu-id="79bf1-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79bf1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79bf1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79bf1-135">-WhatIf</span></span>
<span data-ttu-id="79bf1-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79bf1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79bf1-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79bf1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79bf1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79bf1-138">CommonParameters</span></span>
<span data-ttu-id="79bf1-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79bf1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79bf1-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79bf1-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79bf1-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79bf1-141">INPUTS</span></span>

### <span data-ttu-id="79bf1-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="79bf1-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="79bf1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="79bf1-143">System.String</span></span>

## <span data-ttu-id="79bf1-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79bf1-144">OUTPUTS</span></span>

### <span data-ttu-id="79bf1-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="79bf1-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="79bf1-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="79bf1-146">NOTES</span></span>

## <span data-ttu-id="79bf1-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="79bf1-147">RELATED LINKS</span></span>
