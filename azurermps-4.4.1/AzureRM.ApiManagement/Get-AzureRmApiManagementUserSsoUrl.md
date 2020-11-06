---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: a13d37100e553d8d56cf5b040a796adabe08b7d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498093"
---
# <span data-ttu-id="3e111-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="3e111-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="3e111-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e111-102">SYNOPSIS</span></span>
<span data-ttu-id="3e111-103">Generiert eine SSO-URL für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3e111-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e111-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e111-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e111-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e111-105">DESCRIPTION</span></span>
<span data-ttu-id="3e111-106">Das Cmdlet " **Get-AzureRmApiManagementUserSsoUrl** " generiert eine SSO-URL (Single Sign-on, SSO) für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3e111-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="3e111-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e111-107">EXAMPLES</span></span>

### <span data-ttu-id="3e111-108">Beispiel 1: Abrufen der SSO-URL eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="3e111-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="3e111-109">Mit diesem Befehl wird die SSO-URL eines Benutzers abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3e111-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="3e111-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e111-110">PARAMETERS</span></span>

### <span data-ttu-id="3e111-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3e111-111">-Context</span></span>
<span data-ttu-id="3e111-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3e111-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="3e111-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3e111-113">This parameter is required.</span></span>

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

### <span data-ttu-id="3e111-114">-UserID</span><span class="sxs-lookup"><span data-stu-id="3e111-114">-UserId</span></span>
<span data-ttu-id="3e111-115">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="3e111-115">Specifies a user ID.</span></span>
<span data-ttu-id="3e111-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3e111-116">This parameter is required.</span></span>

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

### <span data-ttu-id="3e111-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e111-117">-DefaultProfile</span></span>
<span data-ttu-id="3e111-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3e111-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e111-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e111-119">CommonParameters</span></span>
<span data-ttu-id="3e111-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e111-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e111-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e111-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e111-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e111-122">INPUTS</span></span>

## <span data-ttu-id="3e111-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e111-123">OUTPUTS</span></span>

### <span data-ttu-id="3e111-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3e111-124">string</span></span>

## <span data-ttu-id="3e111-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e111-125">NOTES</span></span>

## <span data-ttu-id="3e111-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e111-126">RELATED LINKS</span></span>

[<span data-ttu-id="3e111-127">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3e111-127">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


