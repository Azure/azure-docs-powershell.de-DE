---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 7bf54ade1d8299c539bd64ad947840b2c97d0d5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941832"
---
# <span data-ttu-id="47479-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="47479-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="47479-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47479-102">SYNOPSIS</span></span>
<span data-ttu-id="47479-103">Löscht ein Azure IoT Hub-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="47479-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="47479-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47479-104">SYNTAX</span></span>

### <span data-ttu-id="47479-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="47479-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47479-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="47479-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47479-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="47479-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47479-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47479-108">DESCRIPTION</span></span>
<span data-ttu-id="47479-109">Eine detaillierte Erläuterung der Zertifizierungsstellenzertifikate in Azure IoT Hub finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="47479-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="47479-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47479-110">EXAMPLES</span></span>

### <span data-ttu-id="47479-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="47479-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="47479-112">Löscht MyCertificate</span><span class="sxs-lookup"><span data-stu-id="47479-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="47479-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="47479-113">PARAMETERS</span></span>

### <span data-ttu-id="47479-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="47479-114">-CertificateName</span></span>
<span data-ttu-id="47479-115">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="47479-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="47479-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47479-116">-DefaultProfile</span></span>
<span data-ttu-id="47479-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47479-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47479-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="47479-118">-Etag</span></span>
<span data-ttu-id="47479-119">Etag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="47479-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="47479-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47479-120">-InputObject</span></span>
<span data-ttu-id="47479-121">Zertifikatobjekt</span><span class="sxs-lookup"><span data-stu-id="47479-121">Certificate Object</span></span>

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

### <span data-ttu-id="47479-122">-Name</span><span class="sxs-lookup"><span data-stu-id="47479-122">-Name</span></span>
<span data-ttu-id="47479-123">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="47479-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="47479-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47479-124">-PassThru</span></span>
<span data-ttu-id="47479-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="47479-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="47479-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47479-126">-ResourceGroupName</span></span>
<span data-ttu-id="47479-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="47479-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="47479-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47479-128">-ResourceId</span></span>
<span data-ttu-id="47479-129">Zertifikatressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="47479-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="47479-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47479-130">-Confirm</span></span>
<span data-ttu-id="47479-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47479-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47479-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47479-132">-WhatIf</span></span>
<span data-ttu-id="47479-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47479-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47479-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47479-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47479-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47479-135">CommonParameters</span></span>
<span data-ttu-id="47479-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47479-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47479-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47479-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47479-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47479-138">INPUTS</span></span>

### <span data-ttu-id="47479-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="47479-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="47479-140">System.String</span><span class="sxs-lookup"><span data-stu-id="47479-140">System.String</span></span>

## <span data-ttu-id="47479-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47479-141">OUTPUTS</span></span>

### <span data-ttu-id="47479-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47479-142">System.Boolean</span></span>

## <span data-ttu-id="47479-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="47479-143">NOTES</span></span>

## <span data-ttu-id="47479-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="47479-144">RELATED LINKS</span></span>
