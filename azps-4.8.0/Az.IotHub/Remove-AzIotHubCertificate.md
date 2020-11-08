---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 3e30b7aa3d1e43844fc1fe53e860ee8b8c66f385
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008448"
---
# <span data-ttu-id="39154-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="39154-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="39154-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39154-102">SYNOPSIS</span></span>
<span data-ttu-id="39154-103">Löscht ein Azure-viel-Hub-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="39154-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="39154-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39154-104">SYNTAX</span></span>

### <span data-ttu-id="39154-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="39154-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39154-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="39154-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39154-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="39154-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39154-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39154-108">DESCRIPTION</span></span>
<span data-ttu-id="39154-109">Eine ausführliche Erläuterung der CA-Zertifikate in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="39154-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="39154-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39154-110">EXAMPLES</span></span>

### <span data-ttu-id="39154-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39154-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="39154-112">Löscht mein Zertifikat</span><span class="sxs-lookup"><span data-stu-id="39154-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="39154-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="39154-113">PARAMETERS</span></span>

### <span data-ttu-id="39154-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="39154-114">-CertificateName</span></span>
<span data-ttu-id="39154-115">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="39154-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="39154-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39154-116">-DefaultProfile</span></span>
<span data-ttu-id="39154-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39154-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39154-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="39154-118">-Etag</span></span>
<span data-ttu-id="39154-119">ETag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="39154-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="39154-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="39154-120">-InputObject</span></span>
<span data-ttu-id="39154-121">Certificate-Objekt</span><span class="sxs-lookup"><span data-stu-id="39154-121">Certificate Object</span></span>

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

### <span data-ttu-id="39154-122">-Name</span><span class="sxs-lookup"><span data-stu-id="39154-122">-Name</span></span>
<span data-ttu-id="39154-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="39154-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="39154-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39154-124">-PassThru</span></span>
<span data-ttu-id="39154-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="39154-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="39154-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39154-126">-ResourceGroupName</span></span>
<span data-ttu-id="39154-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="39154-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="39154-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="39154-128">-ResourceId</span></span>
<span data-ttu-id="39154-129">Zertifikatressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="39154-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="39154-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39154-130">-Confirm</span></span>
<span data-ttu-id="39154-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39154-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39154-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39154-132">-WhatIf</span></span>
<span data-ttu-id="39154-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39154-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39154-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39154-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39154-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39154-135">CommonParameters</span></span>
<span data-ttu-id="39154-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39154-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39154-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39154-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39154-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39154-138">INPUTS</span></span>

### <span data-ttu-id="39154-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="39154-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="39154-140">System. String</span><span class="sxs-lookup"><span data-stu-id="39154-140">System.String</span></span>

## <span data-ttu-id="39154-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39154-141">OUTPUTS</span></span>

### <span data-ttu-id="39154-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39154-142">System.Boolean</span></span>

## <span data-ttu-id="39154-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="39154-143">NOTES</span></span>

## <span data-ttu-id="39154-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39154-144">RELATED LINKS</span></span>
