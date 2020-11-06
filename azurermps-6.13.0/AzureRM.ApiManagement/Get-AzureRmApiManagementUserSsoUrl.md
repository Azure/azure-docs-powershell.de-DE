---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 485150470bce308d3ab6d1a9a70eabd887abab09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498542"
---
# <span data-ttu-id="66860-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="66860-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="66860-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66860-102">SYNOPSIS</span></span>
<span data-ttu-id="66860-103">Generiert eine SSO-URL für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="66860-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66860-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66860-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66860-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66860-105">DESCRIPTION</span></span>
<span data-ttu-id="66860-106">Das Cmdlet " **Get-AzureRmApiManagementUserSsoUrl** " generiert eine SSO-URL (Single Sign-on, SSO) für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="66860-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="66860-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66860-107">EXAMPLES</span></span>

### <span data-ttu-id="66860-108">Beispiel 1: Abrufen der SSO-URL eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="66860-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="66860-109">Mit diesem Befehl wird die SSO-URL eines Benutzers abgerufen.</span><span class="sxs-lookup"><span data-stu-id="66860-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="66860-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="66860-110">PARAMETERS</span></span>

### <span data-ttu-id="66860-111">-Context</span><span class="sxs-lookup"><span data-stu-id="66860-111">-Context</span></span>
<span data-ttu-id="66860-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="66860-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="66860-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="66860-113">This parameter is required.</span></span>

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

### <span data-ttu-id="66860-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66860-114">-DefaultProfile</span></span>
<span data-ttu-id="66860-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66860-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66860-116">-UserID</span><span class="sxs-lookup"><span data-stu-id="66860-116">-UserId</span></span>
<span data-ttu-id="66860-117">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="66860-117">Specifies a user ID.</span></span>
<span data-ttu-id="66860-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="66860-118">This parameter is required.</span></span>

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

### <span data-ttu-id="66860-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66860-119">CommonParameters</span></span>
<span data-ttu-id="66860-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66860-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66860-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66860-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66860-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66860-122">INPUTS</span></span>

### <span data-ttu-id="66860-123">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="66860-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="66860-124">System. String</span><span class="sxs-lookup"><span data-stu-id="66860-124">System.String</span></span>

## <span data-ttu-id="66860-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66860-125">OUTPUTS</span></span>

### <span data-ttu-id="66860-126">System. String</span><span class="sxs-lookup"><span data-stu-id="66860-126">System.String</span></span>

## <span data-ttu-id="66860-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="66860-127">NOTES</span></span>

## <span data-ttu-id="66860-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66860-128">RELATED LINKS</span></span>

[<span data-ttu-id="66860-129">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="66860-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


