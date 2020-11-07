---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: e03bb9f8f996c274abe07dd3e1b005760756d632
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651279"
---
# <span data-ttu-id="12827-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="12827-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="12827-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12827-102">SYNOPSIS</span></span>
<span data-ttu-id="12827-103">Löschen eines Azure-to-Service-Zertifikats für Hub-Device-Bereitstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="12827-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="12827-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12827-104">SYNTAX</span></span>

### <span data-ttu-id="12827-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="12827-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12827-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="12827-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12827-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="12827-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12827-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12827-108">DESCRIPTION</span></span>
<span data-ttu-id="12827-109">Eine ausführliche Erläuterung der CA-Zertifikate im Azure-Service-Bereitstellungsdienst für Hub-Geräte finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="12827-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="12827-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12827-110">EXAMPLES</span></span>

### <span data-ttu-id="12827-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="12827-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="12827-112">Löschen Sie "mein Zertifikat" in einem Azure viel-Bereitstellungsdienst für Hub-Geräte.</span><span class="sxs-lookup"><span data-stu-id="12827-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="12827-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="12827-113">PARAMETERS</span></span>

### <span data-ttu-id="12827-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="12827-114">-CertificateName</span></span>
<span data-ttu-id="12827-115">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="12827-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="12827-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12827-116">-DefaultProfile</span></span>
<span data-ttu-id="12827-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12827-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12827-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="12827-118">-Etag</span></span>
<span data-ttu-id="12827-119">ETag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="12827-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="12827-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12827-120">-InputObject</span></span>
<span data-ttu-id="12827-121">Viel Geräte Bereitstellungsdienst-Zertifikatobjekt</span><span class="sxs-lookup"><span data-stu-id="12827-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="12827-122">-Name</span><span class="sxs-lookup"><span data-stu-id="12827-122">-Name</span></span>
<span data-ttu-id="12827-123">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="12827-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="12827-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12827-124">-PassThru</span></span>
<span data-ttu-id="12827-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="12827-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="12827-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12827-126">-ResourceGroupName</span></span>
<span data-ttu-id="12827-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="12827-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="12827-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="12827-128">-ResourceId</span></span>
<span data-ttu-id="12827-129">Dienstzertifikat-Ressourcen-ID für den Geräte Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="12827-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="12827-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12827-130">-Confirm</span></span>
<span data-ttu-id="12827-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12827-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12827-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12827-132">-WhatIf</span></span>
<span data-ttu-id="12827-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12827-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12827-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12827-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12827-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12827-135">CommonParameters</span></span>
<span data-ttu-id="12827-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12827-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12827-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12827-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12827-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12827-138">INPUTS</span></span>

### <span data-ttu-id="12827-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="12827-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="12827-140">System. String</span><span class="sxs-lookup"><span data-stu-id="12827-140">System.String</span></span>

## <span data-ttu-id="12827-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12827-141">OUTPUTS</span></span>

### <span data-ttu-id="12827-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12827-142">System.Boolean</span></span>

## <span data-ttu-id="12827-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="12827-143">NOTES</span></span>

## <span data-ttu-id="12827-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12827-144">RELATED LINKS</span></span>
