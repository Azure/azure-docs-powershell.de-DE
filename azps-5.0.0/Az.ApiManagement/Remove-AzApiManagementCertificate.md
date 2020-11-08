---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: ab1623addbb415b1aa2f6a104904629d94b518d6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178365"
---
# <span data-ttu-id="24075-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="24075-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="24075-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24075-102">SYNOPSIS</span></span>
<span data-ttu-id="24075-103">Entfernt ein API-Verwaltungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="24075-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="24075-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24075-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24075-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24075-105">DESCRIPTION</span></span>
<span data-ttu-id="24075-106">Das Cmdlet **Remove-AzApiManagementCertificate** entfernt ein Azure API-Verwaltungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="24075-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="24075-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24075-107">EXAMPLES</span></span>

### <span data-ttu-id="24075-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="24075-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="24075-109">Mit diesem Befehl wird das angegebene API-Verwaltungszertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="24075-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="24075-110">Da der Parameter *Force* angegeben ist, ist keine Bestätigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="24075-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="24075-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="24075-111">PARAMETERS</span></span>

### <span data-ttu-id="24075-112">-Certificate-Nr</span><span class="sxs-lookup"><span data-stu-id="24075-112">-CertificateId</span></span>
<span data-ttu-id="24075-113">Gibt die ID des zu entfernenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="24075-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="24075-114">-Context</span><span class="sxs-lookup"><span data-stu-id="24075-114">-Context</span></span>
<span data-ttu-id="24075-115">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="24075-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="24075-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24075-116">-DefaultProfile</span></span>
<span data-ttu-id="24075-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24075-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24075-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24075-118">-PassThru</span></span>
<span data-ttu-id="24075-119">passthru</span><span class="sxs-lookup"><span data-stu-id="24075-119">passthru</span></span>

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

### <span data-ttu-id="24075-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="24075-120">-Confirm</span></span>
<span data-ttu-id="24075-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24075-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24075-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24075-122">-WhatIf</span></span>
<span data-ttu-id="24075-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24075-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24075-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24075-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24075-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24075-125">CommonParameters</span></span>
<span data-ttu-id="24075-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24075-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24075-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24075-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24075-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24075-128">INPUTS</span></span>

### <span data-ttu-id="24075-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="24075-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="24075-130">System. String</span><span class="sxs-lookup"><span data-stu-id="24075-130">System.String</span></span>

### <span data-ttu-id="24075-131">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="24075-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="24075-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24075-132">OUTPUTS</span></span>

### <span data-ttu-id="24075-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="24075-133">System.Boolean</span></span>

## <span data-ttu-id="24075-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="24075-134">NOTES</span></span>

## <span data-ttu-id="24075-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24075-135">RELATED LINKS</span></span>

[<span data-ttu-id="24075-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="24075-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="24075-137">Neu – AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="24075-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="24075-138">Satz-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="24075-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


