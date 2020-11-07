---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
ms.openlocfilehash: de24d9d16af5b429dcf59ffc8f4cbeb7dd0654f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662925"
---
# <span data-ttu-id="6db67-101">Remove-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="6db67-101">Remove-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="6db67-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6db67-102">SYNOPSIS</span></span>
<span data-ttu-id="6db67-103">Löscht ein Azure-viel-Hub-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="6db67-103">Deletes an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6db67-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6db67-104">SYNTAX</span></span>

### <span data-ttu-id="6db67-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6db67-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6db67-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6db67-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6db67-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6db67-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6db67-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6db67-108">DESCRIPTION</span></span>
<span data-ttu-id="6db67-109">Eine ausführliche Erläuterung der CA-Zertifikate in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="6db67-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="6db67-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6db67-110">EXAMPLES</span></span>

### <span data-ttu-id="6db67-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6db67-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="6db67-112">Löscht mein Zertifikat</span><span class="sxs-lookup"><span data-stu-id="6db67-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="6db67-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6db67-113">PARAMETERS</span></span>

### <span data-ttu-id="6db67-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="6db67-114">-CertificateName</span></span>
<span data-ttu-id="6db67-115">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="6db67-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="6db67-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db67-116">-DefaultProfile</span></span>
<span data-ttu-id="6db67-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6db67-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6db67-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="6db67-118">-Etag</span></span>
<span data-ttu-id="6db67-119">ETag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="6db67-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="6db67-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6db67-120">-InputObject</span></span>
<span data-ttu-id="6db67-121">Certificate-Objekt</span><span class="sxs-lookup"><span data-stu-id="6db67-121">Certificate Object</span></span>

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

### <span data-ttu-id="6db67-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6db67-122">-Name</span></span>
<span data-ttu-id="6db67-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="6db67-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6db67-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6db67-124">-PassThru</span></span>
<span data-ttu-id="6db67-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="6db67-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6db67-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db67-126">-ResourceGroupName</span></span>
<span data-ttu-id="6db67-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6db67-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6db67-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6db67-128">-ResourceId</span></span>
<span data-ttu-id="6db67-129">Zertifikatressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6db67-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="6db67-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6db67-130">-Confirm</span></span>
<span data-ttu-id="6db67-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6db67-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6db67-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6db67-132">-WhatIf</span></span>
<span data-ttu-id="6db67-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6db67-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6db67-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6db67-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6db67-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db67-135">CommonParameters</span></span>
<span data-ttu-id="6db67-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6db67-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db67-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6db67-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db67-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6db67-138">INPUTS</span></span>

### <span data-ttu-id="6db67-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="6db67-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="6db67-140">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6db67-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="6db67-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6db67-141">System.String</span></span>

## <span data-ttu-id="6db67-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6db67-142">OUTPUTS</span></span>

### <span data-ttu-id="6db67-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6db67-143">System.Boolean</span></span>

## <span data-ttu-id="6db67-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="6db67-144">NOTES</span></span>

## <span data-ttu-id="6db67-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6db67-145">RELATED LINKS</span></span>
