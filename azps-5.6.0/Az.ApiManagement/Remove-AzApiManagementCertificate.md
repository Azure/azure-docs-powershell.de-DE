---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: 2a28464c735627e97551e845b1d463da9f324a5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928739"
---
# <span data-ttu-id="eb9ff-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="eb9ff-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="eb9ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb9ff-102">SYNOPSIS</span></span>
<span data-ttu-id="eb9ff-103">Entfernt ein API-Verwaltungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="eb9ff-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="eb9ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb9ff-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb9ff-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb9ff-105">DESCRIPTION</span></span>
<span data-ttu-id="eb9ff-106">Das **Cmdlet Remove-AzApiManagementCertificate** entfernt ein Azure API Management-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="eb9ff-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="eb9ff-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb9ff-107">EXAMPLES</span></span>

### <span data-ttu-id="eb9ff-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="eb9ff-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="eb9ff-109">Mit diesem Befehl wird das angegebene API-Verwaltungszertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="eb9ff-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="eb9ff-110">Da der *Parameter Erzwingen* angegeben ist, ist keine Bestätigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eb9ff-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="eb9ff-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eb9ff-111">PARAMETERS</span></span>

### <span data-ttu-id="eb9ff-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="eb9ff-112">-CertificateId</span></span>
<span data-ttu-id="eb9ff-113">Gibt die ID des zu entfernenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="eb9ff-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="eb9ff-114">-Context</span><span class="sxs-lookup"><span data-stu-id="eb9ff-114">-Context</span></span>
<span data-ttu-id="eb9ff-115">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="eb9ff-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="eb9ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb9ff-116">-DefaultProfile</span></span>
<span data-ttu-id="eb9ff-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb9ff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb9ff-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb9ff-118">-PassThru</span></span>
<span data-ttu-id="eb9ff-119">passthru</span><span class="sxs-lookup"><span data-stu-id="eb9ff-119">passthru</span></span>

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

### <span data-ttu-id="eb9ff-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eb9ff-120">-Confirm</span></span>
<span data-ttu-id="eb9ff-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb9ff-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb9ff-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb9ff-122">-WhatIf</span></span>
<span data-ttu-id="eb9ff-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb9ff-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb9ff-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb9ff-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb9ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb9ff-125">CommonParameters</span></span>
<span data-ttu-id="eb9ff-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb9ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb9ff-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb9ff-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb9ff-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb9ff-128">INPUTS</span></span>

### <span data-ttu-id="eb9ff-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="eb9ff-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="eb9ff-130">System.String</span><span class="sxs-lookup"><span data-stu-id="eb9ff-130">System.String</span></span>

### <span data-ttu-id="eb9ff-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eb9ff-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eb9ff-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb9ff-132">OUTPUTS</span></span>

### <span data-ttu-id="eb9ff-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eb9ff-133">System.Boolean</span></span>

## <span data-ttu-id="eb9ff-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eb9ff-134">NOTES</span></span>

## <span data-ttu-id="eb9ff-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eb9ff-135">RELATED LINKS</span></span>

[<span data-ttu-id="eb9ff-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="eb9ff-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="eb9ff-137">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="eb9ff-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="eb9ff-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="eb9ff-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


