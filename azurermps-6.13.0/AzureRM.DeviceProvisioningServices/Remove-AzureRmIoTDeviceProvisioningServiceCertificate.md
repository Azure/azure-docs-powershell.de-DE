---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 64de44e74b5c6ea21d9d49b1911bcd34a74a374a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663152"
---
# <span data-ttu-id="53fbd-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="53fbd-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="53fbd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="53fbd-103">Löschen eines Azure-to-Service-Zertifikats für Hub-Device-Bereitstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="53fbd-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53fbd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53fbd-104">SYNTAX</span></span>

### <span data-ttu-id="53fbd-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="53fbd-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53fbd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="53fbd-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53fbd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="53fbd-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53fbd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53fbd-108">DESCRIPTION</span></span>
<span data-ttu-id="53fbd-109">Eine ausführliche Erläuterung der CA-Zertifikate im Azure-Service-Bereitstellungsdienst für Hub-Geräte finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="53fbd-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="53fbd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53fbd-110">EXAMPLES</span></span>

### <span data-ttu-id="53fbd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53fbd-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="53fbd-112">Löschen Sie "mein Zertifikat" in einem Azure viel-Bereitstellungsdienst für Hub-Geräte.</span><span class="sxs-lookup"><span data-stu-id="53fbd-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="53fbd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="53fbd-113">PARAMETERS</span></span>

### <span data-ttu-id="53fbd-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="53fbd-114">-CertificateName</span></span>
<span data-ttu-id="53fbd-115">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="53fbd-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="53fbd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53fbd-116">-DefaultProfile</span></span>
<span data-ttu-id="53fbd-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53fbd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53fbd-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="53fbd-118">-Etag</span></span>
<span data-ttu-id="53fbd-119">ETag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="53fbd-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="53fbd-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="53fbd-120">-InputObject</span></span>
<span data-ttu-id="53fbd-121">Viel Geräte Bereitstellungsdienst-Zertifikatobjekt</span><span class="sxs-lookup"><span data-stu-id="53fbd-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="53fbd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="53fbd-122">-Name</span></span>
<span data-ttu-id="53fbd-123">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="53fbd-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="53fbd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53fbd-124">-PassThru</span></span>
<span data-ttu-id="53fbd-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="53fbd-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53fbd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53fbd-126">-ResourceGroupName</span></span>
<span data-ttu-id="53fbd-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="53fbd-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="53fbd-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="53fbd-128">-ResourceId</span></span>
<span data-ttu-id="53fbd-129">Dienstzertifikat-Ressourcen-ID für den Geräte Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="53fbd-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="53fbd-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="53fbd-130">-Confirm</span></span>
<span data-ttu-id="53fbd-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53fbd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53fbd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53fbd-132">-WhatIf</span></span>
<span data-ttu-id="53fbd-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53fbd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53fbd-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53fbd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53fbd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53fbd-135">CommonParameters</span></span>
<span data-ttu-id="53fbd-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53fbd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53fbd-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53fbd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53fbd-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53fbd-138">INPUTS</span></span>

### <span data-ttu-id="53fbd-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="53fbd-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="53fbd-140">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="53fbd-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="53fbd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="53fbd-141">System.String</span></span>

## <span data-ttu-id="53fbd-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53fbd-142">OUTPUTS</span></span>

### <span data-ttu-id="53fbd-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53fbd-143">System.Boolean</span></span>

## <span data-ttu-id="53fbd-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="53fbd-144">NOTES</span></span>

## <span data-ttu-id="53fbd-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53fbd-145">RELATED LINKS</span></span>
