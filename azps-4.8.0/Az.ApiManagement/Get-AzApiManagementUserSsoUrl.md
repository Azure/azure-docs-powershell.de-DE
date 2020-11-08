---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008210"
---
# <span data-ttu-id="f8216-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="f8216-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="f8216-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8216-102">SYNOPSIS</span></span>
<span data-ttu-id="f8216-103">Generiert eine SSO-URL für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f8216-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="f8216-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8216-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8216-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8216-105">DESCRIPTION</span></span>
<span data-ttu-id="f8216-106">Das Cmdlet " **Get-AzApiManagementUserSsoUrl** " generiert eine SSO-URL (Single Sign-on, SSO) für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f8216-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="f8216-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8216-107">EXAMPLES</span></span>

### <span data-ttu-id="f8216-108">Beispiel 1: Abrufen der SSO-URL eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="f8216-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="f8216-109">Mit diesem Befehl wird die SSO-URL eines Benutzers abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f8216-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="f8216-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8216-110">PARAMETERS</span></span>

### <span data-ttu-id="f8216-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f8216-111">-Context</span></span>
<span data-ttu-id="f8216-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f8216-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f8216-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f8216-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f8216-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8216-114">-DefaultProfile</span></span>
<span data-ttu-id="f8216-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8216-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8216-116">-UserID</span><span class="sxs-lookup"><span data-stu-id="f8216-116">-UserId</span></span>
<span data-ttu-id="f8216-117">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="f8216-117">Specifies a user ID.</span></span>
<span data-ttu-id="f8216-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f8216-118">This parameter is required.</span></span>

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

### <span data-ttu-id="f8216-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8216-119">CommonParameters</span></span>
<span data-ttu-id="f8216-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8216-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8216-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8216-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8216-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8216-122">INPUTS</span></span>

### <span data-ttu-id="f8216-123">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f8216-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f8216-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f8216-124">System.String</span></span>

## <span data-ttu-id="f8216-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8216-125">OUTPUTS</span></span>

### <span data-ttu-id="f8216-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f8216-126">System.String</span></span>

## <span data-ttu-id="f8216-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8216-127">NOTES</span></span>

## <span data-ttu-id="f8216-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8216-128">RELATED LINKS</span></span>

[<span data-ttu-id="f8216-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f8216-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


