---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: ab1623addbb415b1aa2f6a104904629d94b518d6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382148"
---
# <span data-ttu-id="23855-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="23855-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="23855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23855-102">SYNOPSIS</span></span>
<span data-ttu-id="23855-103">Entfernt ein API-Verwaltungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="23855-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="23855-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23855-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23855-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23855-105">DESCRIPTION</span></span>
<span data-ttu-id="23855-106">Das **Cmdlet "Remove-AzApiManagementCertificate"** entfernt ein Azure API Management-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="23855-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="23855-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23855-107">EXAMPLES</span></span>

### <span data-ttu-id="23855-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="23855-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="23855-109">Mit diesem Befehl wird das angegebene ZERTIFIKAT für die API-Verwaltung entfernt.</span><span class="sxs-lookup"><span data-stu-id="23855-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="23855-110">Da der *Parameter "Force"* angegeben wird, ist keine Bestätigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="23855-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="23855-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23855-111">PARAMETERS</span></span>

### <span data-ttu-id="23855-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="23855-112">-CertificateId</span></span>
<span data-ttu-id="23855-113">Gibt die ID des zu entfernenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="23855-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="23855-114">-Context</span><span class="sxs-lookup"><span data-stu-id="23855-114">-Context</span></span>
<span data-ttu-id="23855-115">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="23855-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="23855-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23855-116">-DefaultProfile</span></span>
<span data-ttu-id="23855-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23855-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23855-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23855-118">-PassThru</span></span>
<span data-ttu-id="23855-119">passthru</span><span class="sxs-lookup"><span data-stu-id="23855-119">passthru</span></span>

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

### <span data-ttu-id="23855-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23855-120">-Confirm</span></span>
<span data-ttu-id="23855-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23855-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23855-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="23855-122">-WhatIf</span></span>
<span data-ttu-id="23855-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23855-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23855-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23855-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23855-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23855-125">CommonParameters</span></span>
<span data-ttu-id="23855-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23855-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23855-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23855-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23855-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23855-128">INPUTS</span></span>

### <span data-ttu-id="23855-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="23855-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="23855-130">System.String</span><span class="sxs-lookup"><span data-stu-id="23855-130">System.String</span></span>

### <span data-ttu-id="23855-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="23855-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="23855-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23855-132">OUTPUTS</span></span>

### <span data-ttu-id="23855-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="23855-133">System.Boolean</span></span>

## <span data-ttu-id="23855-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="23855-134">NOTES</span></span>

## <span data-ttu-id="23855-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="23855-135">RELATED LINKS</span></span>

[<span data-ttu-id="23855-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="23855-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="23855-137">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="23855-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="23855-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="23855-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


