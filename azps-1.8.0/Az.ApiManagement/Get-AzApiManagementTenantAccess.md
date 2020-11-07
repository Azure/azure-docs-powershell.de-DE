---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: 2418ec3f5e9570046c37c76bdaef8f853ff819b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650367"
---
# <span data-ttu-id="eea89-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="eea89-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="eea89-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eea89-102">SYNOPSIS</span></span>
<span data-ttu-id="eea89-103">Ruft die Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="eea89-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="eea89-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eea89-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eea89-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eea89-105">DESCRIPTION</span></span>
<span data-ttu-id="eea89-106">Das Cmdlet " **Get-AzApiManagementTenantAccess** " Ruft die Mandanten Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="eea89-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="eea89-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eea89-107">EXAMPLES</span></span>

### <span data-ttu-id="eea89-108">Beispiel 1: Abrufen der Mandanten Zugriffskonfiguration</span><span class="sxs-lookup"><span data-stu-id="eea89-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="eea89-109">Dieser Befehl ruft die Mandanten Zugriffskonfiguration für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="eea89-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="eea89-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eea89-110">PARAMETERS</span></span>

### <span data-ttu-id="eea89-111">-Context</span><span class="sxs-lookup"><span data-stu-id="eea89-111">-Context</span></span>
<span data-ttu-id="eea89-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="eea89-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="eea89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea89-113">-DefaultProfile</span></span>
<span data-ttu-id="eea89-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eea89-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eea89-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea89-115">CommonParameters</span></span>
<span data-ttu-id="eea89-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea89-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea89-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea89-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea89-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eea89-118">INPUTS</span></span>

### <span data-ttu-id="eea89-119">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="eea89-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="eea89-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eea89-120">OUTPUTS</span></span>

### <span data-ttu-id="eea89-121">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="eea89-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="eea89-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="eea89-122">NOTES</span></span>

## <span data-ttu-id="eea89-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eea89-123">RELATED LINKS</span></span>

[<span data-ttu-id="eea89-124">Satz-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="eea89-124">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


