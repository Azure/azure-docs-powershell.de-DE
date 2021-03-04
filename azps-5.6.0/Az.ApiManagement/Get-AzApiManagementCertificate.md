---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 1885f8b4f3c72ace4bad55b355e1d16013228611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928747"
---
# <span data-ttu-id="b13de-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b13de-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="b13de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b13de-102">SYNOPSIS</span></span>
<span data-ttu-id="b13de-103">Ruft API-Verwaltungszertifikate ab, die für die gegenseitige Authentifizierung mit Back-End im Dienst konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="b13de-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="b13de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b13de-104">SYNTAX</span></span>

### <span data-ttu-id="b13de-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b13de-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b13de-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b13de-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b13de-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b13de-107">DESCRIPTION</span></span>
<span data-ttu-id="b13de-108">Das **Get-AzApiManagementCertificate-Cmdlet** ruft alle von Ihnen angegebenen Azure-API-Verwaltungszertifikate oder -Zertifikate ab.</span><span class="sxs-lookup"><span data-stu-id="b13de-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="b13de-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b13de-109">EXAMPLES</span></span>

### <span data-ttu-id="b13de-110">Beispiel 1: Alle Zertifikate erhalten</span><span class="sxs-lookup"><span data-stu-id="b13de-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="b13de-111">Dieser Befehl ruft alle API-Verwaltungszertifikate ab.</span><span class="sxs-lookup"><span data-stu-id="b13de-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="b13de-112">Beispiel 2: Erhalten eines Zertifikats nach seiner ID</span><span class="sxs-lookup"><span data-stu-id="b13de-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="b13de-113">Dieser Befehl ruft das API-Verwaltungszertifikat mit der angegebenen ID ab.</span><span class="sxs-lookup"><span data-stu-id="b13de-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="b13de-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b13de-114">PARAMETERS</span></span>

### <span data-ttu-id="b13de-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="b13de-115">-CertificateId</span></span>
<span data-ttu-id="b13de-116">Gibt die ID des zertifikats an, das sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="b13de-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13de-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b13de-117">-Context</span></span>
<span data-ttu-id="b13de-118">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="b13de-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b13de-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13de-119">-DefaultProfile</span></span>
<span data-ttu-id="b13de-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b13de-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b13de-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b13de-121">-ResourceId</span></span>
<span data-ttu-id="b13de-122">Arm Resource Identifier des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="b13de-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="b13de-123">Wenn angegeben, wird versucht, das Zertifikat durch den Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="b13de-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="b13de-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b13de-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13de-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b13de-125">-Confirm</span></span>
<span data-ttu-id="b13de-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b13de-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13de-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b13de-127">-WhatIf</span></span>
<span data-ttu-id="b13de-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b13de-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b13de-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b13de-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13de-130">CommonParameters</span></span>
<span data-ttu-id="b13de-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b13de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13de-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b13de-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13de-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b13de-133">INPUTS</span></span>

### <span data-ttu-id="b13de-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b13de-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b13de-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b13de-135">System.String</span></span>

## <span data-ttu-id="b13de-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b13de-136">OUTPUTS</span></span>

### <span data-ttu-id="b13de-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b13de-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="b13de-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b13de-138">NOTES</span></span>

## <span data-ttu-id="b13de-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b13de-139">RELATED LINKS</span></span>

[<span data-ttu-id="b13de-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b13de-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="b13de-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b13de-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="b13de-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b13de-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


