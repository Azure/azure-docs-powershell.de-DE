---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 1678202d02f25ea8ffa2ed14a859aaf5965776b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935219"
---
# <span data-ttu-id="628c5-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="628c5-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="628c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="628c5-102">SYNOPSIS</span></span>
<span data-ttu-id="628c5-103">Überprüfen Sie ein Azure IoT Hub Device Provisioning Service-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="628c5-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="628c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="628c5-104">SYNTAX</span></span>

### <span data-ttu-id="628c5-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="628c5-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="628c5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="628c5-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="628c5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="628c5-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="628c5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="628c5-108">DESCRIPTION</span></span>
<span data-ttu-id="628c5-109">Überprüfen Sie ein Zertifikat, indem Sie ein Überprüfungszertifikat hochladen, das den Überprüfungscode enthält, der durch Aufrufen von generate-verification-code ermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="628c5-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="628c5-110">Dies ist der letzte Schritt im Beweisbesitzprozess.</span><span class="sxs-lookup"><span data-stu-id="628c5-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="628c5-111">Eine detaillierte Erläuterung der Zertifizierungsstellenzertifikate in Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="628c5-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="628c5-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="628c5-112">EXAMPLES</span></span>

### <span data-ttu-id="628c5-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="628c5-113">Example 1</span></span>
```
PS C:\> Set-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="628c5-114">Überprüfen Sie den Besitz des privaten Schlüssels "mycertificate".</span><span class="sxs-lookup"><span data-stu-id="628c5-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="628c5-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="628c5-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | Set-AzIoTDpsCertificate -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="628c5-116">Überprüfen Sie den Besitz des privaten Schlüssels "mycertificate" mithilfe der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="628c5-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="628c5-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="628c5-117">PARAMETERS</span></span>

### <span data-ttu-id="628c5-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="628c5-118">-CertificateName</span></span>
<span data-ttu-id="628c5-119">Name des Iot-Gerätebereitstellungsdienstzertifikats</span><span class="sxs-lookup"><span data-stu-id="628c5-119">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="628c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="628c5-120">-DefaultProfile</span></span>
<span data-ttu-id="628c5-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="628c5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="628c5-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="628c5-122">-Etag</span></span>
<span data-ttu-id="628c5-123">Etag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="628c5-123">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="628c5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="628c5-124">-InputObject</span></span>
<span data-ttu-id="628c5-125">IoT Device Provisioning Service Certificate Object</span><span class="sxs-lookup"><span data-stu-id="628c5-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="628c5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="628c5-126">-Name</span></span>
<span data-ttu-id="628c5-127">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="628c5-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="628c5-128">-Path</span><span class="sxs-lookup"><span data-stu-id="628c5-128">-Path</span></span>
<span data-ttu-id="628c5-129">Base-64-Darstellung der X509-Zertifikat-CER-Datei oder des PEM-Dateipfads</span><span class="sxs-lookup"><span data-stu-id="628c5-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="628c5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="628c5-130">-ResourceGroupName</span></span>
<span data-ttu-id="628c5-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="628c5-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="628c5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="628c5-132">-ResourceId</span></span>
<span data-ttu-id="628c5-133">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="628c5-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="628c5-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="628c5-134">-Confirm</span></span>
<span data-ttu-id="628c5-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="628c5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="628c5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="628c5-136">-WhatIf</span></span>
<span data-ttu-id="628c5-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="628c5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="628c5-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="628c5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="628c5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="628c5-139">CommonParameters</span></span>
<span data-ttu-id="628c5-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="628c5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="628c5-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="628c5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="628c5-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="628c5-142">INPUTS</span></span>

### <span data-ttu-id="628c5-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="628c5-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="628c5-144">System.String</span><span class="sxs-lookup"><span data-stu-id="628c5-144">System.String</span></span>

## <span data-ttu-id="628c5-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="628c5-145">OUTPUTS</span></span>

### <span data-ttu-id="628c5-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="628c5-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="628c5-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="628c5-147">NOTES</span></span>

## <span data-ttu-id="628c5-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="628c5-148">RELATED LINKS</span></span>
