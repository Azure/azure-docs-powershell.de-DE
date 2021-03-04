---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 999fa5d697feb8eab6edb83816763ed6cf49523c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945149"
---
# <span data-ttu-id="35a9e-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="35a9e-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="35a9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="35a9e-103">Generieren Sie einen Überprüfungscode für ein Azure IoT Hub Device Provisioning Service-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="35a9e-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="35a9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35a9e-104">SYNTAX</span></span>

### <span data-ttu-id="35a9e-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="35a9e-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35a9e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="35a9e-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35a9e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="35a9e-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35a9e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35a9e-108">DESCRIPTION</span></span>
<span data-ttu-id="35a9e-109">Dieser Überprüfungscode wird verwendet, um den Nachweis des Besitzes für ein Zertifikat zu vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="35a9e-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="35a9e-110">Verwenden Sie diesen Überprüfungscode als CN eines neuen Zertifikats, das mit dem privaten Schlüssel für Stammzertifikate signiert ist.</span><span class="sxs-lookup"><span data-stu-id="35a9e-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="35a9e-111">Eine detaillierte Erläuterung der Zertifizierungsstellenzertifikate in Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="35a9e-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="35a9e-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="35a9e-112">EXAMPLES</span></span>

### <span data-ttu-id="35a9e-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35a9e-113">Example 1</span></span>
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

<span data-ttu-id="35a9e-114">Generieren Sie einen Überprüfungscode für "mycertificate".</span><span class="sxs-lookup"><span data-stu-id="35a9e-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="35a9e-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="35a9e-115">Example 2</span></span>
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

<span data-ttu-id="35a9e-116">Generieren Sie mithilfe der Pipeline einen Überprüfungscode für "mycertificate".</span><span class="sxs-lookup"><span data-stu-id="35a9e-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="35a9e-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="35a9e-117">PARAMETERS</span></span>

### <span data-ttu-id="35a9e-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="35a9e-118">-CertificateName</span></span>
<span data-ttu-id="35a9e-119">Name des Iot-Gerätebereitstellungsdienstzertifikats</span><span class="sxs-lookup"><span data-stu-id="35a9e-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="35a9e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a9e-120">-DefaultProfile</span></span>
<span data-ttu-id="35a9e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35a9e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35a9e-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="35a9e-122">-Etag</span></span>
<span data-ttu-id="35a9e-123">Etag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="35a9e-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="35a9e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35a9e-124">-InputObject</span></span>
<span data-ttu-id="35a9e-125">IoT Device Provisioning Service Certificate Object</span><span class="sxs-lookup"><span data-stu-id="35a9e-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="35a9e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="35a9e-126">-Name</span></span>
<span data-ttu-id="35a9e-127">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="35a9e-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="35a9e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a9e-128">-ResourceGroupName</span></span>
<span data-ttu-id="35a9e-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="35a9e-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="35a9e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35a9e-130">-ResourceId</span></span>
<span data-ttu-id="35a9e-131">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="35a9e-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="35a9e-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="35a9e-132">-Confirm</span></span>
<span data-ttu-id="35a9e-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35a9e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35a9e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35a9e-134">-WhatIf</span></span>
<span data-ttu-id="35a9e-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35a9e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35a9e-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35a9e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35a9e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a9e-137">CommonParameters</span></span>
<span data-ttu-id="35a9e-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35a9e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a9e-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35a9e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a9e-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="35a9e-140">INPUTS</span></span>

### <span data-ttu-id="35a9e-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="35a9e-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="35a9e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="35a9e-142">System.String</span></span>

## <span data-ttu-id="35a9e-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="35a9e-143">OUTPUTS</span></span>

### <span data-ttu-id="35a9e-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="35a9e-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="35a9e-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="35a9e-145">NOTES</span></span>

## <span data-ttu-id="35a9e-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="35a9e-146">RELATED LINKS</span></span>
