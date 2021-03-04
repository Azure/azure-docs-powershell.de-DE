---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: bb60ce1fc2cb20a24d1b445cf4a3729bf26747ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925336"
---
# <span data-ttu-id="d5d67-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d5d67-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="d5d67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5d67-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d67-103">Ändert ein API-Verwaltungszertifikat, das für die gegenseitige Authentifizierung mit dem Back-End konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="d5d67-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="d5d67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5d67-104">SYNTAX</span></span>

### <span data-ttu-id="d5d67-105">LoadFromFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5d67-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5d67-106">Unformatierte</span><span class="sxs-lookup"><span data-stu-id="d5d67-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5d67-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5d67-107">DESCRIPTION</span></span>
<span data-ttu-id="d5d67-108">Das **Cmdlet Set-AzApiManagementCertificate** ändert ein Azure-API-Verwaltungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="d5d67-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="d5d67-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5d67-109">EXAMPLES</span></span>

### <span data-ttu-id="d5d67-110">Beispiel 1: Ändern eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="d5d67-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="d5d67-111">Mit diesem Befehl wird das angegebene API-Verwaltungszertifikat geändert.</span><span class="sxs-lookup"><span data-stu-id="d5d67-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="d5d67-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d5d67-112">PARAMETERS</span></span>

### <span data-ttu-id="d5d67-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="d5d67-113">-CertificateId</span></span>
<span data-ttu-id="d5d67-114">Gibt die ID des zu ändernden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="d5d67-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="d5d67-115">-Context</span><span class="sxs-lookup"><span data-stu-id="d5d67-115">-Context</span></span>
<span data-ttu-id="d5d67-116">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="d5d67-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d67-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d67-117">-DefaultProfile</span></span>
<span data-ttu-id="d5d67-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5d67-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5d67-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5d67-119">-PassThru</span></span>
<span data-ttu-id="d5d67-120">passthru</span><span class="sxs-lookup"><span data-stu-id="d5d67-120">passthru</span></span>

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

### <span data-ttu-id="d5d67-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="d5d67-121">-PfxBytes</span></span>
<span data-ttu-id="d5d67-122">Gibt ein Array von Bytes der Zertifikatdatei im PFX-Format an.</span><span class="sxs-lookup"><span data-stu-id="d5d67-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="d5d67-123">Dieser Parameter ist erforderlich, wenn Sie den *Parameter PfxFilePath nicht* angeben.</span><span class="sxs-lookup"><span data-stu-id="d5d67-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="d5d67-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="d5d67-124">-PfxFilePath</span></span>
<span data-ttu-id="d5d67-125">Gibt den Pfad zur Zertifikatdatei im PFX-Format zum Erstellen und Hochladen an.</span><span class="sxs-lookup"><span data-stu-id="d5d67-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="d5d67-126">Dieser Parameter ist erforderlich, wenn Sie den *Parameter PfxBytes nicht* angeben.</span><span class="sxs-lookup"><span data-stu-id="d5d67-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="d5d67-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="d5d67-127">-PfxPassword</span></span>
<span data-ttu-id="d5d67-128">Gibt das Kennwort für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="d5d67-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="d5d67-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d67-129">CommonParameters</span></span>
<span data-ttu-id="d5d67-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5d67-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d67-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5d67-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d67-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5d67-132">INPUTS</span></span>

### <span data-ttu-id="d5d67-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d5d67-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d5d67-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d5d67-134">System.String</span></span>

### <span data-ttu-id="d5d67-135">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="d5d67-135">System.Byte[]</span></span>

### <span data-ttu-id="d5d67-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d5d67-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d5d67-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5d67-137">OUTPUTS</span></span>

### <span data-ttu-id="d5d67-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d5d67-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="d5d67-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d5d67-139">NOTES</span></span>

## <span data-ttu-id="d5d67-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d5d67-140">RELATED LINKS</span></span>

[<span data-ttu-id="d5d67-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d5d67-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="d5d67-142">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d5d67-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="d5d67-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d5d67-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


