---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 5cc7eb81c9ccaf461b1f2ab16e76aa662ea0f57b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483193"
---
# <span data-ttu-id="7e80c-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="7e80c-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="7e80c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e80c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e80c-103">Generiert eine SSO-URL für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7e80c-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e80c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e80c-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e80c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e80c-105">DESCRIPTION</span></span>
<span data-ttu-id="7e80c-106">Das Cmdlet " **Get-AzureRmApiManagementUserSsoUrl** " generiert eine SSO-URL (Single Sign-on, SSO) für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7e80c-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="7e80c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e80c-107">EXAMPLES</span></span>

### <span data-ttu-id="7e80c-108">Beispiel 1: Abrufen der SSO-URL eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="7e80c-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="7e80c-109">Mit diesem Befehl wird die SSO-URL eines Benutzers abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7e80c-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="7e80c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e80c-110">PARAMETERS</span></span>

### <span data-ttu-id="7e80c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7e80c-111">-Context</span></span>
<span data-ttu-id="7e80c-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7e80c-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="7e80c-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7e80c-113">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e80c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e80c-114">-DefaultProfile</span></span>
<span data-ttu-id="7e80c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e80c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e80c-116">-UserID</span><span class="sxs-lookup"><span data-stu-id="7e80c-116">-UserId</span></span>
<span data-ttu-id="7e80c-117">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="7e80c-117">Specifies a user ID.</span></span>
<span data-ttu-id="7e80c-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7e80c-118">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e80c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e80c-119">CommonParameters</span></span>
<span data-ttu-id="7e80c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e80c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e80c-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e80c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e80c-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e80c-122">INPUTS</span></span>

### <span data-ttu-id="7e80c-123">Keine</span><span class="sxs-lookup"><span data-stu-id="7e80c-123">None</span></span>
<span data-ttu-id="7e80c-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7e80c-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e80c-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e80c-125">OUTPUTS</span></span>

### <span data-ttu-id="7e80c-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7e80c-126">string</span></span>

## <span data-ttu-id="7e80c-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e80c-127">NOTES</span></span>

## <span data-ttu-id="7e80c-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e80c-128">RELATED LINKS</span></span>

[<span data-ttu-id="7e80c-129">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7e80c-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


