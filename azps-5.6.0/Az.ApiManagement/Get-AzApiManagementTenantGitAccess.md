---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 29e15515dfb5c8db53255cd283573fec11239940
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945419"
---
# <span data-ttu-id="ea03d-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="ea03d-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="ea03d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea03d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea03d-103">Ruft die Git-Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="ea03d-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="ea03d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea03d-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea03d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea03d-105">DESCRIPTION</span></span>
<span data-ttu-id="ea03d-106">Das **Cmdlet Get-AzApiManagementTenantGitAccess** ruft die Git-Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="ea03d-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="ea03d-107">Schlüssel werden nicht in ergebnisdetails einbezogen.</span><span class="sxs-lookup"><span data-stu-id="ea03d-107">Keys will not be included into result details.</span></span> <span data-ttu-id="ea03d-108">Verwenden Sie **Get-AzApiManagementTenantGitAccessSecret,** um den Geheimtipp des Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ea03d-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="ea03d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea03d-109">EXAMPLES</span></span>

### <span data-ttu-id="ea03d-110">Beispiel 1: Konfiguration des Mandantenzugriffs</span><span class="sxs-lookup"><span data-stu-id="ea03d-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="ea03d-111">Dieser Befehl ruft die Git-Zugriffskonfiguration für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="ea03d-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="ea03d-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ea03d-112">PARAMETERS</span></span>

### <span data-ttu-id="ea03d-113">-Context</span><span class="sxs-lookup"><span data-stu-id="ea03d-113">-Context</span></span>
<span data-ttu-id="ea03d-114">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="ea03d-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ea03d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea03d-115">-DefaultProfile</span></span>
<span data-ttu-id="ea03d-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea03d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea03d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea03d-117">CommonParameters</span></span>
<span data-ttu-id="ea03d-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea03d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea03d-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea03d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea03d-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea03d-120">INPUTS</span></span>

### <span data-ttu-id="ea03d-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ea03d-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="ea03d-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea03d-122">OUTPUTS</span></span>

### <span data-ttu-id="ea03d-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="ea03d-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="ea03d-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ea03d-124">NOTES</span></span>

## <span data-ttu-id="ea03d-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ea03d-125">RELATED LINKS</span></span>
