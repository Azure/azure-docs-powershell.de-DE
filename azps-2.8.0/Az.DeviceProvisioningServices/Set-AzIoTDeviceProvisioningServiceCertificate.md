---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 659998a6a82c08ab57697767276e2357002a4182
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651275"
---
# <span data-ttu-id="b9175-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="b9175-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="b9175-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9175-102">SYNOPSIS</span></span>
<span data-ttu-id="b9175-103">Überprüfen eines Azure-to-Service-Zertifikats für Hub-Device-Bereitstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="b9175-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="b9175-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9175-104">SYNTAX</span></span>

### <span data-ttu-id="b9175-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9175-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9175-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b9175-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9175-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b9175-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9175-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9175-108">DESCRIPTION</span></span>
<span data-ttu-id="b9175-109">Überprüfen Sie ein Zertifikat, indem Sie ein Verifizierungszertifikat hochladen, das den Bestätigungscode enthält, der durch Aufrufen von generieren-Verification-Code abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b9175-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="b9175-110">Dies ist der letzte Schritt beim Nachweis des Besitz Prozesses.</span><span class="sxs-lookup"><span data-stu-id="b9175-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="b9175-111">Eine ausführliche Erläuterung der CA-Zertifikate im Azure-Service-Bereitstellungsdienst für Hub-Geräte finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="b9175-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="b9175-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9175-112">EXAMPLES</span></span>

### <span data-ttu-id="b9175-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9175-113">Example 1</span></span>
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

<span data-ttu-id="b9175-114">Überprüfen Sie den Besitz des privaten Schlüssels "mein Zertifikat".</span><span class="sxs-lookup"><span data-stu-id="b9175-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="b9175-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b9175-115">Example 2</span></span>
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

<span data-ttu-id="b9175-116">Überprüfen Sie den Besitz des privaten Schlüssels "myCertificate" mithilfe von Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b9175-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="b9175-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9175-117">PARAMETERS</span></span>

### <span data-ttu-id="b9175-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b9175-118">-CertificateName</span></span>
<span data-ttu-id="b9175-119">Name des Dienstzertifikats "viel Geräte Bereitstellungsdienst"</span><span class="sxs-lookup"><span data-stu-id="b9175-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="b9175-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9175-120">-DefaultProfile</span></span>
<span data-ttu-id="b9175-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9175-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9175-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="b9175-122">-Etag</span></span>
<span data-ttu-id="b9175-123">ETag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="b9175-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="b9175-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b9175-124">-InputObject</span></span>
<span data-ttu-id="b9175-125">Viel Geräte Bereitstellungsdienst-Zertifikatobjekt</span><span class="sxs-lookup"><span data-stu-id="b9175-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="b9175-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b9175-126">-Name</span></span>
<span data-ttu-id="b9175-127">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="b9175-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b9175-128">-Path</span><span class="sxs-lookup"><span data-stu-id="b9175-128">-Path</span></span>
<span data-ttu-id="b9175-129">Base-64-Darstellung der Datei "X509 Certificate. cer" oder des PEM-Dateipfads</span><span class="sxs-lookup"><span data-stu-id="b9175-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="b9175-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9175-130">-ResourceGroupName</span></span>
<span data-ttu-id="b9175-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b9175-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b9175-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b9175-132">-ResourceId</span></span>
<span data-ttu-id="b9175-133">Dienstzertifikat-Ressourcen-ID für den Geräte Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="b9175-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="b9175-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9175-134">-Confirm</span></span>
<span data-ttu-id="b9175-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9175-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9175-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9175-136">-WhatIf</span></span>
<span data-ttu-id="b9175-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9175-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9175-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9175-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9175-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9175-139">CommonParameters</span></span>
<span data-ttu-id="b9175-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9175-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9175-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9175-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9175-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9175-142">INPUTS</span></span>

### <span data-ttu-id="b9175-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="b9175-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="b9175-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b9175-144">System.String</span></span>

## <span data-ttu-id="b9175-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9175-145">OUTPUTS</span></span>

### <span data-ttu-id="b9175-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="b9175-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="b9175-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9175-147">NOTES</span></span>

## <span data-ttu-id="b9175-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9175-148">RELATED LINKS</span></span>
