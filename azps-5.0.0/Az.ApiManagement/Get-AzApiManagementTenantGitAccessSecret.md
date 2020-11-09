---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303874"
---
# <span data-ttu-id="d0540-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="d0540-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="d0540-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d0540-102">SYNOPSIS</span></span>
<span data-ttu-id="d0540-103">Ruft die git Access-Konfigurationsschlüssel für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="d0540-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="d0540-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0540-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0540-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0540-105">DESCRIPTION</span></span>
<span data-ttu-id="d0540-106">Ruft die git Access-Konfigurationsschlüssel für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="d0540-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="d0540-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0540-107">EXAMPLES</span></span>

### <span data-ttu-id="d0540-108">Beispiel 1: Abrufen der Mandanten Zugriffskonfiguration</span><span class="sxs-lookup"><span data-stu-id="d0540-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="d0540-109">Dieser Befehl ruft die git Access-Konfigurationsschlüssel für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="d0540-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="d0540-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0540-110">PARAMETERS</span></span>

### <span data-ttu-id="d0540-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d0540-111">-Context</span></span>
<span data-ttu-id="d0540-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d0540-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d0540-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d0540-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d0540-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0540-114">-DefaultProfile</span></span>
<span data-ttu-id="d0540-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d0540-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0540-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0540-116">CommonParameters</span></span>
<span data-ttu-id="d0540-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0540-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0540-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0540-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0540-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d0540-119">INPUTS</span></span>

### <span data-ttu-id="d0540-120">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d0540-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="d0540-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d0540-121">OUTPUTS</span></span>

### <span data-ttu-id="d0540-122">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="d0540-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="d0540-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="d0540-123">NOTES</span></span>

## <span data-ttu-id="d0540-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d0540-124">RELATED LINKS</span></span>
