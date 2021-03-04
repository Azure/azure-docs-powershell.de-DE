---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 5e887dc2f608dd7e26c05e3b7ca73036efe2595a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945124"
---
# <span data-ttu-id="969b7-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="969b7-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="969b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="969b7-102">SYNOPSIS</span></span>
<span data-ttu-id="969b7-103">Überprüft ein Azure IoT Hub-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="969b7-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="969b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="969b7-104">SYNTAX</span></span>

### <span data-ttu-id="969b7-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="969b7-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="969b7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="969b7-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="969b7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="969b7-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="969b7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="969b7-108">DESCRIPTION</span></span>
<span data-ttu-id="969b7-109">Überprüft ein Zertifikat, indem ein Überprüfungszertifikat hochgeladen wird, das den vom Cmdlet Get-AzIotHubCertificateVerificationCode erhaltenen Überprüfungscode enthält.</span><span class="sxs-lookup"><span data-stu-id="969b7-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="969b7-110">Dies ist der letzte Schritt im Beweisbesitzprozess.</span><span class="sxs-lookup"><span data-stu-id="969b7-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="969b7-111">Eine detaillierte Erläuterung der Zertifizierungsstellenzertifikate in Azure IoT Hub finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="969b7-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="969b7-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="969b7-112">EXAMPLES</span></span>

### <span data-ttu-id="969b7-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="969b7-113">Example 1</span></span>
```
PS C:\> Set-AzIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="969b7-114">Überprüft den Besitz des privaten MyCertificate-Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="969b7-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="969b7-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="969b7-115">PARAMETERS</span></span>

### <span data-ttu-id="969b7-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="969b7-116">-CertificateName</span></span>
<span data-ttu-id="969b7-117">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="969b7-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="969b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969b7-118">-DefaultProfile</span></span>
<span data-ttu-id="969b7-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="969b7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="969b7-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="969b7-120">-Etag</span></span>
<span data-ttu-id="969b7-121">Etag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="969b7-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="969b7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="969b7-122">-InputObject</span></span>
<span data-ttu-id="969b7-123">Zertifikatobjekt</span><span class="sxs-lookup"><span data-stu-id="969b7-123">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="969b7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="969b7-124">-Name</span></span>
<span data-ttu-id="969b7-125">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="969b7-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969b7-126">-Path</span><span class="sxs-lookup"><span data-stu-id="969b7-126">-Path</span></span>
<span data-ttu-id="969b7-127">Base-64-Darstellung der X509-Zertifikat-CER-Datei oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="969b7-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="969b7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="969b7-128">-ResourceGroupName</span></span>
<span data-ttu-id="969b7-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="969b7-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969b7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="969b7-130">-ResourceId</span></span>
<span data-ttu-id="969b7-131">Zertifikatressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="969b7-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="969b7-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="969b7-132">-Confirm</span></span>
<span data-ttu-id="969b7-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="969b7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="969b7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="969b7-134">-WhatIf</span></span>
<span data-ttu-id="969b7-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="969b7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="969b7-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="969b7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="969b7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969b7-137">CommonParameters</span></span>
<span data-ttu-id="969b7-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969b7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969b7-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="969b7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969b7-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="969b7-140">INPUTS</span></span>

### <span data-ttu-id="969b7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="969b7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="969b7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="969b7-142">System.String</span></span>

## <span data-ttu-id="969b7-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="969b7-143">OUTPUTS</span></span>

### <span data-ttu-id="969b7-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="969b7-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="969b7-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="969b7-145">NOTES</span></span>

## <span data-ttu-id="969b7-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="969b7-146">RELATED LINKS</span></span>
