---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: 3c4151cbc6b170f8b34e70126f37e4478933744d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995634"
---
# <span data-ttu-id="36daf-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="36daf-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="36daf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36daf-102">SYNOPSIS</span></span>
<span data-ttu-id="36daf-103">Ruft die Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="36daf-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="36daf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36daf-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36daf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36daf-105">DESCRIPTION</span></span>
<span data-ttu-id="36daf-106">Das Cmdlet " **Get-AzApiManagementTenantAccess** " Ruft die Mandanten Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="36daf-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="36daf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36daf-107">EXAMPLES</span></span>

### <span data-ttu-id="36daf-108">Beispiel 1: Abrufen der Mandanten Zugriffskonfiguration</span><span class="sxs-lookup"><span data-stu-id="36daf-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="36daf-109">Dieser Befehl ruft die Mandanten Zugriffskonfiguration für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="36daf-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="36daf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="36daf-110">PARAMETERS</span></span>

### <span data-ttu-id="36daf-111">-Context</span><span class="sxs-lookup"><span data-stu-id="36daf-111">-Context</span></span>
<span data-ttu-id="36daf-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="36daf-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="36daf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36daf-113">-DefaultProfile</span></span>
<span data-ttu-id="36daf-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36daf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36daf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36daf-115">CommonParameters</span></span>
<span data-ttu-id="36daf-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36daf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36daf-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36daf-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36daf-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36daf-118">INPUTS</span></span>

### <span data-ttu-id="36daf-119">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="36daf-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="36daf-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36daf-120">OUTPUTS</span></span>

### <span data-ttu-id="36daf-121">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="36daf-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="36daf-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="36daf-122">NOTES</span></span>

## <span data-ttu-id="36daf-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36daf-123">RELATED LINKS</span></span>

[<span data-ttu-id="36daf-124">Satz-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="36daf-124">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


