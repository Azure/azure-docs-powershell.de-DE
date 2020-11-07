---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 9cf6f5a86107e35bb29a9a6dc0b0a02e0e84c47f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844000"
---
# <span data-ttu-id="068fc-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="068fc-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="068fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="068fc-102">SYNOPSIS</span></span>
<span data-ttu-id="068fc-103">Erstellen/Aktualisieren eines Azure-viel-Hub-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="068fc-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="068fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="068fc-104">SYNTAX</span></span>

### <span data-ttu-id="068fc-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="068fc-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="068fc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="068fc-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="068fc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="068fc-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="068fc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="068fc-108">DESCRIPTION</span></span>
<span data-ttu-id="068fc-109">Lädt ein neues Zertifikat hoch oder ersetzt das vorhandene Zertifikat durch denselben Namen.</span><span class="sxs-lookup"><span data-stu-id="068fc-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="068fc-110">Eine ausführliche Erläuterung der CA-Zertifikate in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="068fc-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="068fc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="068fc-111">EXAMPLES</span></span>

### <span data-ttu-id="068fc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="068fc-112">Example 1</span></span>
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

<span data-ttu-id="068fc-113">Lädt eine Zertifikat-CER-Datei für eine Zertifizierungsstelle in einen viel Hub hoch.</span><span class="sxs-lookup"><span data-stu-id="068fc-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="068fc-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="068fc-114">Example 2</span></span>
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

<span data-ttu-id="068fc-115">Aktualisiert ein CA-Zertifikat in einem viel Hub durch Hochladen einer neuen CER-Datei.</span><span class="sxs-lookup"><span data-stu-id="068fc-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="068fc-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="068fc-116">PARAMETERS</span></span>

### <span data-ttu-id="068fc-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="068fc-117">-CertificateName</span></span>
<span data-ttu-id="068fc-118">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="068fc-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="068fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="068fc-119">-DefaultProfile</span></span>
<span data-ttu-id="068fc-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="068fc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="068fc-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="068fc-121">-Etag</span></span>
<span data-ttu-id="068fc-122">ETag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="068fc-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="068fc-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="068fc-123">-InputObject</span></span>
<span data-ttu-id="068fc-124">Certificate-Objekt</span><span class="sxs-lookup"><span data-stu-id="068fc-124">Certificate Object</span></span>

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

### <span data-ttu-id="068fc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="068fc-125">-Name</span></span>
<span data-ttu-id="068fc-126">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="068fc-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="068fc-127">-Path</span><span class="sxs-lookup"><span data-stu-id="068fc-127">-Path</span></span>
<span data-ttu-id="068fc-128">Base-64-Darstellung der Datei "X509 Certificate. cer" oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="068fc-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="068fc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="068fc-129">-ResourceGroupName</span></span>
<span data-ttu-id="068fc-130">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="068fc-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="068fc-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="068fc-131">-ResourceId</span></span>
<span data-ttu-id="068fc-132">Zertifikatressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="068fc-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="068fc-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="068fc-133">-Confirm</span></span>
<span data-ttu-id="068fc-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="068fc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="068fc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="068fc-135">-WhatIf</span></span>
<span data-ttu-id="068fc-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="068fc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="068fc-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="068fc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="068fc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="068fc-138">CommonParameters</span></span>
<span data-ttu-id="068fc-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="068fc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="068fc-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="068fc-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="068fc-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="068fc-141">INPUTS</span></span>

### <span data-ttu-id="068fc-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="068fc-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="068fc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="068fc-143">System.String</span></span>

## <span data-ttu-id="068fc-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="068fc-144">OUTPUTS</span></span>

### <span data-ttu-id="068fc-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="068fc-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="068fc-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="068fc-146">NOTES</span></span>

## <span data-ttu-id="068fc-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="068fc-147">RELATED LINKS</span></span>
