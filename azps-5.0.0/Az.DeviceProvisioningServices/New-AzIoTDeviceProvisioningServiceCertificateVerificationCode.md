---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175713"
---
# <span data-ttu-id="7a9cf-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="7a9cf-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="7a9cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="7a9cf-103">Generieren Sie einen Bestätigungscode für ein Azure-Service-Bereitstellungszertifikat für Hub-Geräte.</span><span class="sxs-lookup"><span data-stu-id="7a9cf-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="7a9cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a9cf-104">SYNTAX</span></span>

### <span data-ttu-id="7a9cf-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a9cf-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a9cf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7a9cf-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a9cf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7a9cf-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a9cf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a9cf-108">DESCRIPTION</span></span>
<span data-ttu-id="7a9cf-109">Dieser Verifizierungscode wird verwendet, um den Beweis des Besitzes für ein Zertifikat abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7a9cf-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="7a9cf-110">Verwenden Sie diesen Verifizierungscode als CN eines neuen Zertifikats, das mit dem privaten Stammzertifikat-Schlüssel signiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7a9cf-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="7a9cf-111">Eine ausführliche Erläuterung der CA-Zertifikate im Azure-Service-Bereitstellungsdienst für Hub-Geräte finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="7a9cf-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="7a9cf-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a9cf-112">EXAMPLES</span></span>

### <span data-ttu-id="7a9cf-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7a9cf-113">Example 1</span></span>
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

<span data-ttu-id="7a9cf-114">Generieren Sie einen Bestätigungscode für "myCertificate".</span><span class="sxs-lookup"><span data-stu-id="7a9cf-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="7a9cf-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7a9cf-115">Example 2</span></span>
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

<span data-ttu-id="7a9cf-116">Generieren Sie einen Bestätigungscode für "myCertificate" mithilfe von Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7a9cf-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="7a9cf-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a9cf-117">PARAMETERS</span></span>

### <span data-ttu-id="7a9cf-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="7a9cf-118">-CertificateName</span></span>
<span data-ttu-id="7a9cf-119">Name des Dienstzertifikats "viel Geräte Bereitstellungsdienst"</span><span class="sxs-lookup"><span data-stu-id="7a9cf-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="7a9cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a9cf-120">-DefaultProfile</span></span>
<span data-ttu-id="7a9cf-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7a9cf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a9cf-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="7a9cf-122">-Etag</span></span>
<span data-ttu-id="7a9cf-123">ETag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="7a9cf-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="7a9cf-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7a9cf-124">-InputObject</span></span>
<span data-ttu-id="7a9cf-125">Viel Geräte Bereitstellungsdienst-Zertifikatobjekt</span><span class="sxs-lookup"><span data-stu-id="7a9cf-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="7a9cf-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7a9cf-126">-Name</span></span>
<span data-ttu-id="7a9cf-127">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="7a9cf-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7a9cf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a9cf-128">-ResourceGroupName</span></span>
<span data-ttu-id="7a9cf-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7a9cf-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7a9cf-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7a9cf-130">-ResourceId</span></span>
<span data-ttu-id="7a9cf-131">Dienstzertifikat-Ressourcen-ID für den Geräte Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="7a9cf-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="7a9cf-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7a9cf-132">-Confirm</span></span>
<span data-ttu-id="7a9cf-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a9cf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a9cf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a9cf-134">-WhatIf</span></span>
<span data-ttu-id="7a9cf-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a9cf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a9cf-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a9cf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a9cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a9cf-137">CommonParameters</span></span>
<span data-ttu-id="7a9cf-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a9cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a9cf-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a9cf-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a9cf-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a9cf-140">INPUTS</span></span>

### <span data-ttu-id="7a9cf-141">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="7a9cf-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="7a9cf-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7a9cf-142">System.String</span></span>

## <span data-ttu-id="7a9cf-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a9cf-143">OUTPUTS</span></span>

### <span data-ttu-id="7a9cf-144">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="7a9cf-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="7a9cf-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a9cf-145">NOTES</span></span>

## <span data-ttu-id="7a9cf-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a9cf-146">RELATED LINKS</span></span>
