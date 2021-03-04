---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 471c861e8601317daf1e12de3a292d84bfce416e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945413"
---
# <span data-ttu-id="3b4d0-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="3b4d0-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="3b4d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b4d0-102">SYNOPSIS</span></span>
<span data-ttu-id="3b4d0-103">Ruft die Git-Zugriffskonfigurationsschlüssel für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="3b4d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b4d0-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b4d0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b4d0-105">DESCRIPTION</span></span>
<span data-ttu-id="3b4d0-106">Ruft die Git-Zugriffskonfigurationsschlüssel für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="3b4d0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3b4d0-107">EXAMPLES</span></span>

### <span data-ttu-id="3b4d0-108">Beispiel 1: Konfiguration des Mandantenzugriffs</span><span class="sxs-lookup"><span data-stu-id="3b4d0-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="3b4d0-109">Dieser Befehl ruft die Git-Zugriffskonfigurationsschlüssel für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="3b4d0-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3b4d0-110">PARAMETERS</span></span>

### <span data-ttu-id="3b4d0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3b4d0-111">-Context</span></span>
<span data-ttu-id="3b4d0-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3b4d0-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-113">This parameter is required.</span></span>

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

### <span data-ttu-id="3b4d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b4d0-114">-DefaultProfile</span></span>
<span data-ttu-id="3b4d0-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b4d0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b4d0-116">CommonParameters</span></span>
<span data-ttu-id="3b4d0-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b4d0-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b4d0-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b4d0-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3b4d0-119">INPUTS</span></span>

### <span data-ttu-id="3b4d0-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3b4d0-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="3b4d0-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3b4d0-121">OUTPUTS</span></span>

### <span data-ttu-id="3b4d0-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="3b4d0-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="3b4d0-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3b4d0-123">NOTES</span></span>

## <span data-ttu-id="3b4d0-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3b4d0-124">RELATED LINKS</span></span>
