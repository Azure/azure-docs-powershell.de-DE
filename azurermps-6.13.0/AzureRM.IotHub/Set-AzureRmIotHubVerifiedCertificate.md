---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
ms.openlocfilehash: 45afd8c7f690be7785a14d336fabe7ac52a6f44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503649"
---
# <span data-ttu-id="bcbb0-101">Set-AzureRmIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="bcbb0-101">Set-AzureRmIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="bcbb0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bcbb0-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbb0-103">Überprüft ein Azure-viel-Hub-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-103">Verifies an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcbb0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcbb0-104">SYNTAX</span></span>

### <span data-ttu-id="bcbb0-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bcbb0-105">ResourceSet (Default)</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcbb0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bcbb0-106">InputObjectSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcbb0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bcbb0-107">ResourceIdSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcbb0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bcbb0-108">DESCRIPTION</span></span>
<span data-ttu-id="bcbb0-109">Überprüft ein Zertifikat durch Hochladen eines Verifizierungszertifikats mit dem Verifizierungscode, der vom Cmdlet Get-AzureRmIotHubCertificateVerificationCode abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzureRmIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="bcbb0-110">Dies ist der letzte Schritt beim Nachweis des Besitz Prozesses.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="bcbb0-111">Eine ausführliche Erläuterung der CA-Zertifikate in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="bcbb0-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="bcbb0-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bcbb0-112">EXAMPLES</span></span>

### <span data-ttu-id="bcbb0-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bcbb0-113">Example 1</span></span>
```
PS C:\> Set-AzureRmIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="bcbb0-114">Überprüft den Besitz des privaten My Certificate-Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="bcbb0-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcbb0-115">PARAMETERS</span></span>

### <span data-ttu-id="bcbb0-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="bcbb0-116">-CertificateName</span></span>
<span data-ttu-id="bcbb0-117">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="bcbb0-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="bcbb0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbb0-118">-DefaultProfile</span></span>
<span data-ttu-id="bcbb0-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcbb0-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="bcbb0-120">-Etag</span></span>
<span data-ttu-id="bcbb0-121">ETag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="bcbb0-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="bcbb0-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bcbb0-122">-InputObject</span></span>
<span data-ttu-id="bcbb0-123">Certificate-Objekt</span><span class="sxs-lookup"><span data-stu-id="bcbb0-123">Certificate Object</span></span>

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

### <span data-ttu-id="bcbb0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="bcbb0-124">-Name</span></span>
<span data-ttu-id="bcbb0-125">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="bcbb0-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bcbb0-126">-Path</span><span class="sxs-lookup"><span data-stu-id="bcbb0-126">-Path</span></span>
<span data-ttu-id="bcbb0-127">Base-64-Darstellung der Datei "X509 Certificate. cer" oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="bcbb0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcbb0-128">-ResourceGroupName</span></span>
<span data-ttu-id="bcbb0-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="bcbb0-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bcbb0-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bcbb0-130">-ResourceId</span></span>
<span data-ttu-id="bcbb0-131">Zertifikatressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="bcbb0-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="bcbb0-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bcbb0-132">-Confirm</span></span>
<span data-ttu-id="bcbb0-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcbb0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcbb0-134">-WhatIf</span></span>
<span data-ttu-id="bcbb0-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcbb0-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcbb0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbb0-137">CommonParameters</span></span>
<span data-ttu-id="bcbb0-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbb0-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcbb0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbb0-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bcbb0-140">INPUTS</span></span>

### <span data-ttu-id="bcbb0-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="bcbb0-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="bcbb0-142">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bcbb0-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="bcbb0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bcbb0-143">System.String</span></span>

## <span data-ttu-id="bcbb0-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bcbb0-144">OUTPUTS</span></span>

### <span data-ttu-id="bcbb0-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="bcbb0-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="bcbb0-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="bcbb0-146">NOTES</span></span>

## <span data-ttu-id="bcbb0-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bcbb0-147">RELATED LINKS</span></span>
