---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 868ca6f3f9f65fea5fd04dba1fc19d4db11bd65c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650932"
---
# <span data-ttu-id="13174-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="13174-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="13174-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13174-102">SYNOPSIS</span></span>
<span data-ttu-id="13174-103">Überprüft ein Azure-viel-Hub-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="13174-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="13174-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13174-104">SYNTAX</span></span>

### <span data-ttu-id="13174-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="13174-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13174-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="13174-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13174-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="13174-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13174-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13174-108">DESCRIPTION</span></span>
<span data-ttu-id="13174-109">Überprüft ein Zertifikat durch Hochladen eines Verifizierungszertifikats mit dem Verifizierungscode, der vom Cmdlet Get-AzIotHubCertificateVerificationCode abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="13174-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="13174-110">Dies ist der letzte Schritt beim Nachweis des Besitz Prozesses.</span><span class="sxs-lookup"><span data-stu-id="13174-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="13174-111">Eine ausführliche Erläuterung der CA-Zertifikate in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="13174-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="13174-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13174-112">EXAMPLES</span></span>

### <span data-ttu-id="13174-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13174-113">Example 1</span></span>
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

<span data-ttu-id="13174-114">Überprüft den Besitz des privaten My Certificate-Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="13174-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="13174-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="13174-115">PARAMETERS</span></span>

### <span data-ttu-id="13174-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="13174-116">-CertificateName</span></span>
<span data-ttu-id="13174-117">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="13174-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="13174-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13174-118">-DefaultProfile</span></span>
<span data-ttu-id="13174-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13174-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13174-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="13174-120">-Etag</span></span>
<span data-ttu-id="13174-121">ETag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="13174-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="13174-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="13174-122">-InputObject</span></span>
<span data-ttu-id="13174-123">Certificate-Objekt</span><span class="sxs-lookup"><span data-stu-id="13174-123">Certificate Object</span></span>

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

### <span data-ttu-id="13174-124">-Name</span><span class="sxs-lookup"><span data-stu-id="13174-124">-Name</span></span>
<span data-ttu-id="13174-125">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="13174-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="13174-126">-Path</span><span class="sxs-lookup"><span data-stu-id="13174-126">-Path</span></span>
<span data-ttu-id="13174-127">Base-64-Darstellung der Datei "X509 Certificate. cer" oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="13174-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="13174-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13174-128">-ResourceGroupName</span></span>
<span data-ttu-id="13174-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="13174-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="13174-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="13174-130">-ResourceId</span></span>
<span data-ttu-id="13174-131">Zertifikatressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="13174-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="13174-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="13174-132">-Confirm</span></span>
<span data-ttu-id="13174-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13174-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13174-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13174-134">-WhatIf</span></span>
<span data-ttu-id="13174-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13174-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13174-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13174-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13174-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13174-137">CommonParameters</span></span>
<span data-ttu-id="13174-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13174-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13174-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13174-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13174-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13174-140">INPUTS</span></span>

### <span data-ttu-id="13174-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="13174-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="13174-142">System. String</span><span class="sxs-lookup"><span data-stu-id="13174-142">System.String</span></span>

## <span data-ttu-id="13174-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13174-143">OUTPUTS</span></span>

### <span data-ttu-id="13174-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="13174-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="13174-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="13174-145">NOTES</span></span>

## <span data-ttu-id="13174-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13174-146">RELATED LINKS</span></span>
