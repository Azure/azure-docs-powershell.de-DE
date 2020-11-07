---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: b565c616ff493b2721486bc6916238e997397ce6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821003"
---
# <span data-ttu-id="f49c0-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f49c0-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="f49c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f49c0-102">SYNOPSIS</span></span>
<span data-ttu-id="f49c0-103">Ändert ein API-Verwaltungszertifikat, das für die gegenseitige Authentifizierung mit Back-End konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="f49c0-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="f49c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f49c0-104">SYNTAX</span></span>

### <span data-ttu-id="f49c0-105">Loadfromdatei (Standard)</span><span class="sxs-lookup"><span data-stu-id="f49c0-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f49c0-106">Unformatierte</span><span class="sxs-lookup"><span data-stu-id="f49c0-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f49c0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f49c0-107">DESCRIPTION</span></span>
<span data-ttu-id="f49c0-108">Das Cmdlet " **Satz-AzApiManagementCertificate** " ändert ein Azure API-Verwaltungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="f49c0-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="f49c0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f49c0-109">EXAMPLES</span></span>

### <span data-ttu-id="f49c0-110">Beispiel 1: Ändern eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="f49c0-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="f49c0-111">Mit diesem Befehl wird das angegebene API-Verwaltungszertifikat geändert.</span><span class="sxs-lookup"><span data-stu-id="f49c0-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="f49c0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f49c0-112">PARAMETERS</span></span>

### <span data-ttu-id="f49c0-113">-Certificate-Nr</span><span class="sxs-lookup"><span data-stu-id="f49c0-113">-CertificateId</span></span>
<span data-ttu-id="f49c0-114">Gibt die ID des zu ändernden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="f49c0-114">Specifies the ID of the certificate to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f49c0-115">-Context</span><span class="sxs-lookup"><span data-stu-id="f49c0-115">-Context</span></span>
<span data-ttu-id="f49c0-116">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f49c0-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f49c0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f49c0-117">-DefaultProfile</span></span>
<span data-ttu-id="f49c0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f49c0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f49c0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f49c0-119">-PassThru</span></span>
<span data-ttu-id="f49c0-120">passthru</span><span class="sxs-lookup"><span data-stu-id="f49c0-120">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f49c0-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="f49c0-121">-PfxBytes</span></span>
<span data-ttu-id="f49c0-122">Gibt ein Bytearray der Zertifikatsdatei im PFX-Format an.</span><span class="sxs-lookup"><span data-stu-id="f49c0-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="f49c0-123">Dieser Parameter ist erforderlich, wenn Sie den *PfxFilePath* -Parameter nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="f49c0-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f49c0-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="f49c0-124">-PfxFilePath</span></span>
<span data-ttu-id="f49c0-125">Gibt den Pfad zur Zertifikatsdatei im PFX-Format zum Erstellen und Hochladen an.</span><span class="sxs-lookup"><span data-stu-id="f49c0-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="f49c0-126">Dieser Parameter ist erforderlich, wenn Sie den *PfxBytes* -Parameter nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="f49c0-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f49c0-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="f49c0-127">-PfxPassword</span></span>
<span data-ttu-id="f49c0-128">Gibt das Kennwort für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="f49c0-128">Specifies the password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f49c0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49c0-129">CommonParameters</span></span>
<span data-ttu-id="f49c0-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f49c0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49c0-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f49c0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49c0-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f49c0-132">INPUTS</span></span>

### <span data-ttu-id="f49c0-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f49c0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f49c0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f49c0-134">System.String</span></span>

### <span data-ttu-id="f49c0-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="f49c0-135">System.Byte[]</span></span>

### <span data-ttu-id="f49c0-136">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="f49c0-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f49c0-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f49c0-137">OUTPUTS</span></span>

### <span data-ttu-id="f49c0-138">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f49c0-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="f49c0-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f49c0-139">NOTES</span></span>

## <span data-ttu-id="f49c0-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f49c0-140">RELATED LINKS</span></span>

[<span data-ttu-id="f49c0-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f49c0-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="f49c0-142">Neu – AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f49c0-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="f49c0-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f49c0-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


