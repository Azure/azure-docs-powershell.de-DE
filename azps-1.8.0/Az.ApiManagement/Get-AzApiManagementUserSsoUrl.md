---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: 2a7a4d602b8e316377496af8ccb9c119338a5c99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650362"
---
# <span data-ttu-id="5d531-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="5d531-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="5d531-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d531-102">SYNOPSIS</span></span>
<span data-ttu-id="5d531-103">Generiert eine SSO-URL für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="5d531-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="5d531-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d531-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d531-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d531-105">DESCRIPTION</span></span>
<span data-ttu-id="5d531-106">Das Cmdlet " **Get-AzApiManagementUserSsoUrl** " generiert eine SSO-URL (Single Sign-on, SSO) für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="5d531-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="5d531-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d531-107">EXAMPLES</span></span>

### <span data-ttu-id="5d531-108">Beispiel 1: Abrufen der SSO-URL eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="5d531-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="5d531-109">Mit diesem Befehl wird die SSO-URL eines Benutzers abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5d531-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="5d531-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d531-110">PARAMETERS</span></span>

### <span data-ttu-id="5d531-111">-Context</span><span class="sxs-lookup"><span data-stu-id="5d531-111">-Context</span></span>
<span data-ttu-id="5d531-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5d531-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="5d531-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5d531-113">This parameter is required.</span></span>

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

### <span data-ttu-id="5d531-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d531-114">-DefaultProfile</span></span>
<span data-ttu-id="5d531-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d531-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d531-116">-UserID</span><span class="sxs-lookup"><span data-stu-id="5d531-116">-UserId</span></span>
<span data-ttu-id="5d531-117">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="5d531-117">Specifies a user ID.</span></span>
<span data-ttu-id="5d531-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5d531-118">This parameter is required.</span></span>

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

### <span data-ttu-id="5d531-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d531-119">CommonParameters</span></span>
<span data-ttu-id="5d531-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d531-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d531-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d531-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d531-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d531-122">INPUTS</span></span>

### <span data-ttu-id="5d531-123">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5d531-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5d531-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5d531-124">System.String</span></span>

## <span data-ttu-id="5d531-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d531-125">OUTPUTS</span></span>

### <span data-ttu-id="5d531-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5d531-126">System.String</span></span>

## <span data-ttu-id="5d531-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d531-127">NOTES</span></span>

## <span data-ttu-id="5d531-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d531-128">RELATED LINKS</span></span>

[<span data-ttu-id="5d531-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5d531-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


