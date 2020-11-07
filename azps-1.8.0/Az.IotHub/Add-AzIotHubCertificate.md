---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 87c7dea7e5cde48d6de6b9e9b756caf9cd2f2626
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819816"
---
# <span data-ttu-id="85b31-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="85b31-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="85b31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85b31-102">SYNOPSIS</span></span>
<span data-ttu-id="85b31-103">Erstellen/Aktualisieren eines Azure-viel-Hub-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="85b31-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="85b31-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85b31-104">SYNTAX</span></span>

### <span data-ttu-id="85b31-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="85b31-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85b31-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="85b31-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85b31-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="85b31-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85b31-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85b31-108">DESCRIPTION</span></span>
<span data-ttu-id="85b31-109">Lädt ein neues Zertifikat hoch oder ersetzt das vorhandene Zertifikat durch denselben Namen.</span><span class="sxs-lookup"><span data-stu-id="85b31-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="85b31-110">Eine ausführliche Erläuterung der CA-Zertifikate in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="85b31-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="85b31-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85b31-111">EXAMPLES</span></span>

### <span data-ttu-id="85b31-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85b31-112">Example 1</span></span>
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

<span data-ttu-id="85b31-113">Lädt eine Zertifikat-CER-Datei für eine Zertifizierungsstelle in einen viel Hub hoch.</span><span class="sxs-lookup"><span data-stu-id="85b31-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="85b31-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="85b31-114">Example 2</span></span>
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

<span data-ttu-id="85b31-115">Aktualisiert ein CA-Zertifikat in einem viel Hub durch Hochladen einer neuen CER-Datei.</span><span class="sxs-lookup"><span data-stu-id="85b31-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="85b31-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="85b31-116">PARAMETERS</span></span>

### <span data-ttu-id="85b31-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="85b31-117">-CertificateName</span></span>
<span data-ttu-id="85b31-118">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="85b31-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="85b31-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b31-119">-DefaultProfile</span></span>
<span data-ttu-id="85b31-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85b31-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85b31-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="85b31-121">-Etag</span></span>
<span data-ttu-id="85b31-122">ETag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="85b31-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="85b31-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="85b31-123">-InputObject</span></span>
<span data-ttu-id="85b31-124">Certificate-Objekt</span><span class="sxs-lookup"><span data-stu-id="85b31-124">Certificate Object</span></span>

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

### <span data-ttu-id="85b31-125">-Name</span><span class="sxs-lookup"><span data-stu-id="85b31-125">-Name</span></span>
<span data-ttu-id="85b31-126">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="85b31-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="85b31-127">-Path</span><span class="sxs-lookup"><span data-stu-id="85b31-127">-Path</span></span>
<span data-ttu-id="85b31-128">Base-64-Darstellung der Datei "X509 Certificate. cer" oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="85b31-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="85b31-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85b31-129">-ResourceGroupName</span></span>
<span data-ttu-id="85b31-130">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="85b31-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="85b31-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="85b31-131">-ResourceId</span></span>
<span data-ttu-id="85b31-132">Zertifikatressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="85b31-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="85b31-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="85b31-133">-Confirm</span></span>
<span data-ttu-id="85b31-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85b31-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85b31-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85b31-135">-WhatIf</span></span>
<span data-ttu-id="85b31-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85b31-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85b31-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85b31-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85b31-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b31-138">CommonParameters</span></span>
<span data-ttu-id="85b31-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85b31-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b31-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85b31-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b31-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85b31-141">INPUTS</span></span>

### <span data-ttu-id="85b31-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="85b31-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="85b31-143">System. String</span><span class="sxs-lookup"><span data-stu-id="85b31-143">System.String</span></span>

## <span data-ttu-id="85b31-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85b31-144">OUTPUTS</span></span>

### <span data-ttu-id="85b31-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="85b31-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="85b31-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="85b31-146">NOTES</span></span>

## <span data-ttu-id="85b31-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85b31-147">RELATED LINKS</span></span>
