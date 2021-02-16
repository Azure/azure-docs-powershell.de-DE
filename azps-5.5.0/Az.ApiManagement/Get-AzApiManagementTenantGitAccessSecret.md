---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145340"
---
# <span data-ttu-id="6c683-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="6c683-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="6c683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c683-102">SYNOPSIS</span></span>
<span data-ttu-id="6c683-103">Ruft die Git-Zugriffs-Konfigurationsschlüssel für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="6c683-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="6c683-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c683-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c683-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c683-105">DESCRIPTION</span></span>
<span data-ttu-id="6c683-106">Ruft die Git-Zugriffs-Konfigurationsschlüssel für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="6c683-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="6c683-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6c683-107">EXAMPLES</span></span>

### <span data-ttu-id="6c683-108">Beispiel 1: Erhalten der Konfiguration für den Mandantenzugriff</span><span class="sxs-lookup"><span data-stu-id="6c683-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="6c683-109">Dieser Befehl ruft die Git-Zugriffskonfigurationsschlüssel für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="6c683-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="6c683-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c683-110">PARAMETERS</span></span>

### <span data-ttu-id="6c683-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6c683-111">-Context</span></span>
<span data-ttu-id="6c683-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6c683-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6c683-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6c683-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6c683-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c683-114">-DefaultProfile</span></span>
<span data-ttu-id="6c683-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c683-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c683-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c683-116">CommonParameters</span></span>
<span data-ttu-id="6c683-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c683-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c683-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c683-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c683-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6c683-119">INPUTS</span></span>

### <span data-ttu-id="6c683-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6c683-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="6c683-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6c683-121">OUTPUTS</span></span>

### <span data-ttu-id="6c683-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="6c683-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="6c683-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6c683-123">NOTES</span></span>

## <span data-ttu-id="6c683-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6c683-124">RELATED LINKS</span></span>
