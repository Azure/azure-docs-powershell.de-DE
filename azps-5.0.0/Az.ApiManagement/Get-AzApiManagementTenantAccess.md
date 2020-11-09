---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301630"
---
# <span data-ttu-id="90530-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="90530-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="90530-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90530-102">SYNOPSIS</span></span>
<span data-ttu-id="90530-103">Ruft die Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="90530-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="90530-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90530-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90530-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90530-105">DESCRIPTION</span></span>
<span data-ttu-id="90530-106">Das Cmdlet " **Get-AzApiManagementTenantAccess** " Ruft die Mandanten Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="90530-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="90530-107">Schlüssel werden nicht in Ergebnisdetails berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="90530-107">Keys will not be included into result details.</span></span> <span data-ttu-id="90530-108">Verwenden **Sie Get-AzApiManagementTenantAccessSecret** , um Client Secret zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="90530-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="90530-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90530-109">EXAMPLES</span></span>

### <span data-ttu-id="90530-110">Beispiel 1: Abrufen der Mandanten Zugriffskonfiguration</span><span class="sxs-lookup"><span data-stu-id="90530-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="90530-111">Dieser Befehl ruft die Mandanten Zugriffskonfiguration für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="90530-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="90530-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="90530-112">PARAMETERS</span></span>

### <span data-ttu-id="90530-113">-Context</span><span class="sxs-lookup"><span data-stu-id="90530-113">-Context</span></span>
<span data-ttu-id="90530-114">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="90530-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="90530-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90530-115">-DefaultProfile</span></span>
<span data-ttu-id="90530-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90530-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90530-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90530-117">CommonParameters</span></span>
<span data-ttu-id="90530-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90530-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90530-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90530-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90530-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90530-120">INPUTS</span></span>

### <span data-ttu-id="90530-121">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="90530-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="90530-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90530-122">OUTPUTS</span></span>

### <span data-ttu-id="90530-123">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="90530-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="90530-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="90530-124">NOTES</span></span>

## <span data-ttu-id="90530-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90530-125">RELATED LINKS</span></span>

[<span data-ttu-id="90530-126">Satz-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="90530-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


