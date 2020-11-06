---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 167137cbb231bbd5093b118a22d33e2102159c67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498117"
---
# <span data-ttu-id="df253-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="df253-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="df253-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df253-102">SYNOPSIS</span></span>
<span data-ttu-id="df253-103">Ruft API-Verwaltungszertifikate ab.</span><span class="sxs-lookup"><span data-stu-id="df253-103">Gets API Management certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df253-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df253-104">SYNTAX</span></span>

### <span data-ttu-id="df253-105">Abrufen aller Zertifikate (Standard)</span><span class="sxs-lookup"><span data-stu-id="df253-105">Get all certificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df253-106">Zertifikat nach ID abrufen</span><span class="sxs-lookup"><span data-stu-id="df253-106">Get certificate by ID</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df253-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df253-107">DESCRIPTION</span></span>
<span data-ttu-id="df253-108">Das Cmdlet " **Get-AzureRmApiManagementCertificate** " ruft alle Azure API-Verwaltungszertifikate oder-Zertifikate ab, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="df253-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="df253-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df253-109">EXAMPLES</span></span>

### <span data-ttu-id="df253-110">Beispiel 1: Abrufen aller Zertifikate</span><span class="sxs-lookup"><span data-stu-id="df253-110">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="df253-111">Dieser Befehl ruft alle API-Verwaltungszertifikate ab.</span><span class="sxs-lookup"><span data-stu-id="df253-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="df253-112">Beispiel 2: Abrufen eines Zertifikats anhand seiner ID</span><span class="sxs-lookup"><span data-stu-id="df253-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="df253-113">Dieser Befehl ruft das API-Verwaltungszertifikat mit der angegebenen ID ab.</span><span class="sxs-lookup"><span data-stu-id="df253-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="df253-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="df253-114">PARAMETERS</span></span>

### <span data-ttu-id="df253-115">-Certificate-Nr</span><span class="sxs-lookup"><span data-stu-id="df253-115">-CertificateId</span></span>
<span data-ttu-id="df253-116">Gibt die ID des abzurufenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="df253-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Get certificate by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df253-117">-Context</span><span class="sxs-lookup"><span data-stu-id="df253-117">-Context</span></span>
<span data-ttu-id="df253-118">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="df253-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="df253-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="df253-119">-Confirm</span></span>
<span data-ttu-id="df253-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df253-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df253-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df253-121">-WhatIf</span></span>
<span data-ttu-id="df253-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df253-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df253-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df253-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df253-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df253-124">-DefaultProfile</span></span>
<span data-ttu-id="df253-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df253-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df253-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df253-126">CommonParameters</span></span>
<span data-ttu-id="df253-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df253-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df253-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df253-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df253-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df253-129">INPUTS</span></span>

## <span data-ttu-id="df253-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df253-130">OUTPUTS</span></span>

### <span data-ttu-id="df253-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="df253-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="df253-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="df253-132">NOTES</span></span>

## <span data-ttu-id="df253-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df253-133">RELATED LINKS</span></span>

[<span data-ttu-id="df253-134">Neu – AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="df253-134">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="df253-135">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="df253-135">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="df253-136">Satz-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="df253-136">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


