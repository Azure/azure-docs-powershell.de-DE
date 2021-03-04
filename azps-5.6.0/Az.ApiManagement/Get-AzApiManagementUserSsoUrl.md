---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: b4c89a1f0da5e4ce07d9d2174fce031365e09cb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932152"
---
# <span data-ttu-id="0d8fe-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="0d8fe-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="0d8fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="0d8fe-103">Generiert eine SSO-URL für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="0d8fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d8fe-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d8fe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d8fe-105">DESCRIPTION</span></span>
<span data-ttu-id="0d8fe-106">Das **Cmdlet Get-AzApiManagementUserSsoUrl** generiert eine SSO-URL (Single Sign-On) für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="0d8fe-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0d8fe-107">EXAMPLES</span></span>

### <span data-ttu-id="0d8fe-108">Beispiel 1: Erhalten der SSO-URL eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="0d8fe-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="0d8fe-109">Dieser Befehl ruft die SSO-URL eines Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="0d8fe-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0d8fe-110">PARAMETERS</span></span>

### <span data-ttu-id="0d8fe-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0d8fe-111">-Context</span></span>
<span data-ttu-id="0d8fe-112">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0d8fe-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0d8fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d8fe-114">-DefaultProfile</span></span>
<span data-ttu-id="0d8fe-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d8fe-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="0d8fe-116">-UserId</span></span>
<span data-ttu-id="0d8fe-117">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-117">Specifies a user ID.</span></span>
<span data-ttu-id="0d8fe-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0d8fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d8fe-119">CommonParameters</span></span>
<span data-ttu-id="0d8fe-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d8fe-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d8fe-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d8fe-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0d8fe-122">INPUTS</span></span>

### <span data-ttu-id="0d8fe-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0d8fe-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0d8fe-124">System.String</span><span class="sxs-lookup"><span data-stu-id="0d8fe-124">System.String</span></span>

## <span data-ttu-id="0d8fe-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0d8fe-125">OUTPUTS</span></span>

### <span data-ttu-id="0d8fe-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0d8fe-126">System.String</span></span>

## <span data-ttu-id="0d8fe-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0d8fe-127">NOTES</span></span>

## <span data-ttu-id="0d8fe-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0d8fe-128">RELATED LINKS</span></span>

[<span data-ttu-id="0d8fe-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0d8fe-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


