---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 52d40ed69adda157a8fdacd9d6c961f88508fbb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650388"
---
# <span data-ttu-id="322d4-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="322d4-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="322d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="322d4-102">SYNOPSIS</span></span>
<span data-ttu-id="322d4-103">Ruft API-Verwaltungszertifikate ab, die für die gegenseitige Authentifizierung mit Back-End im Dienst konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="322d4-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="322d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="322d4-104">SYNTAX</span></span>

### <span data-ttu-id="322d4-105">GetAllCertificates (Standard)</span><span class="sxs-lookup"><span data-stu-id="322d4-105">GetAllCertificates (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="322d4-106">GetByCertificateId</span><span class="sxs-lookup"><span data-stu-id="322d4-106">GetByCertificateId</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="322d4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="322d4-107">DESCRIPTION</span></span>
<span data-ttu-id="322d4-108">Das Cmdlet " **Get-AzApiManagementCertificate** " ruft alle Azure API-Verwaltungszertifikate oder-Zertifikate ab, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="322d4-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="322d4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="322d4-109">EXAMPLES</span></span>

### <span data-ttu-id="322d4-110">Beispiel 1: Abrufen aller Zertifikate</span><span class="sxs-lookup"><span data-stu-id="322d4-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="322d4-111">Dieser Befehl ruft alle API-Verwaltungszertifikate ab.</span><span class="sxs-lookup"><span data-stu-id="322d4-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="322d4-112">Beispiel 2: Abrufen eines Zertifikats anhand seiner ID</span><span class="sxs-lookup"><span data-stu-id="322d4-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="322d4-113">Dieser Befehl ruft das API-Verwaltungszertifikat mit der angegebenen ID ab.</span><span class="sxs-lookup"><span data-stu-id="322d4-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="322d4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="322d4-114">PARAMETERS</span></span>

### <span data-ttu-id="322d4-115">-Certificate-Nr</span><span class="sxs-lookup"><span data-stu-id="322d4-115">-CertificateId</span></span>
<span data-ttu-id="322d4-116">Gibt die ID des abzurufenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="322d4-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCertificateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="322d4-117">-Context</span><span class="sxs-lookup"><span data-stu-id="322d4-117">-Context</span></span>
<span data-ttu-id="322d4-118">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="322d4-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="322d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="322d4-119">-DefaultProfile</span></span>
<span data-ttu-id="322d4-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="322d4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="322d4-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="322d4-121">-Confirm</span></span>
<span data-ttu-id="322d4-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="322d4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="322d4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="322d4-123">-WhatIf</span></span>
<span data-ttu-id="322d4-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="322d4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="322d4-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="322d4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="322d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="322d4-126">CommonParameters</span></span>
<span data-ttu-id="322d4-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="322d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="322d4-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="322d4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="322d4-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="322d4-129">INPUTS</span></span>

### <span data-ttu-id="322d4-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="322d4-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="322d4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="322d4-131">System.String</span></span>

## <span data-ttu-id="322d4-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="322d4-132">OUTPUTS</span></span>

### <span data-ttu-id="322d4-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="322d4-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="322d4-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="322d4-134">NOTES</span></span>

## <span data-ttu-id="322d4-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="322d4-135">RELATED LINKS</span></span>

[<span data-ttu-id="322d4-136">Neu – AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="322d4-136">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="322d4-137">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="322d4-137">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="322d4-138">Satz-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="322d4-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


