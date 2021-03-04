---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 7796dae8d9eac66c3dd5b8fa22ed92c2c3c0b232
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942563"
---
# <span data-ttu-id="f4d72-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="f4d72-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="f4d72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4d72-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d72-103">Erstellen/Aktualisieren eines Azure IoT Hub-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="f4d72-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="f4d72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4d72-104">SYNTAX</span></span>

### <span data-ttu-id="f4d72-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4d72-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4d72-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f4d72-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4d72-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f4d72-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4d72-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4d72-108">DESCRIPTION</span></span>
<span data-ttu-id="f4d72-109">Lädt ein neues Zertifikat hoch, oder ersetzen Sie das vorhandene Zertifikat durch denselben Namen.</span><span class="sxs-lookup"><span data-stu-id="f4d72-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="f4d72-110">Eine detaillierte Erläuterung der Zertifizierungsstellenzertifikate in Azure IoT Hub finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="f4d72-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="f4d72-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4d72-111">EXAMPLES</span></span>

### <span data-ttu-id="f4d72-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4d72-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="f4d72-113">Lädt eine Zertifizierungsstellenzertifikat-CER-Datei in einen IoT-Hub hoch.</span><span class="sxs-lookup"><span data-stu-id="f4d72-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="f4d72-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f4d72-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="f4d72-115">Aktualisiert ein Zertifizierungsstellenzertifikat in einem IoT-Hub, indem eine neue CER-Datei hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="f4d72-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="f4d72-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f4d72-116">PARAMETERS</span></span>

### <span data-ttu-id="f4d72-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="f4d72-117">-CertificateName</span></span>
<span data-ttu-id="f4d72-118">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="f4d72-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="f4d72-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d72-119">-DefaultProfile</span></span>
<span data-ttu-id="f4d72-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4d72-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4d72-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="f4d72-121">-Etag</span></span>
<span data-ttu-id="f4d72-122">Etag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="f4d72-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="f4d72-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4d72-123">-InputObject</span></span>
<span data-ttu-id="f4d72-124">Zertifikatobjekt</span><span class="sxs-lookup"><span data-stu-id="f4d72-124">Certificate Object</span></span>

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

### <span data-ttu-id="f4d72-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f4d72-125">-Name</span></span>
<span data-ttu-id="f4d72-126">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="f4d72-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f4d72-127">-Path</span><span class="sxs-lookup"><span data-stu-id="f4d72-127">-Path</span></span>
<span data-ttu-id="f4d72-128">Base-64-Darstellung der X509-Zertifikat-CER-Datei oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="f4d72-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="f4d72-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d72-129">-ResourceGroupName</span></span>
<span data-ttu-id="f4d72-130">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f4d72-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f4d72-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4d72-131">-ResourceId</span></span>
<span data-ttu-id="f4d72-132">Zertifikatressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f4d72-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="f4d72-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4d72-133">-Confirm</span></span>
<span data-ttu-id="f4d72-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4d72-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4d72-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4d72-135">-WhatIf</span></span>
<span data-ttu-id="f4d72-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4d72-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4d72-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4d72-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4d72-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d72-138">CommonParameters</span></span>
<span data-ttu-id="f4d72-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d72-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d72-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4d72-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d72-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4d72-141">INPUTS</span></span>

### <span data-ttu-id="f4d72-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="f4d72-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="f4d72-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f4d72-143">System.String</span></span>

## <span data-ttu-id="f4d72-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4d72-144">OUTPUTS</span></span>

### <span data-ttu-id="f4d72-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="f4d72-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="f4d72-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f4d72-146">NOTES</span></span>

## <span data-ttu-id="f4d72-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f4d72-147">RELATED LINKS</span></span>
