---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: a70e3323bbd154005f014f1064a535f45a102f8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476365"
---
# <span data-ttu-id="3367c-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3367c-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="3367c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3367c-102">SYNOPSIS</span></span>
<span data-ttu-id="3367c-103">Entfernt ein API-Verwaltungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="3367c-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3367c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3367c-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3367c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3367c-105">DESCRIPTION</span></span>
<span data-ttu-id="3367c-106">Das Cmdlet **Remove-AzureRmApiManagementCertificate** entfernt ein Azure API-Verwaltungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="3367c-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="3367c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3367c-107">EXAMPLES</span></span>

### <span data-ttu-id="3367c-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="3367c-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="3367c-109">Mit diesem Befehl wird das angegebene API-Verwaltungszertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="3367c-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="3367c-110">Da der Parameter *Force* angegeben ist, ist keine Bestätigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3367c-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="3367c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3367c-111">PARAMETERS</span></span>

### <span data-ttu-id="3367c-112">-Certificate-Nr</span><span class="sxs-lookup"><span data-stu-id="3367c-112">-CertificateId</span></span>
<span data-ttu-id="3367c-113">Gibt die ID des zu entfernenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="3367c-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="3367c-114">-Context</span><span class="sxs-lookup"><span data-stu-id="3367c-114">-Context</span></span>
<span data-ttu-id="3367c-115">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3367c-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3367c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3367c-116">-DefaultProfile</span></span>
<span data-ttu-id="3367c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3367c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3367c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3367c-118">-PassThru</span></span>
<span data-ttu-id="3367c-119">passthru</span><span class="sxs-lookup"><span data-stu-id="3367c-119">passthru</span></span>

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

### <span data-ttu-id="3367c-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3367c-120">-Confirm</span></span>
<span data-ttu-id="3367c-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3367c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3367c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3367c-122">-WhatIf</span></span>
<span data-ttu-id="3367c-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3367c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3367c-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3367c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3367c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3367c-125">CommonParameters</span></span>
<span data-ttu-id="3367c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3367c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3367c-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3367c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3367c-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3367c-128">INPUTS</span></span>

### <span data-ttu-id="3367c-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3367c-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3367c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3367c-130">System.String</span></span>

### <span data-ttu-id="3367c-131">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="3367c-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3367c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3367c-132">OUTPUTS</span></span>

### <span data-ttu-id="3367c-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3367c-133">System.Boolean</span></span>

## <span data-ttu-id="3367c-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="3367c-134">NOTES</span></span>

## <span data-ttu-id="3367c-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3367c-135">RELATED LINKS</span></span>

[<span data-ttu-id="3367c-136">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3367c-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="3367c-137">Neu – AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3367c-137">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="3367c-138">Satz-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3367c-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


