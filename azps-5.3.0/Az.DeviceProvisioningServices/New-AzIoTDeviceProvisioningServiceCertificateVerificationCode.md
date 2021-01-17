---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467784"
---
# <span data-ttu-id="076ac-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="076ac-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="076ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="076ac-102">SYNOPSIS</span></span>
<span data-ttu-id="076ac-103">Generieren Sie einen Überprüfungscode für ein Azure IoT Hub Device Provisioning Service-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="076ac-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="076ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="076ac-104">SYNTAX</span></span>

### <span data-ttu-id="076ac-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="076ac-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="076ac-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="076ac-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="076ac-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="076ac-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="076ac-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="076ac-108">DESCRIPTION</span></span>
<span data-ttu-id="076ac-109">Dieser Überprüfungscode wird verwendet, um den Schritt zum Nachweis des Besitzes für ein Zertifikat zu vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="076ac-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="076ac-110">Verwenden Sie diesen Überprüfungscode als CN eines neuen Zertifikats, das mit dem privaten Schlüssel für Stammzertifikate signiert ist.</span><span class="sxs-lookup"><span data-stu-id="076ac-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="076ac-111">Eine ausführliche Erläuterung der Zertifizierungsstellenzertifikate im Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="076ac-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="076ac-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="076ac-112">EXAMPLES</span></span>

### <span data-ttu-id="076ac-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="076ac-113">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="076ac-114">Generieren Sie einen Prüfcode für "mycertificate".</span><span class="sxs-lookup"><span data-stu-id="076ac-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="076ac-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="076ac-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzIoTDpsCVC

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="076ac-116">Generieren Sie mithilfe der Pipeline einen Überprüfungscode für "mycertificate".</span><span class="sxs-lookup"><span data-stu-id="076ac-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="076ac-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="076ac-117">PARAMETERS</span></span>

### <span data-ttu-id="076ac-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="076ac-118">-CertificateName</span></span>
<span data-ttu-id="076ac-119">Name des Zertifikats für den Bereitstellungsdienst für das Iot-Gerät</span><span class="sxs-lookup"><span data-stu-id="076ac-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="076ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="076ac-120">-DefaultProfile</span></span>
<span data-ttu-id="076ac-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="076ac-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="076ac-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="076ac-122">-Etag</span></span>
<span data-ttu-id="076ac-123">Etag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="076ac-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="076ac-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="076ac-124">-InputObject</span></span>
<span data-ttu-id="076ac-125">IoT Device Provisioning Service Certificate Object</span><span class="sxs-lookup"><span data-stu-id="076ac-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="076ac-126">-Name</span><span class="sxs-lookup"><span data-stu-id="076ac-126">-Name</span></span>
<span data-ttu-id="076ac-127">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="076ac-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="076ac-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="076ac-128">-ResourceGroupName</span></span>
<span data-ttu-id="076ac-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="076ac-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="076ac-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="076ac-130">-ResourceId</span></span>
<span data-ttu-id="076ac-131">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="076ac-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="076ac-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="076ac-132">-Confirm</span></span>
<span data-ttu-id="076ac-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="076ac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="076ac-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="076ac-134">-WhatIf</span></span>
<span data-ttu-id="076ac-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="076ac-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="076ac-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="076ac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="076ac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="076ac-137">CommonParameters</span></span>
<span data-ttu-id="076ac-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="076ac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="076ac-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="076ac-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="076ac-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="076ac-140">INPUTS</span></span>

### <span data-ttu-id="076ac-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="076ac-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="076ac-142">System.String</span><span class="sxs-lookup"><span data-stu-id="076ac-142">System.String</span></span>

## <span data-ttu-id="076ac-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="076ac-143">OUTPUTS</span></span>

### <span data-ttu-id="076ac-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="076ac-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="076ac-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="076ac-145">NOTES</span></span>

## <span data-ttu-id="076ac-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="076ac-146">RELATED LINKS</span></span>
