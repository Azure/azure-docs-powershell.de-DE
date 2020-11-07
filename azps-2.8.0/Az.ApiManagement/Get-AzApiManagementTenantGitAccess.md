---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 3338ae75406cc7c9253b21a52726f283f19d4ad7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658292"
---
# <span data-ttu-id="58b1e-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="58b1e-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="58b1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="58b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="58b1e-103">Ruft die git-Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="58b1e-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="58b1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="58b1e-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58b1e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58b1e-105">DESCRIPTION</span></span>
<span data-ttu-id="58b1e-106">Das Cmdlet " **Get-AzApiManagementTenantGitAccess** " Ruft die git-Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="58b1e-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="58b1e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58b1e-107">EXAMPLES</span></span>

### <span data-ttu-id="58b1e-108">Beispiel 1: Abrufen der Mandanten Zugriffskonfiguration</span><span class="sxs-lookup"><span data-stu-id="58b1e-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="58b1e-109">Dieser Befehl ruft die git-Zugriffskonfiguration für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="58b1e-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="58b1e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="58b1e-110">PARAMETERS</span></span>

### <span data-ttu-id="58b1e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="58b1e-111">-Context</span></span>
<span data-ttu-id="58b1e-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="58b1e-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="58b1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b1e-113">-DefaultProfile</span></span>
<span data-ttu-id="58b1e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="58b1e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58b1e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b1e-115">CommonParameters</span></span>
<span data-ttu-id="58b1e-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58b1e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b1e-117">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58b1e-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b1e-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="58b1e-118">INPUTS</span></span>

### <span data-ttu-id="58b1e-119">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="58b1e-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="58b1e-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="58b1e-120">OUTPUTS</span></span>

### <span data-ttu-id="58b1e-121">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="58b1e-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="58b1e-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="58b1e-122">NOTES</span></span>

## <span data-ttu-id="58b1e-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="58b1e-123">RELATED LINKS</span></span>
